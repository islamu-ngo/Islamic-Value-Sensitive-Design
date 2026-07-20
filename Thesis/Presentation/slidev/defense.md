---
created: 2026-06-17
updated: 2026-06-17
publish: false
type: research
status: active
tags:
  - topic/thesis
  - topic/islamic-value-sensitive-design
---

# Thesis Defense Script: Islamic Value-Sensitive Design

This document is a full speaker script for the thesis defense slide deck in `slides.md`. It is written as a synthesis script for oral delivery, not as a replacement source document. The repeated defense boundary is intentional: **framework, not fatwa; case, not proof; traceability, not certification**.

## Slide 1 - Islamic Value-Sensitive Design

### What to say

Good morning, and thank you for being here.

My thesis is titled **Islamic Value-Sensitive Design: A Framework for Provider-Mediated Software Solutions**. The central concern of this thesis is how software providers can reason more responsibly about the moral consequences of the systems they design, operate, fund, govern, and maintain.

The phrase **provider-mediated software solutions** is important. I am not only talking about code as a technical artifact. I am talking about systems where a provider continues to shape the user""'s environment after release: through defaults, data collection, pricing, access, moderation, hosting, policies, support, ownership changes, dependencies, and long-term availability. In that kind of software, the provider is not morally absent. The provider remains part of the system.

The thesis proposes **Islamic Value-Sensitive Design**, or **I-VSD**, as a reusable provider-responsibility framework. It uses Value-Sensitive Design as a design-sensitivity reference, because VSD gives a useful vocabulary for thinking about stakeholders, values, technical design, and lived consequences. But the normative grounding of I-VSD does not come from VSD itself. It comes from selected Sunni Islamic ethical principles, such as trust, truthfulness, justice, non-harm, avoiding deception, avoiding spying, promise-keeping, excellence, and related principles.

I want to state the boundary immediately. This thesis is **not** a fatwa. It is **not** a Sharia certification. It is **not** a product certification. It does not claim that ISLAMU Event, the case study, is already empirically proven to produce trust, fairness, accessibility, security, or community benefit. The contribution is more specific: it is a structured framework for translating selected Islamic ethical principles into provider-facing software design responsibilities, and then showing how that structure can guide one concrete case.

So the defense is not: """This product is now certified Islamic.""" The defense is: """Here is a method for reasoning about provider responsibility in software from selected Islamic principles, here is how it maps into design and implementation decisions, and here is the evidence level we currently have."""

## Slide 2 - The Defense in One Sentence

### What to say

If I had to reduce the whole thesis to one sentence, it would be this:

**I-VSD structures ethical provider reasoning from Islamic principles to software design decisions, while keeping evidence limits explicit.**

There are several parts to that sentence.

First, **Islamic principles provide normative boundaries**. In this thesis, Islamic ethics is not used as decorative language. It is not added after the design work is already done. The selected principles are treated as sources of responsibility. For example, truthfulness affects marketing claims, pricing displays, AI disclaimers, and product promises. Avoiding spying affects analytics, logging, tracking, profiling, and secondary use of data. Promise-keeping affects licensing, support commitments, privacy commitments, portability, and what happens when a provider changes direction.

Second, **VSD provides design-sensitivity vocabulary**. VSD helps ask: who are the stakeholders, what values are affected, where do values become embedded in technical systems, and how can design decisions be examined conceptually, empirically, and technically? But I-VSD does not treat stakeholder preference as the final moral authority. Stakeholder input matters for implementation and lived consequences, but it cannot make deception, unjustified surveillance, or clear breach of promise acceptable inside the framework.

Third, **provider decisions are reviewed across six domains**: strategic, design, technical, operational, governance, and evaluation. This is important because many software ethics discussions stay at the UI level. But a provider""'s moral responsibility also appears in funding, licensing, architecture, data retention, moderation workflows, support, continuity, metrics, and future business changes.

Fourth, **ISLAMU Event illustrates implementation traceability**. It shows how the framework can structure decisions about curation, anti-scam safeguards, privacy, transparent fees, federation, accessibility, moderation, and open-source stewardship. But it remains a single worked application, not general validation.

Finally, **stronger claims require future validation**. The thesis currently supports conceptual grounding, design reasoning, and implementation traceability. It does not yet support claims of stakeholder trust, long-term operational success, scholarly certification, security audit success, or universal transferability.

The formula on the slide summarizes the movement:

**Islamic principles -> I-VSD domains -> provider decisions -> evidence level -> future validation.**

That final step, evidence level, is not a footnote. It is part of the framework. The claim is bounded by what the evidence can support.

## Slide 3 - Presentation Roadmap

### What to say

The defense follows the same evidence thread as the thesis.

First, I begin with the **problem and motivation**: software providers shape moral outcomes. Choices about defaults, tracking, pricing, moderation, infrastructure, and business models are not neutral. They influence user behavior, user dependence, exposure to harm, consent, trust, and the ability to exit.

Second, I explain the **Islamic ethical grounding and the VSD gap**. I-VSD builds on VSD""'s sensitivity to values and stakeholders, but it addresses a religious-normative gap: for Muslim providers who accept Islamic principles as authoritative, stakeholder preference and market pressure cannot be the final moral boundary.

Third, I explain the **construction of I-VSD**: the selected principles, the six provider domains, the principle-to-domain matrix, the derivation protocol, the evidence ladder, and the heuristic families.

Fourth, I explain the **agentic skill and formalization layer**. The thesis includes an `i-vsd` skill as a practitioner-support artifact. This is not an automated moral judge. It is a way to make the review process more repeatable, evidence-aware, and bounded.

Fifth, I apply the framework to **ISLAMU Event**. The case shows how I-VSD can structure real design decisions around Muslim community event discovery, federation, privacy, fees, moderation, accessibility, and stewardship.

Finally, I close with **discussion, limitations, future validation, and the final answer**. The limitations are not hidden. They are central to the responsible claim: this is a framework and illustrative case, not proof of outcomes.

So the evidence thread is:

**conceptual grounding -> design reasoning -> implementation traceability -> future validation.**

## Slide 4 - What This Thesis Is and Is Not

### What to say

This slide is a boundary slide, and it is one of the most important slides in the defense.

This thesis **is** a provider-responsibility framework. It asks: when a provider offers a software solution and continues to shape its operation, what responsibilities arise from selected Islamic principles?

It **is** a design-reasoning structure. It helps move from principles such as trust, truthfulness, justice, and avoiding spying to concrete provider questions: what data is collected, what promises are made, what defaults are chosen, what harms are foreseeable, what exit routes exist, and what evidence supports the provider""'s claims?

It **is** a heuristic translation method. It does not claim to solve every jurisprudential issue. Instead, it translates selected principles into design heuristics across domains: strategy, design, technical architecture, operations, governance, and evaluation.

It **is** a case-based traceability study. ISLAMU Event is used to show that the framework can be applied to real decisions, not only discussed abstractly.

But the thesis **is not** a fatwa. A fatwa requires qualified scholarly authority and a different process. This thesis does not claim that authority.

It **is not** Sharia certification. It does not certify that a product, organization, business model, or implementation is Islamically compliant.

It **is not** product certification. It does not replace security audits, privacy audits, accessibility testing, legal review, user research, operational monitoring, or community governance.

It **is not** empirical proof of outcomes. It does not prove that users trust ISLAMU Event, that harm is reduced in deployment, or that the framework works equally well across all contexts.

So the thesis supports moral design reasoning. It does not replace scholars, stakeholders, legal review, audits, operational evidence, or future validation.

## Slide 5 - Problem: Software Providers Shape Moral Outcomes

### What to say

The starting point is that software providers shape moral outcomes even when they do not describe their work in moral language.

When a provider decides what data to collect, that affects privacy, surveillance, autonomy, and trust. When a provider chooses default settings, that affects what users consent to in practice, especially users who are busy, nontechnical, vulnerable, or simply trusting. When a provider designs pricing, subscription flows, cancellation paths, and renewal notices, that affects fairness and deception. When a provider controls moderation, ranking, or recommendation systems, that affects exposure, dignity, community safety, and recourse.

Architecture also matters. A closed data format can create lock-in. A missing export function can trap a community. Weak security can expose private information. A lack of backup and migration planning can destroy community memory. A payment dependency or hosting dependency can become a point of failure. These are not only engineering concerns; they are moral infrastructure concerns.

The thesis uses conceptual grounding for this claim. It does not need to show that every provider intends harm. The point is that providers continue to shape the environment in which users act, depend, communicate, pay, organize, and trust.

