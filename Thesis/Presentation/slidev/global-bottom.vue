<template>
  <div class="ivsd-footer">
    <span class="ivsd-footer-label">Islamic Value-Sensitive Design · Defense</span>
    <span class="ivsd-footer-page">
      <SlideCurrentNo /> / <SlidesTotal />
    </span>
  </div>
</template>

<style scoped>
.ivsd-footer {
  position: absolute;
  bottom: 10px;
  left: 32px;
  right: 32px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.65rem;
  color: rgba(31, 111, 84, 0.35);
  font-family: 'Inter', system-ui, sans-serif;
  pointer-events: none;
  z-index: 5;
}

.ivsd-footer-page {
  font-variant-numeric: tabular-nums;
}
</style>
