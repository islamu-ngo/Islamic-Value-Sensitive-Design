<script setup lang="ts">
/**
 * I-VSD Defense Deck — glow scene system.
 *
 * Adapted from the blurred-polygon glow system credited to @pi0 @Atinux
 * (KubeCon HK 2025-06-11 reference deck), re-tuned for a light emerald
 * thesis-defense palette. No external RNG dependency: uses a built-in
 * mulberry32 seeded PRNG so polygon distributions stay stable per slide.
 *
 * Per-slide frontmatter props:
 * - glow: 'left' | 'right' | 'top' | 'bottom' | 'full' | 'top-left' |
 *         'top-right' | 'bottom-left' | 'bottom-right' | 'center' | 'topmost'
 * - glowOpacity: number  (default 0.22 for light theme)
 * - glowHue: number      (hue-rotate degrees, default 0)
 * - glowSeed: string|false  (stable seed; 'false' = random per render)
 */
import { useNav } from '@slidev/client'
import { computed, ref, watch } from 'vue'

type Range = [number, number]
type Distribution =
  | 'full' | 'top' | 'bottom' | 'left' | 'right'
  | 'top-left' | 'top-right' | 'bottom-left' | 'bottom-right'
  | 'center' | 'topmost'

const { currentSlideRoute } = useNav()

const formatter = computed(() =>
  (currentSlideRoute.value.meta?.slide as any)?.frontmatter || {},
)
const distribution = computed(() => (formatter.value.glow || 'full') as Distribution)
const opacity = computed<number>(() => +(formatter.value.glowOpacity ?? 0.22))
const hue = computed<number>(() => +(formatter.value.glowHue || 0))
const seed = computed<string>(() =>
  formatter.value.glowSeed === 'false' || formatter.value.glowSeed === false
    ? Date.now().toString()
    : formatter.value.glowSeed || 'default',
)

const overflow = 0.3
const disturb = 0.3
const disturbChance = 0.3

/* Built-in seeded PRNG — replaces the `seedrandom` dependency. */
function hashStringToSeed(str: string): number {
  let h = 2166136261
  for (let i = 0; i < str.length; i++) {
    h ^= str.charCodeAt(i)
    h = Math.imul(h, 16777619)
  }
  return h >>> 0
}
function mulberry32(seed: number) {
  let a = seed >>> 0
  return function () {
    a |= 0
    a = (a + 0x6D2B79F5) | 0
    let t = Math.imul(a ^ (a >>> 15), 1 | a)
    t = (t + Math.imul(t ^ (t >>> 7), 61 | t)) ^ t
    return ((t ^ (t >>> 14)) >>> 0) / 4294967296
  }
}

function distributionToLimits(d: Distribution) {
  const min = -0.2
  const max = 1.2
  let x: Range = [min, max]
  let y: Range = [min, max]
  const inter = (a: Range, b: Range): Range => [Math.max(a[0], b[0]), Math.min(a[1], b[1])]

  for (const limit of d.split('-')) {
    switch (limit) {
      case 'topmost': y = inter(y, [-0.5, 0]); break
      case 'top': y = inter(y, [min, 0.6]); break
      case 'bottom': y = inter(y, [0.4, max]); break
      case 'left': x = inter(x, [min, 0.6]); break
      case 'right': x = inter(x, [0.4, max]); break
      case 'xcenter': x = inter(x, [0.25, 0.75]); break
      case 'ycenter': y = inter(y, [0.25, 0.75]); break
      case 'center': x = inter(x, [0.25, 0.75]); y = inter(y, [0.25, 0.75]); break
      case 'full': x = inter(x, [0, 1]); y = inter(y, [0, 1]); break
    }
  }
  return { x, y }
}

function dist2([x1, y1]: Range, [x2, y2]: Range) {
  return (x2 - x1) ** 2 + (y2 - y1) ** 2
}

function usePoly(count = 16) {
  function getPoints(): Range[] {
    const limits = distributionToLimits(distribution.value)
    const rng = mulberry32(hashStringToSeed(`${seed.value}-${currentSlideRoute.value.no}`))
    const between = ([a, b]: Range) => rng() * (b - a) + a
    const applyOverflow = (r: number, ov: number) => {
      r = r * (1 + ov * 2) - ov
      return rng() < disturbChance ? r + (rng() - 0.5) * disturb : r
    }
    return Array.from({ length: count }).map(() => [
      applyOverflow(between(limits.x), overflow),
      applyOverflow(between(limits.y), overflow),
    ])
  }

  const points = ref(getPoints())
  const poly = computed(() =>
    points.value.map(([x, y]) => `${x * 100}% ${y * 100}%`).join(', '),
  )

  function jumpPoints() {
    const pool = new Set(getPoints())
    points.value = points.value.map((o) => {
      let min = Infinity
      let closest: Range | undefined
      for (const n of pool) {
        const d = dist2(o, n)
        if (d < min) { min = d; closest = n }
      }
      pool.delete(closest)
      return closest as Range
    })
  }

  watch(currentSlideRoute, () => jumpPoints())
  return poly
}