So the ethical question is not only, """Did the provider avoid illegal behavior?""" It is also, """What kind of moral environment did the provider build, and what responsibilities follow from that?"""

## Slide 6 - Trust as a Practical User Constraint

### What to say

Trust is not only an abstract moral value. It is a practical user constraint.

If a tool is highly capable but the provider is not trusted, the user has to compensate. They may need to verify everything, avoid storing sensitive data, maintain backups, plan an exit route, read policies carefully, inspect logs, or avoid the product completely. The product may be technically better, but the trust burden makes it costly or unsafe to use.

By contrast, a less capable tool from a more trustworthy provider may be easier to adopt. Users may tolerate friction, missing features, or slower development if they believe the provider is honest, accountable, and aligned with their interests.

This matters because software adoption is not only about feature checklists. It is also about perceived risk, verification burden, exit pressure, and moral confidence.

In the thesis, trust is treated as a software design concern because provider behavior changes what users must do to protect themselves. If the provider""'s incentives are misaligned, users need more defenses. If the provider has broken promises, the user rationally reduces trust. If the provider has transparent architecture, clear policies, portability, and accountability, the user can make a more informed decision.

So trust is not blind. The thesis repeatedly distinguishes trustworthy design from manipulated trust. I-VSD does not ask users to trust because Islamic words are present. It asks providers to make trust more deserved, more inspectable, and more bounded by evidence.

## Slide 7 - Main Research Question

### What to say

The main research question is:

**How can selected Islamic ethical principles be translated into a reusable provider-responsibility framework for provider-mediated software solutions, and how can this framework structure ethical design decisions in the case of ISLAMU Event?**

There are two parts.

The first part is about translation: how selected Islamic principles become provider-facing responsibilities. This requires moving from high-level principles to design questions, heuristics, domains, and evidence requirements.

The second part is about application: how the framework structures decisions in ISLAMU Event. The case is not used to prove that I-VSD works in all settings. It is used to show that the framework can structure concrete reasoning.

The research question is therefore not: """Is ISLAMU Event successful?""" It is not: """Has I-VSD been empirically validated?""" It is not: """Can I issue Islamic rulings for software products?"""

The question is about building a reusable structure, applying it to one case, and explicitly stating the limits of what that application can prove.

## Slide 8 - Scope: Provider-Mediated Software Solutions

### What to say

The scope is provider-mediated software solutions.

This includes web platforms, SaaS products, APIs, self-hostable systems, mobile or cross-platform tools with ongoing server dependencies, AI-native tools, CLI or MCP-style tools, and other software where the provider continues to shape consequences after delivery.

The key is not the interface category. The key is ongoing provider responsibility. Does the provider shape data handling? Does the provider control access, availability, updates, moderation, pricing, policies, or governance? Does the provider continue to influence stakeholders over time?

The thesis excludes several things. It does not try to cover all Islamic business ethics. It does not cover every kind of organizational misconduct. It does not provide generic programming help. It does not settle all jurisprudential debates. It does not certify products. It does not replace scholars.

This scope matters because it prevents the framework from becoming either too narrow or too unlimited. It is narrower than all ethics, but broader than UI design. It covers the provider""'s continuing role in the software lifecycle.

## Slide 9 - Eight Representative Software Harm Types

### What to say

The thesis organizes the problem space into representative harm types. These are not exhaustive, but they show why provider responsibility must be broad.

The first type is **deception and manipulation**: dark patterns, false urgency, fake reviews, misleading privacy claims, exaggerated AI claims, hidden fees, and broken promises.

The second is **privacy, surveillance, and data misuse**: overcollection, hidden analytics, profiling, secondary use, weak retention rules, or treating user data as a resource to exploit.

The third is **lock-in and dependency abuse**: systems that make it hard to export, migrate, self-host, interoperate, or leave without unreasonable cost.

The fourth is **exploitative monetization**: unclear pricing, manipulative renewals, high-pressure subscriptions, hidden platform fees, or revenue models that depend on confusion or dependency.

The fifth is **algorithmic opacity and AI hallucination**: systems that present uncertain outputs as authoritative, hide ranking logic, or make consequential recommendations without disclosure or review.

The sixth is **security, moderation, and provenance failure**: weak safeguards, ignored abuse reports, unclear moderation, poor appeal processes, and unreliable source attribution.

The thesis also discusses content harm and source/provenance failure in the broader typology. The reason these categories matter is that they cannot all be solved by a checklist at the end. They involve strategy, business model, design, technical architecture, operations, governance, and evaluation.

## Slide 10 - Dark Patterns as Embedded Moral Failure

### What to say

Dark patterns show why moral failure can be embedded in design rather than expressed as an explicit lie.

A provider does not need to write """we deceive users""" for deception to occur. Deception can appear in layout, button contrast, cancellation friction, pricing hierarchy, preselected options, guilt-based copy, confusing consent flows, or deliberately hidden rejection paths.

Examples include false urgency, hidden reject buttons, preselected paid options, guilt-based messages like """No thanks, I do not care about safety,""" confusing pricing, difficult cancellation, or making the harmful path easier than the protective path.

This is why I-VSD treats UI as a moral surface. A design can technically disclose information while practically steering users away from understanding it. It can satisfy a legal minimum while still violating truthfulness, trust, or sincere counsel.

The thesis does not claim that every provider uses dark patterns or that every bad interface is intentional. The claim is more careful: dark patterns motivate design scrutiny because they show how provider values become embedded in interaction design.

## Slide 11 - Harm-to-Principle Bridge

### What to say

This figure connects the problem space to the framework.

The purpose is not to say that every harm maps equally to every principle. The purpose is to show that the harm typology is not disconnected from Islamic ethical reasoning.

For example, deception and manipulation connect strongly to truthfulness, avoiding deception, avoiding excessive uncertainty, and promise-keeping. Privacy and surveillance connect strongly to trust and avoiding spying. Lock-in connects to justice, trust, and promise-keeping. Exploitative monetization connects to avoiding deception, excessive uncertainty, non-harm, and in some cases concerns around riba or impermissible funding structures. Security negligence connects to trust, non-harm, and rights of people.

So the bridge justifies why a provider-responsibility framework needs more than generic """be ethical""" language. It needs a way to move from harm patterns to principle-based provider questions.

## Slide 12 - Representative Industry Cases

### What to say

The thesis uses representative industry cases to show that values, incentives, architecture, governance, and trust interact in real software contexts.

The Pinterest child-safety example shows that a provider can choose to constrain growth metrics for safety reasons. Bill Ready""'s decision to make under-16 accounts private by default is used carefully: not as proof that every ethical decision creates growth, but as evidence that rejecting engagement maximization does not automatically equal failure.

The Redis-to-Valkey case shows how licensing and governance changes can rupture trust. Even if a company later changes direction, trust damage can persist. This connects to promise-keeping, community stewardship, open-source governance, and dependency.

Private Internet Access illustrates that privacy claims need architecture, audits, and tested history. Privacy is not just a slogan; it can be supported or undermined by technical and operational choices.

Meta and Facebook are discussed as examples where monetization can reward harm, especially when fraudulent ads, engagement incentives, or algorithmic amplification become economically valuable. The point is not to single out one company as uniquely immoral; the point is to show why business model review belongs inside software ethics.

Mozilla is used as a caution: even mission-oriented or values-oriented organizations still need operational consistency. A public-interest identity does not remove the need for clear legal wording, aligned product behavior, and trustworthy communication.

Together, these cases support a bounded lesson: ethical software provision is affected by incentives, architecture, governance, communication, and trust. Good intentions or moral branding are not enough.

## Slide 13 - Value Source Hierarchy

### What to say

This slide explains where the framework gets its normative authority.

I-VSD is religiously grounded and operationally informed.

The primary sources are the Quran, the Sunnah, scholarly consensus, and classical Islamic scholarship. The thesis also refers to major Islamic concepts and scholarly traditions, but it does so with caution: it is not issuing rulings, and it does not claim to settle contested matters.

Complementary sources include GDPR, WCAG, IEEE and ACM ethics, privacy by design, Value-Sensitive Design, Value-Based Engineering, AI governance instruments, and other professional or regulatory frameworks.

The hierarchy matters. Compatible standards help operationalize values. They can provide vocabulary, controls, checklists, audit practices, and implementation guidance. But they do not override Islamic boundaries in this framework.

For example, if a practice is legal but deceptive, legality is not enough. If a surveillance practice is allowed by a platform policy but violates trust and avoiding spying, the provider still has an ethical problem. If a business model is common but depends on confusion, dependency, or manipulation, its popularity does not make it acceptable.

