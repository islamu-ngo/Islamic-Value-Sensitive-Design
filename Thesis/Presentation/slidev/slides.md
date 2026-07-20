---
theme: seriph
title: Islamic Value-Sensitive Design
titleTemplate: "%s"
author: Amir Akrari
info: |
  Bachelor thesis defense deck for Islamic Value-Sensitive Design: a framework for provider-mediated software solutions.
colorSchema: light
aspectRatio: 16/9
canvasWidth: 1280
highlighter: shiki
lineNumbers: false
selectable: true
wakeLock: true
presenter: true
download: false
exportFilename: islamic-value-sensitive-design-defense
duration: 25
timer: countdown
transition: fade-out
clickAnimation: fade
comark: true
glowSeed: '42'
drawings:
  enabled: true
  persist: false
  syncAll: false
defaults:
  layout: default
  transition: fade-out
  class: ivsd-slide
themeConfig:
  primary: '#1f6f54'
created: 2026-06-06
updated: 2026-06-18
publish: false
type: research
status: active
tags:
  - topic/thesis
  - topic/islamic-value-sensitive-design
---

# Islamic Value-Sensitive Design
### A Framework for Provider-Mediated Software Solutions

<div class="mt-8 leading-8 text-lg">
  <strong>Bachelor Thesis — Applied Informatics — Odisee</strong><br />
  <strong>Author:</strong> Amir Akrari<br />
  <strong>Supervisor:</strong> Patrick Van den Broeck
</div>

<!--
Speaker notes: Good morning. This thesis develops Islamic Value-Sensitive Design, or I-VSD, as a provider-responsibility framework for software. It is not a fatwa, Sharia certification, or product certification. It is a structured way to reason from selected Islamic ethical principles to software-provider decisions while keeping evidence limits explicit.
-->

---
title: 'The Defense in One Sentence'
level: 2
class: 'ivsd-text-slide'
zoom: '0.92'
---

# The Defense in One Sentence


## I-VSD structures ethical provider reasoning from Islamic principles to software design decisions, while keeping <span>**evidence limits explicit**</span>.
In other words: Translating selected Islamic ethical principles into provider-facing software design responsibilities

<div class="grid grid-cols-2 gap-4 mt-3">
<div class="rounded border border-emerald-800/20 bg-emerald-50/70 p-4">

**It is** — Provider-responsibility framework · Design-reasoning structure · Heuristic translation method · Case-based traceability study

</div>
<div class="rounded border border-red-800/20 bg-red-50/70 p-4">

**It is not** — Islamic Ruling (Fatwa) · Certification · Product · Empirical proof of outcomes

</div>
</div>

How can selected Islamic ethical principles be translated into a reusable provider-responsibility framework for provider-mediated software solutions, and how can this framework structure ethical design decisions in the case of ISLAMU Event?

<!--
Speaker notes: This is the central claim. I am not claiming that I-VSD proves ethical outcomes. I am claiming it gives providers a reusable structure for asking better questions, documenting tradeoffs, and marking which evidence exists or is missing.
-->

---
title: 'Problem, Trust, and Scope'
level: 1
class: 'ivsd-text-slide'
zoom: '0.88'
---

# Problem, Trust, and Scope

Provider-mediated software is not neutral — data collection, defaults, pricing, moderation, and architecture all shape moral outcomes.

| low trust | higher trust |
| --- | --- |
| More verification burden | More willingness to adopt |
| More exit pressure | More tolerance for friction |
| More perceived risk | More perceived safety |

**Scope:** I-VSD applies where a provider has continuing responsibility — web platforms, SaaS, APIs, self-hostable systems, AI-native tools. Excluded: generic programming help, personal advice, full jurisprudence adjudication, product certification.

**Industry cases:** Pinterest (growth metrics can be constrained) · Redis→Valkey (license changes rupture trust) · PIA (privacy claims need architecture) · Meta (monetization can reward harm) · Mozilla (mission needs operational consistency)

> Providers continue shaping the moral environment after release. Trust is therefore a design concern.

<!--
Speaker notes: The provider controls defaults, data handling, governance rules, updates, pricing, and incentives. A user may prefer a less polished tool from a more trustworthy provider. These cases show how values, incentives, architecture, governance, and trust interact.
-->
---
title: 'Islamic Grounding and the VSD Gap'
level: 1
class: 'ivsd-text-slide'
zoom: '0.85'
---

# Islamic Grounding and the VSD Gap

**Value sources:** Quran · Sunnah · Scholarly consensus _(primary)_ — GDPR · WCAG · IEEE/ACM · Privacy by design _(complementary)_