const poly1 = usePoly(10)
const poly2 = usePoly(6)
const poly3 = usePoly(3)
</script>

<template>
  <div class="ivsd-bg" aria-hidden="true">
    <!-- Base gradient + accent bars (kept from v3 as a soft fallback under the glow) -->
    <span class="ivsd-base" />
    <span class="ivsd-bar-top" />
    <span class="ivsd-bar-bottom" />
    <!-- Decorative corner circles — visible only on text-design slides -->
    <span class="ivsd-corner ivsd-corner-tl" />
    <span class="ivsd-corner ivsd-corner-tr" />
    <span class="ivsd-corner ivsd-corner-bl" />
    <span class="ivsd-corner ivsd-corner-br" />
    <!-- Blurred-polygon glow (the main effect) -->
    <div
      class="ivsd-glow"
      :style="{ filter: `blur(80px) hue-rotate(${hue}deg)` }"
    >
      <div
        class="ivsd-clip ivsd-clip-1"
        :style="{ 'clip-path': `polygon(${poly1})`, opacity }"
      />
      <div
        class="ivsd-clip ivsd-clip-2"
        :style="{ 'clip-path': `polygon(${poly2})`, opacity }"
      />
      <div
        class="ivsd-clip ivsd-clip-3"
        :style="{ 'clip-path': `polygon(${poly3})`, opacity: 0.28 }"
      />
    </div>
  </div>
</template>

<style scoped>
.ivsd-bg {
  position: absolute;
  inset: 0;
  z-index: 0;
  pointer-events: none;
  overflow: hidden;
}

/* Base gradient (soft emerald) — sits under the glow as a calm fallback. */
.ivsd-base {
  position: absolute;
  inset: 0;
  background:
    radial-gradient(1200px 600px at 100% 0%, rgba(31, 111, 84, 0.06), transparent 60%),
    radial-gradient(900px 500px at 0% 100%, rgba(31, 111, 84, 0.05), transparent 55%),
    linear-gradient(160deg, #f7faf8 0%, #e9f2ec 100%);
}

.ivsd-bar-top {
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 8px;
  background: linear-gradient(90deg, #1f6f54 0%, #2d8a68 35%, #3aa67e 50%, #2d8a68 65%, #1f6f54 100%);
}

.ivsd-bar-bottom {
  position: absolute;
  bottom: 0; left: 0;
  width: 38%; height: 3px;
  background: linear-gradient(90deg, rgba(31, 111, 84, 0.55), transparent);
}

/* Decorative corner circles — hidden by default, shown on text slides. */
.ivsd-corner {
  position: absolute;
  border-radius: 50%;
  display: none;
  z-index: 1;
}
.ivsd-corner-tl {
  top: -120px; left: -120px; width: 280px; height: 280px;
  background: radial-gradient(circle at 70% 70%, rgba(31,111,84,0.18), rgba(31,111,84,0.06) 60%, transparent 75%);
}
.ivsd-corner-tr {
  top: -80px; right: -80px; width: 220px; height: 220px;
  background: radial-gradient(circle at 30% 70%, rgba(45,138,104,0.16), rgba(45,138,104,0.05) 60%, transparent 75%);
}
.ivsd-corner-bl {
  bottom: -140px; left: -140px; width: 320px; height: 320px;
  background: radial-gradient(circle at 70% 30%, rgba(31,111,84,0.15), rgba(31,111,84,0.04) 60%, transparent 75%);
}
.ivsd-corner-br {
  bottom: -100px; right: -100px; width: 260px; height: 260px;
  background: radial-gradient(circle at 30% 30%, rgba(45,138,104,0.18), rgba(45,138,104,0.06) 60%, transparent 75%);
}

/* Blurred-polygon glow */
.ivsd-glow,
.ivsd-clip {
  transition: all 2.5s ease;
}
.ivsd-glow {
  position: absolute;
  inset: 0;
  z-index: 0;
  overflow: hidden;
}
.ivsd-clip {
  position: absolute;
  inset: 0;
  aspect-ratio: 16 / 9;
  clip-path: circle(75%);
}
.ivsd-clip-1 { background: linear-gradient(to right, #1f6f54, #134a38); }
.ivsd-clip-2 { background: linear-gradient(to left, #2d8a68, #1a5a44); }
.ivsd-clip-3 { background: linear-gradient(to top, #3aa67e, #aaf7d8); }
</style>

<style>
/* Show corner shapes only on text-design slides (unscoped — reaches parent layout class). */
.slidev-layout.ivsd-text-slide .ivsd-corner {
  display: block;
}
</style>