So the framework is not anti-standard or anti-compliance. It uses standards where compatible. But it does not treat compliance as moral sufficiency.

## Slide 14 - Selected Islamic Principles

### What to say

The thesis selects representative Islamic principles that can be translated into provider duties.

The principles include trust, truthfulness, justice, non-harm, rights of people, avoiding interest or usury, avoiding excessive uncertainty, avoiding deception, promise-keeping, excellence, modesty, and avoiding spying.

This is not a complete manual of Islamic ethics. It is a selected set for the purpose of constructing a provider-responsibility framework. The selection is based on relevance to software provision: data, promises, pricing, access, moderation, architecture, security, marketing, and lifecycle responsibility.

For example, **trust** asks what has been entrusted to the provider: data, attention, money, infrastructure, community legitimacy, or future dependence.

**Truthfulness** asks whether claims match behavior: privacy claims, security claims, pricing claims, AI claims, roadmap claims, and product comparisons.

**Justice** asks whether access, moderation, support, pricing, enforcement, and appeal are fair.

**Non-harm** asks what foreseeable harm the provider should prevent, reduce, disclose, or monitor.

**Avoiding spying** asks whether collection and observation are necessary, proportionate, disclosed, and limited.

These principles become provider-facing questions, not merely inspirational words.

## Slide 15 - From Principle to Provider Question

### What to say

This slide shows the translation movement.

The framework does not stop at """trust is important.""" It asks: **what has been entrusted to the provider?** Is it personal data, event attendance, identity, payment information, religious community legitimacy, a promise of privacy, or dependency on infrastructure?

It does not stop at """truthfulness is important.""" It asks: **do claims match behavior?** If a website says """privacy-first,""" what evidence supports that? If it says """open source,""" can users actually build, deploy, inspect, and self-host? If it says """AI-powered,""" are limits disclosed? If it says """free,""" what are users paying with?

It does not stop at """justice is important.""" It asks: **are access, enforcement, support, moderation, and pricing fair?** Are users able to appeal? Are small organizations excluded by design? Are policies applied consistently?

It does not stop at """non-harm is important.""" It asks: **what harms are foreseeable?** Privacy leakage, scams, fraud, religious misinformation, lock-in, inaccessible interfaces, dependency, or exposure to unsafe content.

It does not stop at """promise-keeping is important.""" It asks: **what commitments must be honored over time?** Privacy promises, export promises, licensing promises, uptime promises, support promises, and community governance promises.

This is the core method: principles become provider questions, and provider questions become design heuristics and evidence requirements.

## Slide 16 - What VSD Contributes

### What to say

Value-Sensitive Design contributes a useful design vocabulary.

VSD reminds us that values are not separate from technical systems. It asks designers to identify stakeholders, analyze value tensions, and examine how values appear in technical design. Its conceptual, empirical, and technical investigations are useful for understanding how software affects people.

In this thesis, VSD is not rejected. It is used as a design-sensitivity reference.

However, VSD is not treated as the moral authority. The moral authority in I-VSD comes from selected Islamic sources and principles. VSD helps with questions like stakeholder analysis, lived effects, and design translation. Islamic sources define the normative boundaries for Muslim providers who adopt this framework.

So I-VSD is not """ordinary VSD with Islamic vocabulary added.""" It is a religiously grounded provider-responsibility framework that uses VSD where VSD is helpful.

## Slide 17 - The Methodological Gap

### What to say

The methodological gap is that stakeholder preference alone cannot override Islamic boundaries.

In many design processes, values are negotiated among stakeholders, organizational goals, and philosophical assumptions. That can be useful, but it is not enough for an explicitly Islamic provider framework.

If users prefer a deceptive interface because it gives them short-term convenience, that does not make deception acceptable. If customers prefer more surveillance because it improves targeting, that does not automatically make spying acceptable. If a business model depends on riba, hidden terms, excessive uncertainty, or manipulation, stakeholder demand does not make it ethically valid inside I-VSD.

Stakeholder input still matters. It helps understand harms, needs, accessibility, usability, cultural context, and implementation effects. But Islamic principles define non-negotiable boundaries.

This is one of the main differences between I-VSD and a purely pluralistic design framework. I-VSD says: listen to stakeholders, but do not treat preference as permission to violate clear moral constraints.

## Slide 18 - Research Design

### What to say

The research design is constructive framework-development research.

In Design Science Research terms, I-VSD is an artifact. It is a construct, model, and method: it defines concepts, maps principles to domains, gives a derivation protocol, and supports structured design reasoning.

The thesis combines four methodological ingredients.

First, **Design Science Research**, because the thesis builds a framework artifact.

Second, **normative ethics**, because the framework is grounded in selected Islamic principles rather than only in user preference or market behavior.

Third, **VSD-inspired design sensitivity**, because the framework needs to attend to stakeholders, values, technical design, and lived effects.

Fourth, **illustrative case application**, because the framework is applied to ISLAMU Event to show concrete traceability.

The evaluation criteria are coherence, traceability, usefulness, and case application. They are not empirical proof of outcomes. This distinction matters throughout the defense.

## Slide 19 - Four Research Phases

### What to say

The thesis proceeds in four phases.

The first phase is **problem framing and harm typology**. This identifies representative software harms: manipulation, surveillance, lock-in, exploitative monetization, AI opacity, security negligence, moderation harm, and source/provenance failure.

The second phase is **framework development**. Here the thesis selects principles, defines domains, builds the principle-to-domain matrix, creates the derivation protocol, and formulates heuristic families.

The third phase is the **ISLAMU Event illustrative case**. The framework is applied to a concrete software project in areas such as curation, anti-scam safeguards, privacy, payments, federation, accessibility, moderation, and stewardship.

The fourth phase is **analysis, limitations, and future validation**. This includes objections, evidence boundaries, missing validation, and future research paths.

The flow is:

**problem -> framework -> case -> evidence boundary.**

That final boundary is part of the method. The thesis does not hide what it has not yet proven.

## Slide 20 - Source Selection and Evidence Hierarchy

### What to say

Different sources support different kinds of claims.

Quran and Hadith support normative grounding, but they do not by themselves prove that a specific software architecture achieves trust or privacy.

Islamic scholarship provides context and interpretive caution, but the thesis still does not become a fatwa.

VSD and HCI literature support method and design sensitivity, but they do not supply Islamic normativity.

Standards and regulations such as GDPR, WCAG, IEEE, ACM, or AI governance instruments provide operational support. They help with controls, terminology, process, and audit vocabulary. But they do not make a system Islamically sufficient.

Industry cases support problem examples. They show patterns of trust rupture, value conflict, incentive pressure, or architecture-backed claims. But they do not prove universal rules.

ISLAMU artifacts support implementation traceability. They show that certain design decisions, architecture ideas, and governance concerns were considered. But they do not prove user outcomes.

So the source type determines the claim strength. This evidence discipline is one of the most important safeguards in the thesis.

## Slide 21 - Evidence-Level Ladder

### What to say

This slide makes the evidence boundary visible.

The current thesis supports **conceptual grounding**: it defines I-VSD, explains selected principles, and shows why provider responsibility matters.

It supports **design reasoning**: it translates principles into domains, heuristics, matrices, and provider questions.

It supports **implementation traceability**: the ISLAMU Event case shows how the framework can structure decisions and how some repository or design artifacts align with those decisions.

It supports **illustrative case evidence**: one worked case shows plausibility and concreteness.

But it does not yet include **stakeholder validation**. There are no completed interviews or surveys proving that users perceive the system as more trustworthy or fair.

It does not include **longitudinal operational evidence**. There is no deployed multi-year evidence showing reduced harm, improved trust, or successful governance.

It does not include independent scholar review, practitioner replication, security certification, privacy audit, accessibility certification, or broad comparative studies.

This ladder protects the thesis from overclaiming. It says: here is what the thesis can responsibly claim, and here is what future work must still test.

## Slide 22 - I-VSD Conceptual Model

### What to say

The conceptual model moves from sources to evidence.

At the start are **Islamic sources**. From those sources, the thesis selects representative principles relevant to software provision.

Those principles become **provider questions**. For example: what has been entrusted, what claims are being made, what harms are foreseeable, what promises must be kept, and what data collection is necessary?

The provider questions are organized through **domains**: strategic, design, technical, operational, governance, and evaluation.

Those domains structure **decisions**: funding, pricing, architecture, consent, moderation, portability, support, accessibility, and communication.

