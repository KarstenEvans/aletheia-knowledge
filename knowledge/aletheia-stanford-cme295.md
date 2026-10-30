---
title: Stanford CME 295 — practical lessons for Aletheia
slug: aletheia-stanford-cme295
status: source-checked-knowledge-only
knowledge_type: course-source-review-and-original-learning-design
last_checked: 2026-10-30
source_class: original-Stanford-syllabus-and-instructors-cheatsheet-plus-LinkedIn-discovery
public_html: none
related_task: AK-103
---

# Stanford CME 295: Transformers & LLMs — what Aletheia can reuse

> **Aletheia Markdown • KNOWLEDGE REVIEW • originally 15 October, refreshed 30 October 2026.** This is Aletheia's independent educational/workflow analysis of a public course, **not** a copy of Stanford teaching materials, an endorsement, a new app or a change to the Aletheia Protocol.
>
> [Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) governs provenance, verified versus inferred claims, revisions and authority. [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md) informs optional accessible storytelling and humour without replacing evidence.
>
> **Discovery receipt:** [LinkedIn post shared by user](https://lnkd.in/p/e668zrGZ), Javeriya A., linking the **autumn 2025** nine-lecture Stanford CME 295 series. [Official course](https://cme295.stanford.edu/) • [official syllabus / recording and slide links](https://cme295.stanford.edu/syllabus/) • [2025 Stanford Online nine-video playlist](https://www.youtube.com/playlist?list=PLoROMvodv4rOCXd21gf0CF4xr35yINeOy) • [authors' multilingual cheatsheet repo](https://github.com/afshinea/stanford-cme-295-transformers-large-language-models).

## At a glance

**Finding:** Lectures 7 (retrieval, tools, agents) and 8 (evaluating LLM output) provide the strongest immediate ideas, especially for existing **Aletheia Improve**, source-based Knowledge and repeatable app tests. Lectures 3 and 6 help with prompt/context limits and task decomposition. Aletheia Smart Learn can offer its *own* free, bite-sized, nontechnical-to-technical pathway across all nine topics.

**Do not build:** a separate "Stanford app", separate provider-branded Aletheia AI apps, a compulsory RAG backend, a new agent router or an unapproved monitoring pipeline. Keep Markdown canonical and user-owned; tests may be carried out manually on any AI. An AI response saying "passed" is not independent verification.

**Access and evidence limits:** The 2025 lecture topics and durations were verified from the publicly indexed official course syllabus, plus the original author's cheatsheet repository. Public recordings and slide links are available. This review does **not** claim to have watched all nine recordings in full, replicated the Stanford exercises, completed the university course or inspected every page of every slide.

## Source and edition distinction

- **2025 (complete):** nine recorded lectures from 26 September to 5 December 2025; the official 2025 syllabus describes each topic and links slide sets/recordings. Stanford's course is intended for learners with calculus, linear algebra and basic ML experience. Our accessible track would be *new Aletheia teaching*, not a claim that Stanford's graduate course itself requires no prerequisites.
- **2026 (in progress on 15 October):** Afshine Amidi publicly announced a revised fall course including agents, memory, harness optimisation, post-training and diffusion LLMs. [Author announcement](https://www.linkedin.com/posts/afshineamidi_our-stanford-class-cme-295-transformers-activity-7510504260703264770-avUg) • [course site](https://cme295.stanford.edu/syllabus/). A scheduled, upcoming lecture or externally published pre-lecture commentary **is not a verified completed Stanford recording**. Verify lecture dates, updated slides and recording URLs from the live course page before incorporating new specifics.
- **Cheatsheet:** [Afshine and Shervine Amidi's repository](https://github.com/afshinea/stanford-cme-295-transformers-large-language-models) advertises Arabic, Czech, English, French, Serbian, Thai and other translations. [Its repository LICENSE](https://github.com/afshinea/stanford-cme-295-transformers-large-language-models/blob/main/LICENSE) states MIT, copyright © 2025 Afshine Amidi and Shervine Amidi. MIT's notice/attribution requirements apply if substantial licensed material is reused. **Do not infer** that separately hosted Stanford slides, videos, textbook or all third-party assets share that licence. Prefer original text, diagrams and examples with ordinary source links.

## 2025 lecture-to-Aletheia learning map

| # | Stanford 2025 syllabus topic | What Aletheia can teach in original language | Small independent exercise | Integration status |
| --- | --- | --- | --- | --- |
| 1 | Transformer: tokens, embeddings, attention, architecture | Why text is processed in pieces and why important context may be missed | Give a short paragraph; highlight which phrases are essential for an accurate answer | Proposed lesson only |
| 2 | Transformer models and optimisations, positional encoding, BERT | Why model architectures and context handling differ | Compare the same classification question with two candidate models, recording errors | Proposed lesson only |
| 3 | LLMs: context, sampling, prompts, in-context learning | Clear tasks, constraints, examples and what a response does not prove | Write a precise job-search request; compare with a vague request | Proposed prompt review only |
| 4 | Pretraining, quantisation, SFT, LoRA | Distinguish model training, adapting, prompting and local execution | Sort examples into 'prompt', 'retrieval' or 'fine-tuning'; justify each choice | Proposed lesson only |
| 5 | Preference tuning, RLHF, reward models, DPO | Why a pleasing answer can still be inaccurate | Check a confident explanation against its cited primary source | Proposed lesson only |
| 6 | Reasoning, reinforcement learning, scaling | Decompose real tasks while retaining evidence and stopping rules | Split an event-verification task into date, location, source and decision checks | Proposed Improve test only |
| 7 | Agentic LLMs: RAG, advanced retrieval, function calling, agents, ReAct | Evidence lookup when needed; tools are optional and permission-limited | Compare full-library paste with retrieval of just three relevant Markdown cards | **Priority research** |
| 8 | LLM evaluation: judges, best practices, biases | Explicit acceptance checks and human adjudication | Score three answers against verifiable facts; blind the evaluator to provider names | **First pilot** |
| 9 | Recap/current trends | Distinguish genuine technical change from a marketing slogan | Date-stamp one new claim and decide whether it changes user-facing advice | Proposed research habit |

The table is **Aletheia's proposed adaptation**, not a claim that Stanford teaches these exact exercises or endorses Aletheia.

## AK-CME-001 | Retrieve evidence when needed, not every file at once

### Summary
Keep the answerable knowledge in versioned Markdown. Use a small, question-relevant set of sources instead of pasting an entire knowledge library into every prompt. More context is not automatically better context.

**Status:** PROPOSED DESIGN INFERENCE • **Source inspiration:** 2025 lecture 7 on RAG, tools and agents • **Verified:** course topic exists; **not tested** against an Aletheia implementation.

### Minimal portable retrieval receipt

```yaml
request: "What is on in Niš next weekend?"
scope: "event dates, official organisers and venue"
retrieved:
  - file_or_url: "<actual canonical record or primary URL>"
    title: "<source title>"
    checked_at: "<date/time and local zone>"
    evidence_span: "<where in source>"
    status: "observed | reported | inferred"
unresolved:
  - "<missing event confirmation>"
permission: "read-only research"
result: "answer | needs-check | no-supported-result"
```

Optional semantic search, embeddings or hosted RAG may speed up retrieval later, but a file index and ordinary search remain valid. Never silently convert speculation to a source-backed fact.

## AK-CME-002 | Evaluation is a set of observations, not an AI's opinion

### Summary
Separate deterministic checks, primary-source verification, human usability tests and AI suggestions. Model-as-judge can be useful, but position bias, verbosity bias and self-favouring bias mean it cannot be its own final referee.

**Status:** ORIGINAL PROPOSED ACCEPTANCE FRAMEWORK • **Course grounding:** 2025 lecture 8 covers LLM-as-a-judge, benefits, biases and pitfalls.

### Small reusable Aletheia Improve scorecard

| Dimension | Pass criterion | Method | Failure handling |
| --- | --- | --- | --- |
| Task compliance | All explicit constraints fulfilled or clearly identified as unmet | Requirements checklist | FAIL / partial with explanation |
| Grounding | Material changing facts have dated, direct sources | Open original source and cross-check the cited detail | UNVERIFIED until checked |
| Freshness | Dates, location, time zones and source-check date are explicit where needed | Compare event/job/price to originating page | STALE / needs recheck |
| Accuracy | No substantive contradiction with authoritative evidence in sample | Human or rule-based spot checks | FAIL and record corrected claim |
| Access/permissions | No external action without authority; no private data exposed | Action log and permission review | STOP / escalate |
| Portability | Markdown survives copy, save and use in a different AI | Manual transfer test | FAIL with reproduction steps |
| User experience | Short useful answer, working primary links, mobile-readable output | Person tests with a real task | IMPROVE, record observed problem |
| Honesty | No invented tool call, citation, test result or claim of deployment | Compare report with actual tool receipts | FAIL |

**Result rule:** Return **PASS / PARTIAL / FAIL / NOT TESTED** for each applicable dimension. 'PASS' requires actual evidence. An attractive answer with zero checked claims is *NOT TESTED*, not a pass. Preserve sample size and known limitations; do not fabricate aggregate scores.

### Three pilot cases

1. **What's On:** A candidate event result with date/time/venue/organiser → check all details against the organiser or venue; identify when no confirmed date exists.
2. **Job Search:** A vacancy link → verify that the listing is live, role matches location/remote constraints, and application goes to the actual employer/platform.
3. **Rice Intelligence:** A quoted price → require market, product grade, currency/unit, period, source, and explicit observed-versus-forecast-versus-inference label.

Use a deliberately false control example, plus a correct and an incomplete example, to confirm that evaluation can distinguish all three. Do not send confidential user/work data to additional models without explicit approval.

## AK-CME-003 | Context and handover without dependence on one AI

### Summary
A portable, concise task-state Markdown record prevents the next AI from treating a completed stage as unfinished.

**Status:** PROPOSED SMALL IMPROVEMENT • **Sources:** Lecture 3 (context, prompts) and Lecture 6 (reasoning), plus Aletheia's existing handover rules.

```yaml
task_id: "<stable ID>"
goal: "<what the user requested>"
scope: "<what is in/out>"
sources_checked: ["<real links/files>"]
completed: ["<observed completed action>"]
pending: ["<next verification or decision>"]
uncertain: ["<unresolved issue>"]
permissions: "read only | suggested edits | approved edits"
acceptance: "<test and result>"
last_updated: "<date>"
```

Do **not** put supposed private reasoning, passwords or hidden AI state in a handover. Store decisions, sources, actions, outcomes, explicit uncertainties and next steps.

## AK-CME-004 | Free-first Smart Learn course (original Aletheia curriculum)

### Summary
Give learners a small, useful accomplishment before asking them to understand mathematics. These units are **inspired by topics**, not copied lecture slides or summaries of unwatched content.

- **Beginner (no prerequisites):** Nine 5–10 minute original lessons: tokens; attention; prompts; training versus lookup; confident error; reasoning/checking; agents/tools; evaluating answers; spotting hype. Each has one short real-life example and a one-question check.
- **Practical:** Nine corresponding exercises using free AI access or no AI at all; allow printed or offline Markdown. Prefer one-button 'Surprise Me' and simple progress stored in a user-owned file, if the existing Smart Learn design supports it.
- **Technical (opt in):** link the Stanford lecture/slides/cheatsheet; learners choosing the advanced track should know its mathematics/ML prerequisites. Explain optional embeddings, re-ranking, evaluation design, sampling and system trade-offs.
- **Accessibility:** plain UK English by default; optional Thai, Norwegian and other translations; text-first/mobile/low bandwidth; no subscription, account creation or grading gate required just to read the educational Markdown.
- **Portability:** include the Aletheia/Thalia links, lesson objective, original example, exercise, checking criteria, sources, date and 'HELP' prompt in any future course Markdown. A learner can paste it into a different AI, or use it without AI.

### Copyable course-entry prompt (AI-independent)

```text
You are helping me study an original Aletheia Smart Learn lesson inspired by
Stanford CME 295. Read this Markdown as the portable lesson source.
Start with: 1) Learn (beginner/practical/technical), 2) Surprise Me, 3) Help.
Ask at most one useful question at a time. Teach one small concept in plain
language, then one practical exercise. Give hints, not just a prewritten answer.
Distinguish Stanford original sources from Aletheia examples and original
explanations. Do not claim I watched or completed a Stanford lecture.
If you cannot visit a source, say so. Accept HELP at any stage. End with
a brief summary and an optional next lesson. Keep state portable in Markdown.
```

## 2026 refresh and adjacent free Stanford courses (30 October 2026)

**Verified from official course pages and original instructors' repositories, not from video watch-throughs.** The user-shared 29 October LinkedIn post `https://lnkd.in/p/eX_zusnq` links the **2025 course**; the 2026 CME 295 edition is in progress. Do not confuse announcement, syllabus, released slides and published recordings.

| Resource | Public link | Evidence / course status | Smallest Aletheia reuse |
| --- | --- | --- | --- |
| CME 295 2026 | [Official syllabus, slides, recordings as published](https://cme295.stanford.edu/syllabus/) | Autumn 2026 term, not all sessions released as of 30 Oct | Update AI Fluency original examples about tokens, context, agent tooling, evaluation |
| CME 295 complete 2025 series | [2025 public recording playlist](https://www.youtube.com/playlist?list=PLoROMvodv4rOCXd21gf0CF4xr35yINeOy) | Complete historical nine-lecture archive | Preserve reference, label 2025 |
| CME 295 2026 videos | [Current public playlist](https://www.youtube.com/playlist?list=PLakGfbKCei80) | Progressive publication; inspect per-lecture availability | Point to syllabus instead of claiming every lecture available |
| CME 295 authors' cheatsheets | [MIT-licensed reference repository](https://github.com/afshinea/stanford-cme-295-transformers-large-language-models) | Free; licence covers this repository, not separate university video/slides | Link from Learn resources, do not copy copyrighted Stanford teaching media |
| CS329Z Engineering AI Agents | [Public official course, readings and slides](https://cs329z.stanford.edu/) | 2026 course; some recordings/coursework may require Stanford access | Small agent-memory, MCP, retrieval and evaluation exercises using existing Aletheia Protocol |
| CME 296 Diffusion & Large Vision Models | [Official 2026 syllabus](https://cme296.stanford.edu/syllabus/) | Spring 2026 course; linked lectures/slides | Optional source for Aletheia image/video-generation education |
| CME 296 author's cheatsheet | [MIT-licensed reference repository](https://github.com/afshinea/stanford-cme-296-diffusion-large-vision-models) | Free original source notes | Resources first, no clone/course |
| Super Study Guide | [Official paid Leanpub book](https://leanpub.com/transformers-large-language-models) | Bookshop.org UK listing not verified; no claimed Bookshop affiliate | Optional books only; public free cheatsheet first |

### Findings that change an Aletheia decision

1. **Context management:** distinguish stable project Markdown memory, current task and fetched question-relevant evidence. Retrieval and compaction can omit crucial safety constraints; require traceable handover and reconciliation, not automatic blind summarisation.
2. **Agent action boundaries:** tool calling, MCP and multi-agent messages are not permissions. Read untrusted documents as data. Keep external write/send/publish subject to explicit human authorisation and canonical Protocol permissions.
3. **Evidence-based evaluation:** a correct but incomplete answer must be PARTIAL; a false claim must FAIL; no executed test is NOT TESTED. Use actual source receipts and a receiving-model A/B comparison before claiming the concise rubric improves performance.
4. **Practical AI Fluency:** integrate short original optional labs into existing modules 4, 6, 8, 9, not an additional 10+ lesson course. Public resource links go to `aletheia-learn-rsc.htm`.
5. **Media:** CME 296 helps explain diffusion and video models, but neither an accessible lecture nor a paper proves that Aletheia's own video generation is implemented.

### Resource UI and gifts

The owning [Aletheia Learn Resources](https://karstenevans.github.io/aletheia-app/aletheia-learn/aletheia-learn-rsc.htm) is the only public front door for Stanford links, optional paid books and gifts. Free sources precede purchases; link course and book titles directly, not duplicate buttons. Claude gift subscriptions can be redeemed globally; OpenAI wallet gift cards are US-only. Official terms: [Anthropic gifting](https://support.claude.com/en/articles/12938627-how-to-gift-a-claude-subscription), [OpenAI gift-card restrictions](https://help.openai.com/en/articles/20001491-buying-and-redeeming-openai-gift-cards), [separate limited-rollout ChatGPT gifting credits](https://help.openai.com/en/articles/20001417-gifting-credits-in-chatgpt).

**What has been implemented:** Aletheia Learn Resources has been updated and AI Fluency 0.2.2 adds these original optional teaching labs. **What has not:** no new Stanford video watch-through, cross-provider A/B evaluation result, deployed browser/mobile QA, new paid product, model-training backend, protocol change or official Stanford endorsement.

## Implementation order and acceptance

1. **Now:** retain this source-traced knowledge note; catalogue as *knowledge-only*; record follow-up tasks. No app code, new reader or runtime change.
2. **First pilot:** inspect the actual existing Aletheia Improve specification/code and make a 3-case **manual** evaluation sheet (one correct, one false, one incomplete), with source receipts. Record baseline, detected failures and human checks. No implementation without evidence of benefit.
3. **If pilot useful:** propose the smallest change to existing Improve instructions or acceptance tests, preserving AI-independent Markdown, existing pre-flight validation and current permissions.
4. **Updated 30 Oct:** the existing 0–9-module AI Fluency course now has small optional Stanford-inspired labs and a linked resources page. Do not create a second nine-lesson clone. Any additional Smart Learn path remains a separate, optional idea.
5. **2026 edition follow-up:** revisit official 2026 lecture slides and recordings only after release, especially scheduled 6 Nov agent lecture; do not treat pre-lecture commentary as an official recording.

## Licence, provenance and corrections

- Link to university syllabus/videos/slide files and author cheatsheets. **Do not copy** the lecture videos, slide decks, textbook or illustration library into Aletheia without checking their individual rights.
- MIT repository licence does not equal a blanket Stanford course-media licence. Substantial reuse of the MIT material requires preserving applicable copyright and licence text.
- Attribution: Stanford University CME 295; instructors Afshine Amidi and Shervine Amidi. This Aletheia note and exercises are original editorial work and are unaffiliated with Stanford.
- This assessment uses course *topic outlines* and official link destinations; it is not a hands-on review of complete lecture content. Refresh claims as the 2026 edition progresses.
- Source links, observed facts, Aletheia inferences and proposed tasks must remain distinguishable.

## Sources and related files

1. User shared: https://lnkd.in/p/e668zrGZ
2. Stanford CME 295 course: https://cme295.stanford.edu/
3. Official syllabus (2025 archive/index and changing 2026 content): https://cme295.stanford.edu/syllabus/
4. 2025 Stanford Online playlist: https://www.youtube.com/playlist?list=PLoROMvodv4rOCXd21gf0CF4xr35yINeOy
5. Amidi authors' MIT-licensed multilingual reference repository: https://github.com/afshinea/stanford-cme-295-transformers-large-language-models
6. Repository MIT licence: https://github.com/afshinea/stanford-cme-295-transformers-large-language-models/blob/main/LICENSE
7. 2026 author announcement: https://www.linkedin.com/posts/afshineamidi_our-stanford-class-cme-295-transformers-activity-7510504260703264770-avUg
8. Related local concepts: [Aletheia Knowledge README](../README.md), [Aletheia Knowledge tasks](../aletheia-knowledge-tasks.md), [Aletheia Knowledge ideas](../aletheia-knowledge-ideas.md).

**Review state (30 October 2026):** source-linked knowledge note refreshed; initial three-case synthetic evaluation fixture exists, real receiving-model A/B pilot remains unperformed; AI Fluency optional labs and Learn resource links have been committed, with live browser QA still pending. No GitHub Pages app, mobile browser check, model performance benchmark, source-media download or protocol change is claimed.
