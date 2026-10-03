# Aletheia: Digital Adoption 2026 - execution-gap evidence and design tests

[Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) · [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md)

**Status:** knowledge-only, source-attributed design research; not an implemented feature or independent confirmation of vendor impact.  
**Reviewed:** 2026-10-03. **Source period:** first-quarter 2026 research.  
**Primary supplied source:** WalkMe (an SAP company), *The State of Digital Adoption 2026: The AI Reality Check*, [42-page PDF](https://www.walkme.com/wp-content/uploads/2026/04/Soda-Report-2026.pdf).  
**Related existing source register:** [Aletheia AI Discovery Sources](aletheia-ai-discovery-sources.md), which **already mentioned this same WalkMe report before this review**.  
**Purpose:** preserve specific findings, limitations and testable improvements, without rebranding WalkMe's marketing as neutral proof, copying report illustrations or rebuilding Aletheia around a vendor product.

## Executive finding

**Aletheia already has most of the principles. The useful change is to operationalise them.** Assess complete user journeys, the context passed between tools, timely help, and evidence of completed work instead of counting features, agents or generated outputs. Prioritise a small, privacy-respecting workflow test over a new orchestration platform.

Do not say Aletheia is a truth machine. It is a source-aware, uncertainty-aware set of knowledge and workflow tools; the user retains control of consequential actions.

## Study design and interpretation boundary

- WalkMe commissioned online surveys of **3,750 people** at organisations with at least 1,000 employees: **1,700 senior leaders** and **2,050 office/hybrid workers**, across 14 countries in Q1 2026 (pp. 4, 41). Behavioural analytics from WalkMe's own platform across thousands of enterprise applications and **60+ organisations over 12 months** are a separate evidence stream (pp. 4, 11, 41).
- Survey answers describe reported perceptions and behaviours, not necessarily independently timed or causally established performance effects. The vendor sells digital adoption software: interpret especially its proposed solution and ROI comparisons in this commercial context (pp. 33-40).
- Percentages below are **WalkMe's reported sample findings**, not universal population rates, predictions for Aletheia users or controlled-test results. Exact denominators can vary by question. The report does not give enough underlying microdata here to independently reproduce or stratify all results.
- The survey geography includes **9% UK and Ireland combined** and **6% Built Environment/AEC** respondents, so neither group is independently well-characterised in the published charts (p. 41).
- The headline **51 workdays lost annually** extrapolates self-reported **7.9 hours/week** to a standard work year. Do not use it as observed leave-adjusted time loss (pp. 14-15, 42).
- The report's **$142m** annual digital-inefficiency illustration applies to **companies with 5,000+ staff**, combines estimated components and uses directional survey assumptions; it is **not** an expected saving for Aletheia or a generic employer (pp. 9, 42).
- The report's visibility-gap example compares executives' *estimated* app counts with platform-observed counts across a vendor sample. It is useful as a prompt to measure real workflows, **not** proof that all enterprises use 661 applications (pp. 11, 42).
- An in-flow-support **3.7x** training-relevance association is a comparison of survey response proportions (28% vs 7%), **not demonstrated causation** (p. 33).

## Evidence cards (source claims are deliberately separate from Aletheia proposals)

### DA-001 | Workflow interruption is an adoption defect
**WalkMe finding (pp. 12, 23):** Respondents report an average **2.88 applications per task**. **37%** report sometimes avoiding AI because switching to it disrupts their workflow or forces manual transfers. In more complex workflows spanning eight or more apps, the report shows greater task interruptions than in 1-3-app workflows.

**Aletheia design inference:** Evaluate full journeys from starting question to meaningful output; count repeated entry, lost task state and unnecessary navigation. Do not add a new screen merely to display that an AI exists.

**Test:** Begin a discovery task in one Aletheia app, open a related resource and return. Does the original query, location, task stage and evidence survive without a second entry? Mark any part requiring explicit handoff versus seamless continuity.

### DA-002 | Recoverable context, not unlimited memory
**WalkMe finding (pp. 20-22):** Only **12%** of workers in its survey say they are fully confident AI tools understand the context of their work. The report attributes friction to missing previous steps, applicable rules and workflow state.

**Aletheia design inference:** Define a minimal, portable **Task Context Packet**, never a hidden collection of all user data:

```json
{
  "schema": "aletheia.task-context.v0-proposal",
  "task_id": "user-generated-or-local-id",
  "purpose": "specific user goal",
  "stage": "draft|review|ready-for-human-action",
  "inputs": ["user-approved references or local paths"],
  "provenance": ["source URL, as-of date, evidence status"],
  "permissions": ["explicitly authorised actions"],
  "open_questions": ["what is still unknown"],
  "next_step": "one concrete action",
  "sensitivity": "public|private",
  "expires_at": "optional timestamp"
}
```

This is an **example for design**, not an existing schema or promise of secure synchronisation. Use explicit export/import or user-approved connectors; browsers cannot silently reach into other sites or accounts. Never include passwords, sensitive source text or employer/client files in a public knowledge repository.

**Test:** A resumed task presents its last source dates, unknowns and next step, without inventing missing history or silently upgrading permissions.

### DA-003 | Guidance at the point of difficulty
**WalkMe finding (pp. 14, 17, 32-33):** The report allocates a reported **3.69 hours/week** to missing guidance, **2.34** to cross-application fragmentation and **1.88** to AI lacking context. **38%** say they feel well trained; **46%** say they receive guidance while doing the work. Survey respondents with contextual help more often report useful training (the report's 3.7x comparison). These are **self-reports and associations**.

**Aletheia design inference:** A small **Help me continue** or **HI / Hint Ladder** action belongs next to the stalled step in Learn and suitable apps. Offer one step, then explanation, then optional deeper instruction; do not overwhelm the first screen.

**Test:** With an incomplete form or uncertain source, the person can recover *in context*, without a lengthy modal, a new account or losing their entered data.

### DA-004 | Trust means traceability and user control
**WalkMe finding (pp. 13, 22):** **55%** report trusting AI only for simple tasks; **9%** report sufficient trust for high-impact tasks. **40%** report inconsistent advice across tools.

**Aletheia design inference:** Follow the existing Aletheia provenance, date/freshness, contradiction, uncertainty, human approval and **ATTEMPTED / COMPLETED / VERIFIED** conventions. A polished answer is not a verified action.

**Test:** For one conflicting pair of sources, show date and provenance for each, what remains unsettled and the human next action. Never label a job vacancy/event/price as currently verified from an old extract.

### DA-005 | Shadow AI is a governance AND usability signal
**WalkMe finding (pp. 24-25):** **45%** of surveyed workers say they used unapproved AI tools in the past 30 days; **36%** report using such tools with company-, customer- or employee-confidential data. These are sensitive **self-reported responses**, not measurements of Aletheia usage. The report characterises much of the behaviour as an adoption gap but that does **not** remove confidentiality or compliance duties.

**Aletheia design inference:** Provide explicit safe routes for allowed tasks; refuse silent data transfers; label which connectors and external model services receive data; require consent and a separate human action for publication, submission or disclosure. Never interpret usability as an excuse to bypass corporate restrictions.

**Test:** A mock sensitive input stays local unless an authorised transfer is requested and approved; audit paths distinguish draft, send and publish.

### DA-006 | Leadership dashboards are not user reality
**WalkMe finding (p. 26):** **88%** of executives think employees have adequate tools, compared with **21%** of employees fully agreeing. The **67-percentage-point gap** concerns different survey groups and perceptions, not proof about a particular organisation.

**Aletheia design inference:** Aletheia Improve should include user-path testing and an anonymous/optional friction report, instead of inferring readiness from a deployed-feature inventory.

**Test:** Compare maintainer-assumed flows against observed task attempt results; record steps that actually fail, not imagined improvements.

### DA-007 | Support should be useful without being intrusive
**WalkMe finding (pp. 17, 31):** Respondents prioritise reliability and ease of use; **59%** call integration between AI and tools important; **56%** say the best AI tools work without adding steps and interruptions.

**Aletheia design inference:** Preserve existing simple interfaces and sensible search-first defaults. Provide quiet progressive disclosure; never make a visible widget or persistent assistant mandatory to perform the ordinary task.

**Test:** On mobile, one principal action, keyboard access, reduced motion and a usable no-AI fallback continue to work.

### DA-008 | Measure completed tasks rather than invented ROI
**WalkMe finding (pp. 8-10, 35, 42):** The report gives large directional budget/inefficiency and ROI estimates. Some costs depend on self-reported bands and estimated conversions.

**Aletheia design inference:** Avoid copying headline dollar claims into product promises. Run a small, repeatable task experiment and record **task completed? / steps / elapsed time / extra re-entry / correctness / source freshness / user-reported confusion**. Report sample sizes and failures. No invisible workplace surveillance or production telemetry by default.

**Test:** Repeat an identical scenario before and after a change, compare evidence with uncertainty, and keep a rollback option.

### DA-009 | Help can be AI-assisted without becoming a new vendor dependency
**WalkMe finding (p. 23):** **49%** of respondents say they have used AI to explain how to use other workplace software.

**Aletheia design inference:** The existing Learn commands and help cards could offer explanations drawn from maintained local documentation, then permit source-checking. Keep clear limits when an interface/version differs from the stored instructions.

**Test:** With the network disconnected, user can still read locally bundled guidance or sees an honest unavailable state. Live verification is never fabricated.

### DA-010 | Reuse before reinvention
**WalkMe thesis (pp. 30-39):** Enterprises should make existing AI and software work together before buying more. This is compatible with Aletheia's existing model-neutral, free-first design, but **WalkMe's proposed proprietary orchestration product is not an Aletheia requirement**.

**Aletheia design inference:** Do not clone the vendor DAP, add tracking scripts, require an enterprise subscription or design a giant orchestration layer in this pass. Improve one observed journey at a time.

**Test:** Reject a proposed feature unless it removes a verified pain point or adds a distinct, user-requested capability.

## Aletheia Improve candidate: ADOPT audit (proposal only)

**Input:** a working app, its canonical MD and page specification, plus a real or synthetic task.  
**Output:** a concise, source-backed audit with **KEEP / CHANGE / DEFER / REJECT** decisions and explicit owners.  
**Metrics:** task success, steps, resumability, re-entry, friction, permission clarity, evidence accuracy, mobile accessibility and failure recovery.

**Eight checks:**
1. **ADOPT-01:** Can the user finish a defined journey without repeatedly typing the same context?
2. **ADOPT-02:** Does the app preserve or explicitly export/import task state? Is its provenance intact?
3. **ADOPT-03:** Is one useful next step or hint offered at a point of failure?
4. **ADOPT-04:** Are private inputs and connector boundaries transparent and opt-in?
5. **ADOPT-05:** Are attempted, completed and verified actions visibly different?
6. **ADOPT-06:** Does mobile, keyboard, reduced-motion, offline/no-AI fallback still work?
7. **ADOPT-07:** Do source date, locality, claim quality and conflicting evidence survive handoff?
8. **ADOPT-08:** Is there a measurable benefit in one representative before/after task, without misleading ROI claims?

**One suggested pilot:** Aletheia Job Search: user specifies a place and skills, reads verified employer vacancy, opens an employment guidance card, then returns to the **same** result and filters. Use mocked vacancies first so no employer data, application or job submission is accidentally touched. Owner reviews changes before any HTML/app deployment.

**Other possible crosslinks, not implementation promises:** Learn Hint Ladder; Discover place/date context; Shopping lists and retailer preferences; Publisher source/approval receipts; MDL Renew exact-file diagnostic history.

## Priority and non-duplication decision

- **Already present:** evidence/provenance, human authority, model independence, AI discovery-source mention of WalkMe, knowledge Markdown, local/offline support, Hint Ladder idea, and Aletheia Improve.
- **Worth adding now:** specific evidence/methodology note, reusable ADOPT checks, a small task-context sketch, and a friction-focused pilot proposal.
- **Defer:** universal cross-app sync, new browser instrumentation, tracking, third-party digital-adoption platforms, new app/rebuild, paid subscriptions and publishing workflows.
- **Reject:** treating percentages as universal truths, publishing copied vendor charts/content, claiming tests passed because source was committed, or using cost-savings statistics as guarantees.

## Source receipt

WalkMe, *The State of Digital Adoption 2026: The AI Reality Check*, published 2026, supplied and reviewed 2026-10-03: https://www.walkme.com/wp-content/uploads/2026/04/Soda-Report-2026.pdf .

Reproducible page map: **4, 41-42** methodology/definitions; **8-11** budget, cost and visibility; **12-15** interruption/time; **17** user priorities; **20-26** context/trust/shadow AI/perception gap; **30-33** integration/training; **35-39** vendor recommendations. For copyright and provenance, this file provides independent condensation and Aletheia proposals rather than reproduced graphics or extensive passages.