Finally, each decision needs an **evidence level**. Is this a conceptual claim, a design rationale, implementation traceability, empirical result, audit result, stakeholder finding, or future validation need?

The model is not an empirical outcome proof. It is a reasoning structure that keeps the path from principle to decision visible.

## Slide 23 - Six I-VSD Domains

### What to say

The six domains expand provider responsibility beyond interface design.

The **strategic domain** covers mission, ownership, funding, partnerships, market positioning, stewardship, and business model. If a provider""'s revenue depends on confusion, surveillance, dependency, or harmful engagement, that is not just a business issue; it is part of the ethical design problem.

The **design domain** covers UX, information architecture, defaults, accessibility, localization, persuasive patterns, pricing flows, and user comprehension.

The **technical domain** covers architecture, data governance, security, authorization, interoperability, algorithms, infrastructure, dependencies, and portability.

The **operational domain** covers maintenance, support, incident response, privacy operations, moderation operations, continuity, backup, and deprecation.

The **governance domain** covers accountability, policy, decision rights, audit trails, appeals, contribution governance, escalation, and review ownership.

The **evaluation domain** covers metrics, harm review, stakeholder feedback, post-deployment evaluation, audit evidence, and future validation.

The point is simple: if provider responsibility spans the lifecycle, then the framework must span the lifecycle too.

## Slide 24 - Principle-to-Domain Matrix

### What to say

The principle-to-domain matrix is where the framework becomes practical.

Take **trust**. Strategically, trust asks whether the provider preserves user trust and avoids business models that betray it. In design, trust asks whether risks and choices are visible. Technically, it asks whether entrusted data is protected. Operationally and governantly, it asks who is responsible when something goes wrong.

Take **truthfulness**. Strategically, it prevents exaggerated positioning. In design, it requires honest labels and understandable pricing. Technically, it requires documentation and behavior to match. Operationally, it requires truthful reporting about incidents, limitations, and changes.

Take **justice**. Strategically, it asks whether access is unfairly restricted. In design, it asks whether flows are equitable. Technically, it asks whether ranking, authorization, or automation creates unfair outcomes. Governance asks whether users have appeal and recourse.

Take **avoiding spying**. Strategically, it rejects surveillance-based business models where unjustified. In design, it requires clear privacy choices. Technically, it requires minimization, access control, retention discipline, and justified logging. Governance asks whether intrusive practices are reviewed and documented.

The full matrix in the thesis is larger, but this slide shows the pattern: principles become concrete responsibilities in each provider domain.

## Slide 25 - Normative Roles of Principles

### What to say

The selected principles do not all function in only one way.

Sometimes a principle functions as a **value**. Trust, truthfulness, justice, and excellence are goods the provider should seek.

Sometimes a principle functions as a **constraint**. For example, avoiding spying constrains what data can be collected, even if more data would improve personalization.

Sometimes a principle functions as an **interpretive heuristic**. It helps ask better questions: what would a truthful provider disclose here, what would sincere counsel require, what would justice require for appeal?

Sometimes a principle functions as a **governance rule**. Promise-keeping, for example, affects change management, licensing, support, and continuity.

Sometimes a principle functions as a **red-line prohibition**. Clear deception, unjustified surveillance, clear breach of promise, and impermissible business structures are not ordinary optimization variables.

This matters because many organizations treat ethics as a tradeoff category: if the conversion rate is high enough, if the revenue is high enough, if the market demands it, the ethical concern becomes negotiable. I-VSD rejects that for clear boundaries.

## Slide 26 - Explicit Derivation Protocol

### What to say

The derivation protocol prevents Islamic terminology from becoming decoration.

The process begins with a **principle**. For example, truthfulness.

Then it asks for the **ethical context**. What kind of situation is this? Pricing? Marketing? AI output? Privacy? Moderation?

Then it identifies the **provider responsibility**. What does the provider control? What claim is being made? What user dependence exists?

Then it identifies the **harm or tension**. Could the user be misled? Could consent be distorted? Could pricing become unclear? Could a promise be broken?

Then it converts this into a **design question**. For example: will an attentive user understand the price, the limitation, the data use, and the refusal path?

Then it becomes a **heuristic**. For example: show total cost early, separate operational emails from marketing, avoid preselected paid options, disclose AI uncertainty.

Then it asks for **evidence needed**. Does the claim require a screenshot, test, policy, audit, user study, scholar review, or future deployment data?

Finally, it records **certainty and contestability**. Is this a clear principle application? Is it disputed? Does it require qualified review?

This protocol turns moral language into traceable reasoning.

## Slide 27 - I-VSD Distinct from Ordinary VSD

### What to say

This slide clarifies that I-VSD is not simply VSD with Islamic words added.

Ordinary VSD is valuable because it helps designers think about values, stakeholders, and technical systems. But I-VSD changes the source of normative authority. It says that, for providers adopting this framework, selected Islamic principles define boundaries that cannot be overridden by stakeholder preference, market pressure, or growth metrics.

It also changes the lifecycle scope. Business model, funding, ownership, governance, support, and evaluation are treated as part of the design problem.

And it changes the evidence discipline. I-VSD repeatedly asks: what kind of claim is being made, and what evidence would be needed to support it?

So I-VSD is a religiously grounded provider-responsibility framework that uses design-sensitivity tools. It is not a rebranding of secular VSD.

## Slide 28 - Why an Agentic Skill Exists

### What to say

The thesis includes an `i-vsd` agentic skill because frameworks often fail when they remain abstract.

The skill operationalizes the framework as practitioner support. It can help route a review: is this about architecture, data governance, AI, marketing, business model, implementation, or moral-diff review? It can ask for context, identify missing evidence, and produce a durable report.

But the skill is not an automated moral judge. It does not issue fatwas. It does not certify products. It does not replace scholars, stakeholders, audits, or accountable human decision-making.

Its value is procedural. It helps make the review process more repeatable, more bounded, and more evidence-aware. It can refuse or narrow tasks when I-VSD does not apply. It can record claim boundaries. It can surface when evidence is missing.

So the skill is part of the framework""'s practical formalization. It shows how I-VSD might be used in software workflows without pretending that an LLM can become the moral authority.

## Slide 29 - Agentic Derivation Protocol

### What to say

This slide shows how the methodology becomes an artifact.

Principle selection becomes a **resource index**. The skill knows where to look for the relevant principles, domains, heuristics, and report templates.

The derivation protocol becomes **routed actions**. If the user asks about data collection, it routes toward data governance. If the user asks about a diff, it may route to moral-diff review. If the user asks about marketing copy, it routes to truthfulness and communication heuristics.

Evidence discipline becomes a **report contract**. A report should say what was reviewed, what evidence was available, what evidence was missing, what claim level is supported, and what needs escalation.

Scope caution becomes **refusal and escalation logic**. If a task asks for a Sharia ruling, the skill should refuse or narrow. If a task involves contested finance or religious content, it should flag the need for qualified scholarly review.

This is a practical way to keep the framework from becoming vague.

## Slide 30 - Scope Gate and Refusal Logic

### What to say

The scope gate protects the framework from misuse.

I-VSD applies to provider-mediated software decisions. If the question is outside that scope, the skill should narrow or refuse.

For example, if someone asks the skill to declare a product halal, that is outside scope. If someone asks for a fatwa on a financial structure, that requires qualified scholarship. If someone asks for general organizational advice not connected to software provision, that may fall outside the framework. If someone asks for a purely personal religious ruling, I-VSD is not the right tool.

Refusal logic is not a weakness. It is part of responsible design. A framework that claims to answer everything becomes dangerous. I-VSD is useful because it is bounded.

## Slide 31 - Agentic Implementation Layer

### What to say

The agentic implementation layer produces a durable review output.

That output should include the reviewed scope, the relevant domains, the principles involved, the evidence reviewed, the missing evidence, findings, recommendations, escalation needs, and claim boundaries.

The most important part is that it records what can and cannot be concluded. For example, a review might say: """This implementation shows traceability toward data minimization, but no privacy audit or user validation has been performed.""" Or: """This marketing copy is directionally truthful, but the claim `secure` requires stronger evidence."""

This makes the framework usable in real development workflows. The goal is not to produce moral theater. The goal is to preserve reasoning, evidence, and limits.

## Slide 32 - Routed Action Families

### What to say

The routed action families help practitioners use the framework in different situations.

Some reviews are **discovery or orientation** reviews: what is this system, who are the stakeholders, what provider decisions matter?