**Selected principles:** Trust · Truthfulness · Justice · Non-Harm · Rights of People · Avoiding Interest · Avoiding Uncertainty · Avoiding Deception · Promise-Keeping · Excellence · Modesty · Avoiding Spying

Each principle becomes a provider question — _Trust → "What has been entrusted?" · Avoiding Spying → "Is collection necessary and proportionate?"_

| Standard VSD | I-VSD |
| --- | --- |
| Values emerge through stakeholders | Stakeholder input informs implementation |
| Tradeoffs remain pluralistic | Islamic principles define non-negotiable boundaries |
| Design sensitivity is central | Provider responsibility is central |

> VSD provides design-sensitivity vocabulary; Islamic sources provide normative authority. Empirical preference cannot make deception, unjustified surveillance, or riba acceptable inside I-VSD.

<!--
Speaker notes: This avoids two mistakes: reducing Islam to decoration and ignoring useful operational standards. Islamic sources set normative boundaries; compatible standards can support implementation. I-VSD does not reject stakeholder research — it limits what stakeholder preference can do.
-->

---
title: 'Harm-to-Principle Bridge'
level: 2
layout: 'image'
image: '/thesis/figure_2.3_harm-principle-bridge.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This figure is important because it connects the problem space to the framework. The thesis does not claim every harm maps equally to every principle. It shows the strongest links.
-->

---
title: 'Evidence-Level Ladder'
level: 2
layout: 'image'
image: '/thesis/figure_evidance-level-ladder.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This is one of the most important slides. The thesis currently supports conceptual grounding, design reasoning, implementation traceability, and illustrative case evidence. It does not yet have stakeholder validation or longitudinal operational evidence.
-->

---
title: 'Six I-VSD Domains'
level: 2
layout: 'image'
image: '/thesis/figure_provider-responsibility-accross-the-lifecycle.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: Provider responsibility includes funding, ownership, interface choices, architecture, support, moderation, governance, and metrics. That is why I-VSD is not only a UI framework.
-->

---
title: 'UI/UX Heuristics'
level: 2
layout: 'image'
image: '/thesis/figure_dark-pattern-interfaces-vs-i-vsd-interface.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This figure contrasts coercive and non-coercive choice architecture. It is illustrative, not a claim that the exact interface has already been implemented.
-->

---
title: 'Case-Study Boundary'
level: 1
layout: 'image'
image: '/thesis/figure_case-study-boundary.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This slide protects the thesis from overclaiming. Event is not proof of the framework. It is a worked application showing how the framework can structure concrete design decisions.
-->

---
title: 'Practitioner Workflow'
level: 2
hideInToc: true
layout: 'image'
image: '/thesis/figure_practitioner-workflow-for-i-vsd.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This figure shows how a practitioner would actually use I-VSD in a real repository context.
-->

---
title: 'Ecosystem and Deployment Model'
level: 2
layout: 'image'
image: '/thesis/figure_islamu-event-ecosystem.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: The key claim is risk reduction, not completion. Self-hosting and open-source stewardship can reduce centralization pressure, but interoperability, moderation, and operational reliability remain future evaluation areas.
-->

---
title: 'High-Level Technical Architecture'
level: 2
layout: 'image'
image: '/thesis/figure_high-level-technical-architecture.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: The architecture can support traceability and inspectability. It does not prove security, privacy, accessibility, or production maturity by itself.
-->

---
title: 'Security and Privacy Trust Boundaries'
level: 2
layout: 'image'
image: '/thesis/figure_islamu-event-security.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This is not a security audit. It shows where the design places trust boundaries: browser, BFF, API, authorization, tenancy, persistence, and auditability.
-->

---
title: 'Moderation, Verification, and Appeal Workflow'
level: 2
layout: 'image'
image: '/thesis/figure_moderation-verification-appeal-workflow.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: The point is not to claim fair moderation has already been achieved. The point is that moderation should be designed as a reviewable governance process.
-->

---
title: 'Business Model Against Enshittification'
level: 2
layout: 'image'
image: '/thesis/figure_islamu-event-business-model.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: Anti-enshittification is risk reduction, not immunity. The point is to design fewer incentives and fewer technical paths to trap users later.
-->

---
title: 'ISLAMU Event Evidence Ledger'
level: 2
layout: 'image'
image: '/thesis/figure_treacability-map-islamu-event.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This slide shows the difference between building a traceable design and proving real-world outcomes.
-->

---
title: 'Future Validation Roadmap'
level: 1
layout: 'image'
image: '/thesis/figure_i-vsd-validation-roadmap.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This roadmap is not a claim that validation has already happened. It is a research agenda for strengthening the thesis.
-->