Some are **domain-specific** reviews: architecture, data governance, AI, marketing, business model, moderation, accessibility, or operations.

Some are **implementation reviews**: checking code, configuration, policies, or documentation against I-VSD concerns.

Some are **incident or anti-pattern reviews**: looking at dark patterns, privacy failures, deceptive claims, lock-in, security negligence, or governance breakdown.

The routing matters because different issues require different evidence. A pricing claim needs different evidence than a security claim. A moderation fairness claim needs different evidence than an accessibility claim. A finance concern may require scholarly review.

## Slide 33 - Moral-Diff Review

### What to say

Moral-diff review is the idea of treating changes in software like code review, but with ethical lenses.

When a pull request changes analytics, permissions, pricing copy, export behavior, moderation rules, ranking logic, or AI output labels, the ethical meaning of the diff may be significant.

The review asks questions such as: does this change weaken truthfulness? Does it increase data extraction? Does it hide a refusal path? Does it reduce portability? Does it create new dependency? Does it make a promise harder to keep? Does it remove an accessibility safeguard? Does it introduce a dark pattern? Does it increase surveillance without justification?

This is not meant to slow every small change equally. It is meant to make morally significant changes visible before they disappear into ordinary development workflow.

## Slide 34 - Semantic Interpretation vs Deterministic Enforcement

### What to say

This distinction is crucial.

An LLM or agent can help interpret context. It can read a diff, identify a possible dark pattern, notice missing evidence, or connect a change to a principle. That is semantic interpretation.

But final enforcement should be deterministic and auditable where possible. If a policy says any critical issue blocks a release, that threshold should not depend on the mood of a model. If warnings accumulate into governance debt, the counting and threshold should be transparent.

So the future direction separates interpretation from enforcement. The agent helps classify and explain. A policy engine or governance process applies declared thresholds. Humans remain accountable, and scholars or auditors are involved where necessary.

This avoids turning an LLM into a final moral authority.

## Slide 35 - Formalized Artifact Layers

### What to say

The formalized artifact layers are lightweight formalization.

They include the skill entrypoint, the resource index, the action-to-report mapping, the context and evidence gate, the claim-boundary rules, and the escalation logic.

These layers improve repeatability and traceability. They help ensure that reviews do not merely say """this feels ethical""" or """this seems Islamic.""" They force a path: what was reviewed, which principle applies, which domain is affected, what evidence exists, what evidence is missing, and what claim can be made.

But this formalization is not Islamic moral judgment itself. It is a support structure for review. It cannot guarantee completeness, sincerity, moral correctness, or scholarly validity.

## Slide 36 - Report Contract and Evidence Ladder

### What to say

The report contract forces traceability.

A useful I-VSD report should not only list recommendations. It should say what was reviewed, what was out of scope, what evidence was used, what evidence was missing, what claim level is supported, and what future validation is needed.

For example, a report might distinguish between:

Design rationale: """The system is designed to support data portability."""

Implementation traceability: """There is an export endpoint and documented schema."""

Operational evidence: """Exports have been used by real users in deployment."""

Audit evidence: """An external audit verified export completeness."""

Stakeholder evidence: """Users reported that export was understandable and usable."""

These are different strengths of claim. The report contract prevents them from being collapsed into one vague ethical statement.

## Slide 37 - Seven Heuristic Families

### What to say

The framework includes seven heuristic families.

The **architecture** family covers lock-in, data sovereignty, security, assurance, continuity, and exit.

The **UI/UX** family covers dark patterns, pricing clarity, consent, defaults, accessibility, and culturally appropriate interaction.

The **data governance** family covers collection, use, sharing, retention, deletion, export, and audit.

The **content moderation** family covers reporting, triage, review, decision, explanation, appeal, and audit.

The **AI and algorithmic** family covers disclosure, uncertainty, source integrity, bias, autonomy, and escalation.

The **marketing and communication** family covers truthful claims, attention, roadmap language, comparisons, evidence, and limitations.

The **business model** family covers funding, pricing, dependency, governance, monetization incentives, and enshittification risk.

These are design-reasoning heuristics. They do not prove outcomes by themselves, but they guide responsible provider decision-making.

## Slide 38 - Architecture Heuristics

### What to say

Architecture is moral infrastructure.

If users cannot export data, architecture affects justice and trust. If a system depends on a single provider with no migration path, architecture affects promise-keeping and continuity. If logs expose sensitive information, architecture affects privacy and avoiding spying. If authorization boundaries are weak, architecture affects rights and non-harm.

The architecture heuristics include avoiding unjustified lock-in, prioritizing data sovereignty, treating security as a moral obligation, matching assurance to sector risk, and designing for continuity and exit.

Avoiding lock-in does not mean every system must use only open standards from day one. It means exceptions should be justified, documented, and revisited. If a custom format is necessary, the provider should consider export, conversion, and migration.

Data sovereignty means users and communities should not lose control over their data simply because the provider""'s business changes. This connects to self-hosting, tenant isolation, portability, and clear ownership.

Security as a moral obligation means password hashing, key management, access control, patching, dependency review, incident response, and secure defaults are not optional polish.

But stronger claims require audits, operational evidence, and stakeholder feedback. Architecture can support trust. It does not prove trust by itself.

## Slide 39 - UI/UX Heuristics

### What to say

This slide contrasts a dark-pattern interface with an I-VSD-aligned interface.

The point is illustrative. It does not claim that the exact wireframe is implemented everywhere. It shows the design direction.

In a dark-pattern interface, the provider may hide the refusal path, preselect the paid option, use guilt language, delay price disclosure, or make cancellation harder than subscription.

In an I-VSD-aligned interface, choices are legible, refusal is available, pricing is clear, defaults are protective, claims are bounded, and the user can understand what they are accepting.

This connects to truthfulness, avoiding deception, avoiding excessive uncertainty, sincere counsel, and trust. The provider should not exploit inattention. Many users accept defaults. Therefore defaults are moral choices.

An I-VSD interface may produce lower conversion than a manipulative interface. That is not a bug in the framework. It is the point: optimization happens within permissible boundaries.

## Slide 40 - Data Governance Heuristics

### What to say

Data governance follows the lifecycle: collect, use, share, retain, delete, export, and audit.

At collection, the provider asks: is this data necessary? Is there a less intrusive alternative? Is the purpose understandable?

At use, the provider asks: is data being used for the purpose users reasonably expect, or has it become a hidden asset for unrelated goals?

At sharing, the provider asks: who receives the data, why, under what limits, and with what user understanding?

At retention, the provider asks: how long is the data kept, who can access it, and how is deletion handled?

At export, the provider asks: can users leave with their data in a usable form?

At audit, the provider asks: can the organization inspect access, misuse, exceptions, and policy compliance without turning audit logs into surveillance?

For ISLAMU Event, this matters for attendee information, organizer contact, registration data, payment-related data, moderation reports, and federation metadata. The current thesis supports privacy-by-design reasoning and implementation traceability, not proof of privacy outcomes.

## Slide 41 - Content Moderation Heuristics

### What to say

Moderation is not just content removal. It is governance.

The moderation lifecycle includes report, risk triage, review, decision, reason, appeal, and audit.

For a Muslim community event platform, moderation can involve scams, impersonation, fake charities, misleading religious claims, unsafe events, inappropriate content, abusive organizers, or conflicts between local communities.

I-VSD asks for consistency, severity ranking, transparency, and appeal. It also asks the provider not to hide behind neutrality when the platform lends legitimacy to harmful listings.

But the thesis does not claim that fair moderation has been achieved. Fair moderation would require operational evidence, appeal data, stakeholder feedback, and perhaps community governance review. The case supports design reasoning and traceability.

## Slide 42 - AI and Algorithmic Heuristics

### What to say

AI and algorithmic systems introduce specific provider responsibilities.

If a system summarizes, ranks, recommends, moderates, translates, or answers questions, the provider must consider disclosure, uncertainty, source integrity, bias, autonomy, and escalation.

For religious or community contexts, this is especially sensitive. AI output can appear authoritative even when it is uncertain. A recommendation system can shape attention. A ranking system can favor certain organizations or content. A moderation model can amplify bias. A translation system can distort meaning.

The heuristic chain is: source, model, output, uncertainty label, human escalation.

The provider should disclose AI use and limits, preserve source integrity, review bias and disparate harm, evaluate source openness by risk, and protect user autonomy.

In ISLAMU Event, future AI use should begin with low-risk support such as search assistance, summarization drafts, moderation triage, translation drafts, or admin suggestions. It should not silently make high-impact moderation, billing, deletion, mass communication, or religious authority decisions.

Again, the thesis treats AI integration mostly as future design guidance, not completed validation.

## Slide 43 - Marketing and Communication Heuristics

### What to say

Marketing claims are design artifacts.

Users often encounter the product first through the landing page, pricing page, comparison page, documentation, changelog, roadmap, or social media. If these claims are exaggerated, vague, or unsupported, the provider can mislead users before they even touch the interface.

The heuristic is: claim, evidence, limitation, review owner.

If the provider claims """secure,""" what evidence supports it? If it claims """privacy-first,""" what architecture, policy, or audit supports that? If it claims """open source,""" can the system actually be built and self-hosted? If it claims """AI-powered,""" are the limits and risks disclosed? If it claims """GDPR-friendly""" or """enterprise-grade,""" is that a precise statement or an implied maturity claim without evidence?

Marketing should respect attention, communicate changes before trust is harmed, compete honestly, and explain who should not choose the product when relevant.

Unsupported claims become UI deception at a distance. They shape user decisions without adequate evidence.

## Slide 44 - Business Model Heuristics

### What to say

The business model is part of software design because it shapes what the provider will be pressured to optimize.

If revenue depends on surveillance, the product will be pressured toward more data extraction. If revenue depends on confusion, the product will be pressured toward unclear pricing. If revenue depends on addiction, the product will be pressured toward compulsive engagement. If revenue depends on lock-in, the product will be pressured against portability.

I-VSD asks providers to review funding, pricing, dependency, governance, monetization, and long-term stewardship.

It asks whether funding compromises the mission. It asks whether pricing and terms create excessive uncertainty. It asks whether monetization exploits religious guilt, user vulnerability, attention, or dependency. It asks whether commitments survive business changes.

Revenue is not rejected. The thesis is clear that infrastructure, salaries, support, security, accessibility, translation, and maintenance cost money. But money is treated as an accountable means, not the master metric.

The business model should not depend on confusion, surveillance, lock-in, addiction, religious guilt, or broken expectations.

## Slide 45 - Case-Study Boundary

### What to say

Now we move into ISLAMU Event.

Before discussing the case, the boundary must be repeated: Event is not proof. It is a worked application.

The case shows how I-VSD structures concrete design decisions. It does not prove that the framework works universally. It does not prove that users trust Event. It does not prove deployed outcomes. It does not prove security, privacy, accessibility, or fairness.

Because I am the founder and developer, positionality matters. The case is self-applied. That makes it transparent and detailed, but it also means independent validation is missing.

So the evidence level is implementation traceability and illustrative case reasoning.

## Slide 46 - ISLAMU ASBL Context

### What to say

ISLAMU ASBL is an emerging nonprofit context serving Muslim communities through software and related infrastructure.

The thesis frames ISLAMU with two maxims: **the vision is bigger than the organization**, and **the organization is bigger than the individual**. This matters because the software is not meant to become personal empire-building. The organization is meant to serve a mission beyond one person, and the mission itself is bigger than the organization.

The context includes a preference for free and open software where feasible, transparency, inspectability, and community stewardship. But the thesis does not claim that ISLAMU represents all Muslims. It does not claim that a nonprofit structure automatically produces ethics. Nonprofits can still fail, drift, communicate poorly, or mishandle trust.

The nonprofit context reduces certain pressures, such as investor growth demands, but it introduces other risks: funding fragility, slower development, operational burden, and dependency on trust.

This context explains why ISLAMU Event is a suitable illustrative case for I-VSD: it is a provider-mediated software project with explicit moral commitments, community stakeholders, and long-term governance concerns.

## Slide 47 - ISLAMU Event Overview

### What to say

ISLAMU Event is envisioned as community-owned event discovery infrastructure for Muslim communities.

The target users include attendees, mosques, charities, universities, organizers, community groups, and potentially federated or self-hosted instances.

The problem is that Muslim community events are often fragmented across posters, WhatsApp groups, social media, commercial platforms, and word of mouth. That creates discovery problems, trust problems, accessibility problems, and dependency on platforms that may optimize for advertising, engagement, or data extraction.

ISLAMU Event is not just a CRUD app for events. The ethical surfaces include curation, identity, privacy, payments, moderation, accessibility, federation, portability, anti-scam safeguards, and community governance.

The vision is to help Muslim communities socialize and learn through accessible, ethical, community-owned event discovery.

The claim is design direction and traceability, not that the full ecosystem is already mature or validated.

## Slide 48 - Ecosystem and Deployment Model

### What to say

The ecosystem model reduces centralization pressure, but it does not eliminate risk.

Self-hosting and open-source stewardship can help communities avoid total dependence on one provider. Federation can help communities interoperate without all control being centralized. Public code and documentation can support inspection and contribution.

But these features are not magic. Self-hosting can be hard. Federation can introduce moderation and interoperability complexity. Open source can still be unusable if documentation, deployment, and maintenance are poor. A protocol can reduce one kind of lock-in while adding new dependencies.

So the responsible claim is risk reduction, not completion. The design direction supports autonomy and portability, but reliability, moderation, abuse handling, long-term maintenance, and user experience require future evaluation.

## Slide 49 - Strategic Traceability Ledger

### What to say

The strategic traceability ledger shows how decisions connect to I-VSD concerns and remaining risks.

The first decision is the Islamic curation boundary. The official instance focuses on Islamic events within declared scope. This connects to trust, modesty, community expectations, and scope fairness. The open risk is how to avoid arbitrary exclusion, represent scope honestly, and handle contested cases.

The second decision is anti-scam and instance safety. This connects to non-harm and trust. The open risk is whether reporting, verification, abuse testing, and governance processes work in practice.

The third decision is transparent fees. This connects to truthfulness and avoiding uncertainty. The open risk is user comprehension: do users actually understand who receives what money and why?

The fourth decision is the privacy strategy. This connects to avoiding spying and trust. The open risk is privacy audit evidence and operational discipline.

The fifth decision is federation and portability. This connects to promise-keeping and justice. The open risk is interoperability evidence, migration usability, and ecosystem maturity.

This ledger is the case study in miniature: decision, principle concern, evidence, and remaining risk.

## Slide 50 - High-Level Technical Architecture

### What to say

The architecture slide shows how technical structure can support traceability.

The point is not to prove security or privacy. A diagram is not an audit. The point is that architecture choices can be connected to responsibilities.

For example, a browser-to-BFF-to-API boundary can limit token exposure. Authorization boundaries can separate user, organizer, tenant, and platform responsibilities. Persistence and storage choices affect data stewardship. Observability affects accountability and incident response. Self-hosting and deployment architecture affect autonomy and continuity.

The architecture can support inspectability, but stronger claims need tests, audits, deployment evidence, incident history, and external review.

## Slide 51 - Technical Stack by Responsibility Layer

### What to say

The technical stack is organized by responsibility layer.

The UI layer supports accessible and honest interaction. In the thesis, this includes Blazor and MudBlazor, but the exact technology is less important than the responsibility: make interaction understandable, accessible, and non-manipulative.

The BFF and API layer handle tokens, boundaries, and server-side mediation. This matters for security and privacy.

The application and domain layer handle business rules, CQRS-style separation, validation, and event logic. This is where provider promises become enforceable behavior.

The authorization layer uses identity and scoped authority concepts, including Keycloak and Cerbos/local authorization ideas. This matters because users, organizers, tenants, and platform administrators should not have confused or excessive authority.

The persistence and storage layer handles data stewardship, tenant filters, PII separation, retention, export, and backup.

The infrastructure layer handles observability, self-hosting, deployment, health checks, and operational continuity.

This is implementation traceability: connecting stack decisions to provider responsibilities.

## Slide 52 - Security and Privacy Trust Boundaries

### What to say

This slide shows trust boundaries, not proof.

Security and privacy depend on boundaries: browser, BFF, API, authorization, tenancy, persistence, storage, logs, and operational access.

I-VSD asks what is entrusted at each boundary and what could go wrong. Are tokens exposed? Can one tenant access another tenant""'s data? Are audit logs necessary and proportionate? Is sensitive data separated? Are permissions scoped? Are exports safe? Are uploads controlled? Are dependencies trusted?

The thesis supports the claim that these concerns are part of the design. It does not claim that a complete security audit has been performed.

So if asked whether Event is secure, the responsible answer is: the architecture includes security-oriented boundaries and traceable design decisions, but security requires testing, review, audits, deployment evidence, and ongoing maintenance.