---
title: 'The Agentic Skill'
level: 2
layout: 'image'
image: '/thesis/figure_agentic-skill.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.85'
---

<!--
Speaker notes: The skill turns the framework into something usable inside a repository. It formalizes review procedure, but it does not certify products or issue religious judgments. These families are where abstract principles become practical software design guidance.
-->

---
title: 'Agentic Derivation Protocol'
level: 2
layout: 'image'
image: '/thesis/figure_agentic-derivation-protocol.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This figure shows traceability from thesis methodology to tool structure. Each methodological step has a corresponding implementation choice in the skill.
-->

---
title: 'Agentic Implementation Layer'
level: 2
layout: 'image'
image: '/thesis/figure_agentic-implementation-layer.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: The output is a durable report with scope, evidence, findings, missing evidence, recommendations, and claim boundaries.
-->

---
title: 'Scope Gate and Refusal Logic'
level: 2
layout: 'image'
image: '/thesis/figure_scope-gate-and-refusal-logic.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

# Scope Gate and
# Refusal Logic

<!--
Speaker notes: The skill is not a generic ethics chatbot. It should refuse or narrow requests when I-VSD does not apply. That protects the framework from misuse.
-->

---
title: 'Routed Action Families'
level: 2
layout: 'image'
image: '/thesis/figure_routed-action-families.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This answers the practical question of how someone applies the framework. The skill routes different needs into structured review outputs.
-->

---
title: 'Report Contract and Evidence Ladder'
level: 2
layout: 'image'
image: '/thesis/figure_report-contract-evidence-ladder.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: The report contract prevents vague moral commentary. It forces traceability: what was reviewed, what was missing, what can be claimed, and what needs escalation.
-->

---
title: 'Moral-Diff Review'
level: 2
layout: 'image'
image: '/thesis/figure_moral-diff-review-as-implementation-traceability.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: The idea is similar to code review, but the review lenses are ethical: truthfulness, privacy, trust, continuity, provider responsibility, minimal extraction, and promise-keeping.
-->

---
title: 'Semantic Interpretation vs Deterministic Enforcement'
level: 2
layout: 'image'
image: '/thesis/figure_semantic-interpretation-vs-deterministic-enforcement.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This avoids letting an LLM become the final authority. The model helps interpret context; the enforcement logic should be deterministic and auditable.
-->

---
title: 'Future Evaluation of the Agentic Skill'
level: 2
layout: 'image'
image: '/thesis/figure_future-evaluation-agentic-skill.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: Future evaluation should test whether different agents or practitioners can use the same skill resources consistently, and whether refusal behavior works correctly.
-->

---
title: 'Assay-Backed I-VSD Governance Gate'
level: 2
layout: 'image'
image: '/thesis/figure_assay-backed-i-vsd-governance-gate.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: The gate does not automate Islamic moral judgment. It enforces declared categories and thresholds while preserving evidence.
-->

---
title: 'Hard and Soft Violation Thresholds'
level: 2
layout: 'image'
image: '/thesis/figure_hard-soft-violation-treshold-logic.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: A critical issue blocks. Warnings are not harmless; repeated warnings can become blocking governance debt.
-->

---
title: 'Local-to-CI Lifecycle Enforcement'
level: 2
layout: 'image'
image: '/thesis/figure_local-to-cli-lifecyle-enforcement-path.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This connects ethical traceability to the same lifecycle where tests, builds, scans, and deployment policy already operate.
-->

---
title: 'Evidence Bundle and Audit Trail'
level: 2
layout: 'image'
image: '/thesis/figure_evidence-bundle-and-audit-trail.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: This is not a certificate. It is an archive of the decision path so future reviewers can inspect what happened and why.
-->

---
title: 'Future Research Comparison Matrix'
level: 2
layout: 'image'
image: '/thesis/figure_future-research-comparaison-matrix-i-vsd-enforcement.png'
backgroundSize: 'contain'
class: 'ivsd-figure-slide'
zoom: '0.88'
---

<!--
Speaker notes: The matrix matters because it compares workflow capability, not moral superiority. The Assay-backed gate remains workflow enforcement only.
-->

---
title: 'Thank You'
level: 2
layout: 'end'
---

# Thank You
### Questions and discussion

Key defense reminders:

- Framework, not fatwa
- Case, not proof
- Traceability, not certification
- Future validation explicitly identified

`Islamic Value-Sensitive Design`

<!--
Speaker notes: Thank you. I welcome questions about the framework, methodology, case study, technical implementation, limitations, or future validation.
-->