## Slide 53 - Moderation, Verification, and Appeal Workflow

### What to say

Moderation and verification are governance workflows.

For Event, this includes verified organizations, unverified or user-reported events, reports, escalation, review, decisions, explanations, appeals, and auditability.

Verification labels should make uncertainty visible. They should not imply that unverified equals immoral or that verified equals perfect. They are trust signals with limits.

Moderation should be reviewable because the platform lends legitimacy. If fake charities, impersonation, scams, or harmful event listings appear, the provider cannot simply say """users posted it.""" The platform has responsibilities around reporting, triage, and response.

But again, the thesis does not claim fair moderation has been achieved. It shows the governance direction and traceability.

## Slide 54 - UX: Dark Pattern vs I-VSD-Aligned Interface

### What to say

This slide returns to the UI level using a concrete contrast.

The same product goal can be implemented manipulatively or transparently.

For example, if the goal is ticket purchase, a manipulative interface might hide fees until the end, preselect add-ons, make refusal visually weak, use guilt language, or make cancellation hard.

An I-VSD-aligned interface shows the price early, explains fees, avoids preselected paid options, allows refusal, separates donation from purchase, and does not exploit religious guilt.

For Event, transparent fee display is important because Muslim charities, mosques, and attendees may be sensitive to how money flows. If ISLAMU or a payment processor receives a share, users should be able to understand it.

This is not only usability. It is truthfulness, trust, avoiding deception, avoiding excessive uncertainty, and sincere counsel.

## Slide 55 - Accessibility and Localization

### What to say

Accessibility and localization are ethical quality concerns, not polish.

For a Muslim community platform, users may differ in language, age, ability, device quality, bandwidth, literacy, and technical confidence. Some users may need screen readers, keyboard navigation, high contrast, clear focus, text-to-speech, image descriptions, or right-to-left language support.

The thesis treats accessibility as part of excellence, justice, non-harm, and sincere service. An inaccessible product is not merely less pretty; it can exclude people from community events, religious learning, charity, and social connection.

The Event implementation includes traceability for language preference, RTL direction plumbing, focus and announcement services, skip links, main landmarks, live regions, component conventions, and selected tests.

But this is not WCAG certification. It is implementation traceability. Stronger claims require accessibility audits, user testing, affected-user feedback, and ongoing maintenance.

## Slide 56 - Business Model Against Enshittification

### What to say

This slide discusses enshittification risk: the pattern where platforms initially serve users, then business customers, then themselves, extracting more value as dependency grows.

I-VSD asks providers to design against this risk early.

For ISLAMU Event, risk-reduction choices include nonprofit structure, open-source orientation, self-hosting, federation, transparent funding, no conventional investor pressure, and attention to portability.

But these choices do not create immunity. A nonprofit can drift. Open source can become unusable. A project can become underfunded. Sponsors can create influence pressure. A future provider can change terms. Community governance can fail.

So the claim is risk reduction, not guarantee. The framework asks: what incentives and technical paths could trap users later, and how can the provider reduce those paths now?

## Slide 57 - ISLAMU Event Evidence Ledger

### What to say

The Event evidence ledger distinguishes traceable design from proven outcomes.

For privacy, there may be architectural decisions, PII separation, token boundaries, consent concepts, or export plans. That supports design reasoning and implementation traceability. It does not prove user trust or audit success.

For accessibility, there may be RTL support, focus services, landmarks, and tests. That supports traceability. It does not prove accessibility for affected users.

For moderation, there may be verification labels, scoped admin authority, reports, and escalation concepts. That supports governance design. It does not prove fair enforcement.

For federation, there may be ATProto/PDS groundwork and portability concepts. That supports direction. It does not prove ecosystem maturity.

This ledger prevents overclaiming. It says: here is what the evidence currently supports, and here is what future validation must still provide.

## Slide 58 - Main Thesis Contribution

### What to say

The main contribution is a reusable framework for morally accountable software provision.

I-VSD translates selected Islamic principles into provider responsibilities. It organizes those responsibilities across six domains. It provides seven heuristic families. It offers an explicit derivation protocol. It includes an evidence ladder and report contract. It applies the framework to ISLAMU Event. It also proposes an agentic skill and future governance formalization path.

The contribution is strongest as conceptual grounding, design reasoning, and implementation traceability.

It is not strongest as empirical validation, because that work remains future. It is not strongest as jurisprudential authority, because that requires scholars. It is not strongest as product certification, because audits and operational evidence are missing.

So the contribution is ambitious but bounded: a structured Islamic provider-responsibility framework for software design and traceability.

## Slide 59 - Current Claim Boundary

### What to say

This slide states the strongest responsible claim.

The thesis can claim that I-VSD provides a reusable provider-responsibility structure that guides design reasoning and implementation traceability in ISLAMU Event.

It cannot claim that I-VSD is empirically proven. It cannot claim universal validation. It cannot claim scholar certification. It cannot claim product certification. It cannot claim user outcomes. It cannot claim that Event is already secure, private, accessible, fair, trusted, or sustainable in deployment.

This boundary is not a weakness. It is part of the thesis contribution because ethical frameworks can become dangerous when they overstate evidence.

The phrase to remember is:

**Framework, not fatwa. Case, not proof. Traceability, not certification.**

## Slide 60 - Limitations

### What to say

The limitations are substantial and explicit.

First, the scope is Sunni and selected. The thesis does not represent all Islamic traditions, all scholars, or all possible principles.

Second, there has not yet been formal contemporary scholar review. That is needed, especially for finance, religious content, contested matters, AI authority, privacy, public harm, and future governance questions.

Third, the case is single and self-applied. I am both the thesis author and the founder/developer behind the Event case. That gives detailed access but creates positionality risk.

Fourth, empirical investigation is limited. There are no completed stakeholder interviews, surveys, longitudinal deployment studies, independent audits, or operational outcome measurements.

Fifth, there is no proof of user trust, user benefit, reduced harm, accessibility success, privacy success, security success, or moderation fairness.

These limitations define the future work. They also protect the current contribution from being overstated.

## Slide 61 - Anticipated Objections

### What to say

There are several likely objections.

The first is **religious imposition**. The response is that I-VSD is for providers who explicitly adopt Islamic principles. It is not a universal mandate imposed on all software. Many outcomes, like no deception and better privacy, may benefit non-Muslim users, but the framework is intentionally grounded in Islamic accountability.

The second is **which interpretation of Islam?** The response is that the thesis declares its Sunni scope, distinguishes broad principles from contested applications, and says contested issues require qualified review.

The third is **ethical constraints may be fatal competitively**. The response is that ethical choices can create costs and disadvantages, but that does not make unethical practices acceptable. The thesis does not promise worldly success. It argues for responsible means.

The fourth is **the framework is too abstract**. The response is that the matrix, derivation protocol, heuristic families, case application, and agentic skill reduce abstraction, though more tooling and training are needed.

The fifth is **why not use secular frameworks?** The response is that secular frameworks are useful but do not provide Islamic normativity or non-negotiable boundaries for Muslim providers. I-VSD complements rather than replaces them.

The sixth is **one case is not enough**. That objection is correct. One case is not validation. It is illustration and traceability.

The seventh is **software is neutral**. The response is that defaults, data collection, pricing, ranking, moderation, permissions, and business incentives encode values. Claiming neutrality often hides the values already present.

## Slide 62 - Evidence Boundary: Where We Are

### What to say

Where are we now?

The thesis supports conceptual grounding. It explains why provider responsibility matters and how selected Islamic principles can be relevant to software provision.

It supports design reasoning. It gives domains, heuristics, matrices, and derivation protocol.

It supports implementation traceability. ISLAMU Event shows how decisions can be traced to principles and domains.

It supports illustrative case evidence. The case demonstrates one worked application.

Where are we not yet?

We do not yet have practitioner review showing that other developers can apply the framework consistently. We do not yet have scholar review confirming the translation of principles. We do not yet have stakeholder interviews showing user experience. We do not yet have audits. We do not yet have deployment data. We do not yet have longitudinal evaluation.

This transparency strengthens the claim. It makes the thesis more credible because it says exactly where the evidence stops.

## Slide 63 - Future Validation Roadmap

### What to say

This roadmap is not validation already completed. It is a research agenda.

Future validation should include theological or scholarly review: are the selected principles appropriate, are the translations responsible, and where are the contested areas?

It should include practitioner review: can other developers, designers, product leads, or organizations use the framework consistently?

It should include stakeholder research: do users, organizers, and affected communities understand and experience the system as more trustworthy, fair, accessible, and respectful?

It should include operational audits: privacy audits, security audits, accessibility audits, moderation review, incident records, and deployment evidence.

It should include additional cases, including negative or mixed cases, not only favorable examples.

The roadmap turns current limitations into future research steps.

## Slide 64 - Future Evaluation of the Agentic Skill

### What to say

The `i-vsd` skill should also be evaluated in the future.

Important questions include: do different agents or practitioners use the same resources consistently? Does the skill route tasks correctly? Does it refuse or narrow when the task is outside scope? Does it preserve claim boundaries? Does it identify missing evidence? Does it produce useful reports? Does it overclaim?

The skill should be tested across examples, diffs, architecture decisions, marketing copy, privacy changes, AI features, and business model changes.

The evaluation should not ask whether the skill is a moral authority. It is not. The evaluation should ask whether it supports disciplined review.

## Slide 65 - Assay-Backed I-VSD Governance Gate

### What to say

The Assay-backed governance gate is a future direction for combining agentic review with deterministic enforcement.

The idea is that an agent can review a change and classify findings: hard violations, soft warnings, missing evidence, escalation needs, and claim boundaries.

Then a separate policy layer applies declared thresholds. For example, any critical issue might block a release. Repeated warnings might accumulate into governance debt. Missing evidence might require review before deployment.

This does not automate Islamic moral judgment. It enforces declared categories and thresholds while preserving evidence.

The gate would say: against this declared policy, this change passed or failed. It would not say: this product is Islamically certified.

## Slide 66 - Hard and Soft Violation Thresholds

### What to say

The distinction between hard and soft violations is important.

A hard violation might be hidden telemetry, deceptive pricing, removal of export without justification, a security backdoor, privacy-invasive permissions, or a dark-pattern consent flow. These can block because they directly violate core responsibilities.

A soft warning might be ambiguous documentation, incomplete evidence, unclear communication, missing accessibility follow-up, or a weakened governance baseline. A single warning may not block, but warnings are not harmless. Repeated warnings can become governance debt.

This mirrors real engineering practice. Not every warning fails a build, but unresolved warnings can indicate quality decay. In I-VSD, unresolved ethical warnings can indicate responsibility decay.

## Slide 67 - Local-to-CI Lifecycle Enforcement

### What to say

This slide connects ethical traceability to the existing software lifecycle.

Developers already use local checks, tests, builds, scans, CI pipelines, protected branches, and deployment gates. The future I-VSD governance direction asks whether ethical review can become part of that lifecycle.

For example, a local pre-commit check might warn about changed privacy copy. A pull request check might require an I-VSD report when data collection changes. A deployment gate might block if a critical dark-pattern finding is unresolved.

The point is not to bureaucratize every change. The point is to prevent serious moral changes from bypassing review simply because they appear as ordinary code, configuration, or copy changes.

## Slide 68 - Evidence Bundle and Audit Trail

### What to say

The evidence bundle is an archive of the decision path.

It might include the changed files, the review report, relevant policies, screenshots, tests, logs, missing evidence notes, escalation decisions, and final claim boundary.

It is not a certificate. It is not proof of moral correctness. But it makes future inspection possible.

If a decision is challenged later, the provider can show what was considered, what evidence existed, what was missing, who reviewed it, and why a decision was made. That supports accountability.

## Slide 69 - Future Research Comparison Matrix

### What to say

The future comparison matrix compares workflow capability, not moral superiority.

For example, one approach may provide better documentation, another better stakeholder research, another better technical enforcement, and another stronger policy integration.

An Assay-backed gate would be valuable because it connects review outputs to lifecycle enforcement. But that does not make it morally superior by itself. It only improves a particular workflow capability: making declared review thresholds auditable and enforceable.

This distinction matters because the thesis does not claim that tooling equals ethics. Tooling supports accountability. It does not replace moral judgment.

## Slide 70 - Answering the Main Research Question

### What to say

Now I answer the main research question directly.

Selected Islamic principles can be translated into provider-facing design responsibilities by moving through a structured path:

**Sources -> principles -> heuristics -> domains -> decisions -> evidence.**

The sources provide normative grounding. The principles identify moral responsibilities. The heuristics translate them into practical design questions. The six domains ensure the review covers strategy, design, technical architecture, operations, governance, and evaluation. The decisions show how the framework affects real software. The evidence level states what can responsibly be claimed.

In ISLAMU Event, this structure guides decisions about Islamic curation, anti-scam safeguards, transparent fees, privacy, self-hosting, federation, accessibility, moderation, technical boundaries, and stewardship.

The case shows that I-VSD can structure ethical design reasoning in one concrete software project. But it remains illustrative and self-applied. It does not validate the framework universally.

So the answer is: yes, selected Islamic principles can be translated into a reusable provider-responsibility framework, and ISLAMU Event shows one traceable application. Stronger claims require future validation.

## Slide 71 - Final Responsible Claim

### What to say

The final responsible claim is:

**Islamic Value-Sensitive Design provides a reusable provider-responsibility framework that structures design and implementation traceability for provider-mediated software. ISLAMU Event illustrates how the framework can guide one concrete case. Stronger claims require future empirical, operational, practitioner, and scholarly validation.**

This is the claim I can defend without overclaiming.

It is a framework, not a fatwa.

It is a case, not proof.

It is traceability, not certification.

If there is one sentence I want the examiners to remember, it is that. The thesis is ambitious because it tries to connect Islamic ethics, software design, provider responsibility, implementation traceability, and future governance. But it is bounded because it repeatedly states what it has not proven.

## Slide 72 - Hidden Examiner Support: Limits and Evidence Scope

### What to say

If I am pushed on proof, my answer is that Event is one worked traceability case, not generalization.

The case shows that the framework can structure decisions. It does not show that all users experience the system as trustworthy. It does not show that the framework works across sectors. It does not show that scholar review has validated the principle translation. It does not show that audits have passed.

Legal and platform compliance can help execution, but they are not moral sufficiency. A system can comply with a law and still be deceptive, exploitative, or misaligned with Islamic duties.

The evidence strength comes from source quality, method coherence, and implementation traceability. Remaining gaps include independent audit, user study, longitudinal deployment, wider controls, practitioner replication, and scholar review.

So the case evidence is directional and illustrative, not conclusive.

## Slide 73 - Hidden Practitioner Workflow

### What to say

The practitioner workflow is the practical form of the framework.

First, define the decision or system boundary. What is being reviewed? A feature, product, pricing page, data model, AI integration, architecture decision, or business model?

Second, identify stakeholders and entrusted goods. Who is affected, and what is entrusted: data, money, attention, religious trust, community legitimacy, access, or dependency?

Third, select relevant principles and domains. Not every principle is equally central in every case.

Fourth, derive provider questions and heuristics. What must the provider ask, disclose, protect, avoid, or review?

Fifth, classify evidence. Is the current support conceptual, design rationale, implementation traceability, audit evidence, stakeholder evidence, operational evidence, or future validation?

Sixth, document findings, missing evidence, tradeoffs, red lines, and escalation needs.

This workflow makes I-VSD usable without pretending that every practitioner becomes a scholar or auditor.

## Slide 74 - Thank You

### What to say

Thank you for listening.

The main reminders are:

I-VSD is a framework, not a fatwa.

ISLAMU Event is a case, not proof.

Implementation evidence is traceability, not certification.

The future validation path is identified, not completed.

I welcome your questions.

## Slide 75 - Hidden Likely Examiner Questions and Answers

### What to say

If asked whether this is a fatwa or Sharia certification, the answer is no. It is a provider-responsibility framework grounded in selected Islamic principles, and contested matters require qualified scholars.

If asked whether Event proves I-VSD, the answer is no. Event illustrates traceability in one self-applied case. It does not validate outcomes.

If asked why VSD is not enough, the answer is that VSD is useful for design sensitivity, but it does not provide selected Islamic non-negotiable boundaries for Muslim providers. I-VSD adds that normative layer while using compatible design methods.

If asked whether compliance is enough, the answer is no. Compliance can support accountability, but legal permission does not equal Islamic moral sufficiency.

If asked what the strongest evidence is, the answer is conceptual grounding, design reasoning, implementation traceability, and a worked case.

If asked what evidence is missing, the answer is scholar review, practitioner replication, stakeholder research, audits, deployment data, and longitudinal evaluation.

If asked whether the thesis is too ambitious, the answer is that it is ambitious but bounded. It does not claim final validation. It builds a framework and shows one traceable application, then names the work still required.
