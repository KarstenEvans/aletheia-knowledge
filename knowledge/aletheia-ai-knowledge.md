---
title: Aletheia AI Knowledge
slug: aletheia-ai-knowledge
version: 0.2.0
status: active
last_checked: 2026-09-24
knowledge_type: provider-neutral AI capability and workflow library
resource_url: https://karstenevans.github.io/aletheia-knowledge/app/aletheia-ai-knowledge.htm
---

# Aletheia AI Knowledge

A provider-neutral, source-traced knowledge library about useful AI capabilities, limitations, workflows and Aletheia integration patterns.

This collection deliberately separates four things that are often blurred together:

- **Provider fact:** what an official product currently says it can do.
- **Aletheia pattern:** a portable way of using that capability without becoming dependent on one provider.
- **Community field note:** a useful report or workflow from users that has not been promoted to provider fact.
- **Open question:** something worth testing before it becomes a recommendation.

Features change quickly. Every time-sensitive card has a checked date and source links. Community observations never outrank official documentation or a fresh test.

Discovery source register: `aletheia-ai-discovery-sources.md`. Supplied books/reports are used as topic/workflow maps rather than copied into the cards.

---

## AI-001 | What Aletheia AI Knowledge is for

### Summary
This library is the AI capability map for Aletheia. It stores the useful facts inside the cards so an Aletheia app can answer ordinary questions locally first, then use live search only to refresh information that may have changed.

**Type:** ALETHEIA ARCHITECTURE  
**Evidence:** PROJECT DESIGN  
**Last checked:** 2026-09-24

### Details
The aim is not to decide that one AI is "best". Different systems are useful for different jobs, and their products change too quickly for a permanent ranking.

A card should therefore answer five practical questions before sending a person elsewhere:

1. What can this feature actually do?
2. Who can currently use it?
3. What is it especially useful for?
4. What are its important limits or privacy boundaries?
5. How can Aletheia use the idea portably?

Live web search is an update layer, not the card itself. When a feature changes, the card should be refreshed from current primary documentation and retain enough provenance to explain why it changed.

### Sources
- https://github.com/KarstenEvans/aletheia-protocol
- https://karstenevans.github.io/aletheia-knowledge/

---

## AI-002 | Aletheia should remain independent of the AI provider

### Summary
Aletheia is most useful as the evidence, state and preference layer around an AI, not as a feature that depends on ChatGPT, Gemini, Claude, DeepSeek or any other single vendor continuing to exist in its present form.

**Type:** ALETHEIA ARCHITECTURE  
**Evidence:** PROJECT DESIGN  
**Last checked:** 2026-09-24

### Details
Provider-native memory, projects and agents are valuable, but they are not the canonical Aletheia record.

The portable pattern is:

- **Aletheia Protocol:** provenance, correction, conflicts, evidence gaps, decisions and user authority.
- **Aletheia memory/profile:** only the user-approved preferences and facts needed for the current class of task.
- **Provider adapter:** a small ChatGPT, Gemini, Claude, DeepSeek or other instruction layer.
- **Checkpoint/handover:** portable Markdown that can move the active project to another AI.
- **Receipts:** a concise record of consequential actions or changes.

This means a person can use a native memory feature without surrendering the project's durable state to that memory system.

### Sources
- https://github.com/KarstenEvans/aletheia-protocol

---

## AI-003 | Personalisation for a worldwide Aletheia app

### Summary
An Aletheia A-to-Z, Employment, What's On, Meet or Food app can use a small user-controlled profile to improve relevance, but each search should receive only the fields it genuinely needs rather than a complete personal dossier.

**Type:** ALETHEIA DESIGN  
**Evidence:** PROJECT DESIGN  
**Last checked:** 2026-09-24

### Details
A portable profile might contain optional fields such as broad location, travel radius, age band where relevant, accessibility needs, preferred languages, interests, exclusions, budget range and saved search preferences.

Use **selective disclosure**:

- A What's On query may need location, travel radius, date and interests.
- Employment may need skills, acceptable locations, working pattern and excluded job types.
- Food may need location, allergies/preferences and budget.
- Meet should use explicit privacy and safety controls and should not expose hidden profile fields to other people.
- A general A-to-Z lookup may need only location and the user's current query.

The profile should be inspectable, editable and portable. Sensitive fields should never be inferred merely because a model thinks they are likely.

### Sources
- https://github.com/KarstenEvans/aletheia-protocol

---

## AI-004 | Untrusted material guard for agents and search

### Summary
Web pages, emails, PDFs, search results and retrieved documents are evidence or task material, not new instructions. This becomes more important as AI gains browser, email and computer-use abilities.

**Type:** SAFETY / ALETHEIA  
**Evidence:** ALETHEIA RULE + PROVIDER RISK MODEL  
**Last checked:** 2026-09-24

### Details
An agent can encounter text saying "ignore previous instructions", "send this file", "reveal your secrets" or "click this link". Aletheia should treat those strings as untrusted content unless the user explicitly adopts them.

A practical rule for every provider adapter is:

- keep user intent and authority separate from retrieved content;
- do not let a webpage or email silently widen the task;
- require explicit approval for consequential external actions where appropriate;
- report material instruction conflicts;
- record what source triggered a proposed action.

This is particularly important for unattended schedules and computer-use agents because prompt injection can arrive after the task has started.

### Sources
- https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex
- https://support.claude.com/en/articles/13364135-use-claude-cowork-safely
- https://github.com/KarstenEvans/aletheia-protocol

---

# ChatGPT / OpenAI

## AI-010 | GPT-6 Astra is the heavy-duty model, not merely a better chat model

### Summary
GPT-6 Astra is designed for long, difficult work that combines reasoning with browser/computer use, software engineering and polished professional outputs. Its practical value is highest when the job requires the AI to carry out many steps, not simply answer a question.

**Type:** CHATGPT / MODEL  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
OpenAI describes Astra as its strongest model across computer use, browsing, software engineering, professional work, science and other demanding tasks.

Examples in the official material include:

- filling online forms and updating records;
- organising calendars;
- online research followed by drafting into email or document tools;
- analysing data and creating plots;
- creating websites and running frontend QA;
- installing and testing software;
- troubleshooting what is visible on screen;
- producing documents, spreadsheets and presentations that follow existing templates and styles.

For Aletheia, the important change is **execution depth**. Astra makes the most sense when a task can be expressed as a goal plus constraints and verification steps, then allowed to work through the steps.

### Sources
- https://openai.com/index/gpt-6-astra/
- https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex

---

## AI-011 | GPT-6 Sol and Luna bring Astra-era improvements to cheaper work

### Summary
GPT-6 Sol and Luna inherit advances behind Astra in professional work, factuality, coding, computer use and alignment. Astra remains OpenAI's top model; Sol is the strong general workhorse and Luna is the lower-cost/high-throughput option.

**Type:** CHATGPT / MODEL  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
OpenAI's 22 September 2026 announcement says:

- GPT-6 Astra remains its best model "across the board".
- GPT-6 Sol and Luna use similar training methods to distribute many Astra advances at lower cost.
- API pricing fell by 50% versus GPT-5.6 promotional pricing: Sol to $2 input / $10 output per million tokens; Luna to $0.10 input / $0.50 output.
- GPT-6 prompt caching gives a 90% discount on cached input-token reads, which is useful for agents and long conversations that reuse a stable Aletheia bootstrap or reference corpus.
- Sol is intended to provide more room to iterate on difficult work; Luna makes repetitive or high-volume work cheaper.

Aletheia should not hard-code one model as permanent default. Route by task: inexpensive extraction/classification to the economical model, difficult synthesis or consequential multi-step work to the stronger model.

### Sources
- https://openai.com/index/introducing-gpt-6-sol-and-luna/

---

## AI-012 | Chat, Work and Codex are three different ChatGPT jobs

### Summary
The biggest paid-feature trap is treating every request as ordinary Chat. Current ChatGPT separates conversational Chat, multi-step **Work**, and software-focused **Codex**. For Aletheia development, Work and Codex may be more valuable than changing the chat model picker.

**Type:** CHATGPT / WORKFLOW  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
OpenAI currently describes:

- **Chat:** fast everyday conversation and assistance.
- **Work:** an agent for longer multi-step work and finished deliverables.
- **Codex:** software-development and technical work.

Current plan information says Plus includes GPT-6 Astra in Work and Codex, although its Astra allowance is limited and can be consumed faster than GPT-5.6 Sol. GPT-6 Pro powered by Astra in ordinary Chat is listed for higher plans.

For an Aletheia repository job, a good division is:

- ask Chat to discuss architecture or make a decision;
- give Work a multi-file research/build task with a finished output;
- give Codex a repository change that must inspect code, edit files, run checks and report the diff.

### Sources
- https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex

---

## AI-013 | ChatGPT Work is an agent that can finish multi-step jobs

### Summary
Work is the closest current ChatGPT feature to "hand this job over and bring back the completed result". It can use a cloud browser/computer, connected apps and files for longer workflows rather than stopping at instructions.

**Type:** CHATGPT / AGENT  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
Good Aletheia uses include:

- audit a site, follow links, collect evidence, edit a report and return the finished artifact;
- inspect a GitHub project plus supporting files and reconcile a change;
- research a topic from multiple live sources, then update the relevant knowledge cards;
- operate a web interface where an API or direct connector is unavailable;
- produce a document, spreadsheet or presentation rather than merely describing one.

The Aletheia handoff should give Work: goal, source of truth, constraints, approval boundary, required output, tests and receipt format.

Work should not be given blanket authority merely because it can click. Consequential actions should retain a human approval boundary.

### Sources
- https://openai.com/index/gpt-6-astra/
- https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex

---

## AI-014 | Codex with Astra is ChatGPT's direct answer to the Claude Code-shaped problem

### Summary
For repository work, Codex is the ChatGPT feature to compare with Claude Code. Astra is available in Codex on eligible paid plans and is specifically trained for software engineering, codebase understanding, execution and verification.

**Type:** CHATGPT / CODING  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
A useful Aletheia Codex task is not "write me some HTML". It is closer to:

1. read the repository instructions and current files;
2. understand the existing app and data format;
3. make the smallest safe change;
4. run syntax/tests or browser checks;
5. inspect the diff;
6. update project documentation;
7. produce a receipt with files changed and checks performed.

This is the same family of workflow that makes Claude Code attractive. The important question is therefore not whether ChatGPT can emit code in a chat box, but whether the repository has good durable instructions and a testable task boundary.

### Sources
- https://openai.com/index/gpt-6-astra/
- https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex

---

## AI-015 | AGENTS.md can make Aletheia rules native to Codex repository work

### Summary
Codex reads AGENTS.md repository instructions. A small root AGENTS.md can point Codex at the current Aletheia GUI, code, task and protocol files so new coding sessions inherit the project's rules without relying on old chat memory.

**Type:** CHATGPT / CODEX / ALETHEIA  
**Evidence:** OFFICIAL OPENAI CODEX GUIDANCE  
**Last checked:** 2026-09-24

### Details
OpenAI's Codex guidance treats AGENTS.md as durable repository guidance and notes that more specific nested instructions can apply in subdirectories.

For Aletheia Knowledge, a future root AGENTS.md could say, in essence:

- read README.md, aletheia-knowledge-GUI.md, aletheia-knowledge-code.md and aletheia-knowledge-tasks.md before editing;
- canonical facts live in knowledge Markdown;
- read the current page spec and implementation;
- preserve working behaviour;
- search/check changing facts;
- do not overwrite newer concurrent work;
- run relevant tests before claiming completion;
- append a concise task receipt.

This is not a replacement for the canonical guides. It is a short **router to them**, which keeps one source of truth.

### Sources
- https://github.com/openai/codex
- https://developers.openai.com/codex/guides/agents-md/

---

## AI-016 | Astra is sensitive to repo instructions, skills and effort settings

### Summary
Astra follows project instructions strongly. That is an advantage when the repository rules are good and a liability when old or contradictory instruction files remain accessible. Audit the instruction layer before judging the model.

**Type:** CHATGPT / CODEX  
**Evidence:** OFFICIAL OPENAI GUIDANCE  
**Last checked:** 2026-09-24

### Details
Current Astra prompting guidance emphasises:

- make instruction priority clear;
- inspect relevant skills and AGENTS.md files;
- tell the model when you want it to continue autonomously rather than pause for non-blocking questions;
- specify the desired writing style;
- specify how much testing or verification the task warrants;
- state when subagents should or should not be used.

Aletheia can turn this sensitivity into an advantage by keeping concise routing instructions and detailed canonical rules in separate Markdown files.

### Sources
- https://github.com/openai/codex/blob/main/docs/prompting.md
- https://developers.openai.com/codex/guides/agents-md/

---

## AI-017 | Connected apps and plugins turn ChatGPT into a workspace

### Summary
ChatGPT connected apps can provide live information from external services and, where supported, take actions. Plugins can package reusable instructions, skills and connected-app capabilities. They are most useful when a recurring Aletheia workflow touches the same service repeatedly.

**Type:** CHATGPT / PLUGINS  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
Depending on the app and permissions, ChatGPT can:

- search and reference connected information;
- use connected sources in deep research;
- interact with in-chat documents, maps or other experiences;
- create or update external information;
- use supported app events to trigger Work tasks.

Aletheia should keep connection authority explicit. A plugin being installed does not mean every task should use it, and an action-capable connector should not silently send, delete or publish material.

### Sources
- https://help.openai.com/en/articles/11487775-connected-apps-in-chatgpt
- https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex

---

## AI-018 | Gmail can be a real ChatGPT action surface

### Summary
With the Gmail connection enabled, ChatGPT can work with the authorised mailbox for tasks such as finding threads, summarising messages, drafting replies and supported message actions. Work can also react to new Gmail messages through event-triggered tasks.

**Type:** CHATGPT / EMAIL  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
Useful Aletheia patterns include:

- "Find the email thread about this project and give me the decision trail."
- "Draft a reply using this project's tone and facts, but do not send it."
- "When a new message with this subject arrives, summarise it and tell me whether action is needed."
- "Prepare a reply only when the incoming message matches these conditions."

The mailbox remains governed by the connected Google account's permissions. Actions that require approval can pause rather than execute invisibly.

For a personal Aletheia workflow, connect only the mailbox the user intentionally chooses and keep private mailbox data out of portable public knowledge files.

### Sources
- https://help.openai.com/en/articles/10408842-google-app-data-controls-faq
- https://help.openai.com/en/articles/10291617-tasks-in-chatgpt

---

## AI-019 | GitHub connection can support both repo work and event-triggered review

### Summary
ChatGPT can retrieve content from authorised GitHub repositories on demand, while eligible Work tasks can react to pull-request activity. This creates a useful Aletheia loop: repo change arrives, AI checks it against project rules, human receives a concise review.

**Type:** CHATGPT / GITHUB  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
GitHub access is permission-scoped. Current OpenAI documentation says ChatGPT retrieves permitted repository content on demand rather than maintaining a general synced index of every repository.

Event-triggered Work tasks can respond to supported pull-request events such as opening, review activity, commit updates, merges or closure, depending on the event.

Possible Aletheia uses:

- check whether a PR changes canonical knowledge without updating its page spec;
- detect a broken source or missing task receipt;
- review a code change against Aletheia GUI rules;
- summarise the change and flag conflicts, without automatically merging it.

### Sources
- https://help.openai.com/en/articles/11145903-connecting-github-to-chatgpt
- https://help.openai.com/en/articles/10291617-tasks-in-chatgpt

---

## AI-020 | Scheduled tasks can run reminders, recurring research and monitoring

### Summary
ChatGPT can run one-time or recurring tasks and monitor for changes. This is useful for Aletheia jobs such as vacancy scans, periodic site checks and "tell me only when this changes" watches.

**Type:** CHATGPT / AUTOMATION  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
Scheduled tasks can perform recurring work and send notifications. Current guidance says supported tasks can use connected apps when available.

Good Aletheia automation design includes:

- a clear cadence or condition;
- a source scope;
- a "do not notify me if nothing meaningful changed" rule when appropriate;
- a receipt stating what was checked and when;
- a review boundary before consequential external actions.

Important limitation: a task created inside a ChatGPT Project cannot currently access uploaded files or files stored in that Project. Put required stable instructions into the task itself or a supported connected source instead of assuming Project files follow the schedule.

### Sources
- https://help.openai.com/en/articles/10291617-tasks-in-chatgpt

---

## AI-021 | Event-triggered tasks can react to Gmail, Slack and GitHub

### Summary
Eligible ChatGPT users can create Work tasks that run when a supported external event occurs, rather than polling on a clock. Current supported examples include new Gmail messages, Slack channel messages and GitHub pull-request activity.

**Type:** CHATGPT / AUTOMATION  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
This is particularly useful for an Aletheia receipt model:

    event -> condition -> Aletheia instructions -> Work action/review -> receipt -> human

Examples:

- a particular sender emails -> summarise and prepare a draft;
- a PR opens -> check it against AGENTS.md and the task register;
- a Slack message mentions a project -> collect context and create an attention summary.

The trigger does not transfer additional permissions. It uses the account and repositories/channels/mailbox already authorised, and an action that needs approval can pause.

### Sources
- https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex
- https://help.openai.com/en/articles/10291617-tasks-in-chatgpt

---

## AI-022 | ChatGPT Sites are useful for prototypes, not a substitute for Aletheia's source-controlled site

### Summary
OpenAI's site-building capability can quickly create and host web experiences from prompts, but Aletheia's public library benefits from remaining GitHub/Markdown-first because its data, standards, history and portability matter more than instant generation.

**Type:** CHATGPT / SITES  
**Evidence:** OFFICIAL OPENAI + ALETHEIA DESIGN  
**Last checked:** 2026-09-24

### Details
Sites are useful for:

- trying a new layout;
- creating a one-off demonstrator;
- testing a user journey;
- rapidly prototyping a small app.

For the worldwide Aletheia concept, the stronger foundation is:

- GitHub as inspectable source control;
- canonical Markdown knowledge;
- explicit manifests;
- small HTML apps that can work without an AI;
- optional AI for discovery, synthesis and updating.

A generated site becomes much more useful when it is made to follow the Aletheia GUI/app-development Markdown rather than inventing its own design system each time.

### Sources
- https://openai.com/index/gpt-6-astra/
- https://karstenevans.github.io/aletheia-knowledge/

---

## AI-023 | ChatGPT can create and edit images directly

### Summary
Image generation and image editing remain native ChatGPT capabilities. They are suitable for app artwork, story illustrations, explanatory visuals, mock-ups and transformations of user-supplied images.

**Type:** CHATGPT / MEDIA  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
For Aletheia projects, keep the useful distinction between:

- **content image:** illustration or story art intended for the visitor;
- **interface asset:** icon/background/UI artwork;
- **evidence image:** screenshot or source image that must not be "improved" in a way that changes the evidence.

Store prompts or art-direction notes when consistency matters across a story or app.

### Sources
- https://openai.com/index/sora/
- https://openai.com/index/gpt-6-astra/

---

## AI-024 | OpenAI's native Sora video product has been discontinued

### Summary
Do not tell current ChatGPT users that their subscription includes Sora text-to-video. The Sora web/app experiences ended on 26 April 2026, and OpenAI says the Sora API is discontinued on 24 September 2026.

**Type:** CHATGPT / VIDEO  
**Evidence:** OFFICIAL OPENAI  
**Last checked:** 2026-09-24

### Details
This is a good example of why Aletheia AI Knowledge needs dates. Older articles and tutorials still describe Sora as a Plus/Pro benefit, but that is no longer a current product fact.

Video can still be brought into a ChatGPT workflow through third-party connected apps where available. Current plugin discovery includes services such as Runway, OpenArt, HeyGen, Descript and Adobe with various generation/editing capabilities.

That does not make those services part of the ChatGPT subscription; their own account, plan, credits and terms may apply.

### Sources
- https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation
- https://openai.com/index/sora/

---

## AI-025 | Astra usage should be spent where its extra depth matters

### Summary
Astra can consume a paid allowance faster than Sol. A practical workflow is to use Astra for hard multi-step, codebase, browser/computer or verification-heavy work and use Sol/Luna for ordinary iteration, extraction and repeatable low-risk tasks.

**Type:** CHATGPT / COST  
**Evidence:** OFFICIAL OPENAI + COMMUNITY FIELD NOTE  
**Last checked:** 2026-09-24

### Details
Official OpenAI guidance says Astra uses the plan's Work/Codex allowance and can consume it faster than GPT-5.6 Sol depending on input/output size, task and reasoning settings.

Community reports broadly reinforce the common-sense version of this: large codebases and high-effort agent runs can burn through allowance quickly, while lower effort can be a good balance for many jobs. These reports are anecdotal and should not be treated as plan guarantees.

Aletheia routing rule:

- default to the cheapest model that can reliably perform the task;
- escalate when the task fails a check or genuinely needs deeper reasoning;
- spend Astra on hard execution and verification rather than simple formatting.

### Sources
- https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex
- https://www.reddit.com/r/ChatGPT/
- https://www.reddit.com/r/OpenAI/

---

## AI-026 | Community tip: use a strong agent to supervise another coding agent, but verify the handoff

### Summary
A useful community pattern is "agent supervises agent": one system drives or reviews another coding environment, checking diffs and tests. It is promising for Aletheia orchestration but remains a workflow experiment, not an official reliability guarantee.

**Type:** COMMUNITY FIELD NOTE  
**Evidence:** ANECDOTAL  
**Last checked:** 2026-09-24

### Details
Users have reported using strong browser/computer agents to supervise coding tools, review their progress, inspect GitHub changes and request corrections.

The Aletheia version should be stricter:

1. define which agent owns the task;
2. define which tool is allowed to mutate the repository;
3. require tests/diff inspection;
4. keep a receipt of which agent proposed and which agent executed;
5. let the human approve consequential publication or merge steps.

Multiple agents do not automatically create higher truth. They can also amplify the same bad assumption.

### Sources
- https://www.reddit.com/r/ChatGPT/
- https://www.reddit.com/r/ClaudeAI/
- https://github.com/openai/codex

---


## AI-027 | Plus Astra allowance makes Work and Codex a scarce resource

### Summary
On ChatGPT Plus, Astra in Work and Codex is explicitly a **limited** allowance, and Astra can consume that allowance faster than Sol. A long agent job can therefore stop before the underlying project is finished even when ordinary Chat remains available.

**Type:** CHATGPT / LIMITS / WORKFLOW  
**Evidence:** OFFICIAL OPENAI + USER FIELD EXPERIENCE  
**Last checked:** 2026-09-24

### Details
OpenAI's current usage guide confirms the practical limitation: Work and Codex share one plan allowance. Depending on plan, both a five-hour window and a weekly limit can apply, and a user can exhaust the five-hour allowance before five clock-hours have passed.

For Plus, OpenAI currently gives an **estimated** Astra range of roughly **5–45 local messages per five-hour period**, not a fixed quota. Sol's corresponding estimate is higher. Actual consumption varies with task size, input/output, reasoning level, Fast mode and multi-step work. Astra can therefore be an awkward foundation for a business workflow that assumes one long uninterrupted agent run.

Aletheia should therefore design long jobs so they survive an exhausted allowance:

- break work into independently useful stages;
- make the agent save progress into the repository or a checkpoint early;
- make every stage start by reading current files rather than replaying the whole history;
- avoid using Astra for work Sol/ordinary Chat can do reliably;
- require a compact receipt before a long run is allowed to finish;
- keep the canonical state outside the agent session so a later run can continue rather than restart.

This is an engineering constraint, not a failure of the Aletheia idea. Agent capacity is part of the system design.

### Sources
- https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex
- https://help.openai.com/en/articles/20001516-managing-usage-with-gpt-6-astra-in-work-and-codex

---

## AI-028 | Codex is for repository engineering, not general website brainstorming

### Summary
Codex is most useful when the work has files, code, tests and a repository state that the agent can inspect and change. For quick design iteration or a small static page, ordinary Chat may be faster; for a multi-file refactor, migration, test/fix loop or repeated maintenance task, Codex is the better-shaped tool.

**Type:** CHATGPT / CODEX / WORKFLOW  
**Evidence:** OFFICIAL OPENAI + ALETHEIA DESIGN  
**Last checked:** 2026-09-24

### Details
Current Codex material describes end-to-end engineering work such as features, refactors, migrations, code review, CI/CD and scheduled maintenance. It supports worktrees, cloud environments and reusable Skills.

The useful Aletheia split is:

- **Chat:** discuss, design, research, review, make a small targeted edit through a connected repository tool.
- **Codex:** enter the repository, read `AGENTS.md`, inspect several files, edit, run commands/tests, examine failures and keep iterating.
- **Work:** jobs where browser/computer/app operation matters more than software engineering.

A static Aletheia app can still be built in Chat. Codex earns its keep when the task benefits from an actual engineering loop rather than simply producing source text.

### Sources
- https://openai.com/codex/
- https://developers.openai.com/learn/codex
- https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra

---

# Google Gemini

## AI-100 | Gemini Personal Intelligence combines several personal context sources

### Summary
Gemini's Personal Intelligence can personalise ordinary chats using memory of past Gemini chats, explicit Instructions for Gemini and selected connected Google information. Each component has its own eligibility and controls.

**Type:** GEMINI / PERSONALISATION  
**Evidence:** OFFICIAL GOOGLE  
**Last checked:** 2026-09-24

### Details
Current Google help says eligible personal-account users can obtain personalisation from:

- past Gemini chat memory;
- Instructions for Gemini;
- connected Google apps/content.

Past-chat Memory currently requires an adult personal Google account and Keep Activity on. Google says it is not available inside Gems or Live chats.

Aletheia should treat Gemini memory as a convenient context source, not a canonical ledger. Explicit corrections, source provenance and the portable Aletheia state file remain useful because provider memory is selective.

### Sources
- https://support.google.com/gemini/answer/16598623
- https://support.google.com/gemini/answer/16598469
- https://support.google.com/gemini/answer/16598625

---

## AI-101 | Gemini Gems need their own Aletheia instructions and knowledge

### Summary
A Gem is a repeatable customised Gemini with its own instructions and optional Knowledge files. Global Instructions for Gemini and ordinary past-chat Memory do not currently apply inside Gems, so an Aletheia Gem must carry its own bootstrap/state explicitly.

**Type:** GEMINI / GEMS / ALETHEIA  
**Evidence:** OFFICIAL GOOGLE  
**Last checked:** 2026-09-24

### Details
A useful project Gem can contain:

- a short Aletheia adapter in the Gem instructions;
- the project's canonical Aletheia state or handover;
- source documents under Knowledge;
- task-specific formatting/behaviour rules.

Google currently allows device or Drive files to be added as Gem Knowledge. Because ordinary Memory and global Instructions are unavailable in Gems, never claim that a Gem automatically "knows everything Gemini knows about me".

### Sources
- https://support.google.com/gemini/answer/15235603
- https://support.google.com/gemini/answer/15236405
- https://support.google.com/gemini/answer/16598469
- https://support.google.com/gemini/answer/16598625

---

## AI-102 | Gemini can personalise using selected Google services

### Summary
Eligible Gemini Personal Intelligence can use connected Google sources such as Workspace content, Contacts, Search/Maps/Shopping signals, YouTube history and, in supported places, Photos. This can make it powerful for personal retrieval, but it also makes selective disclosure and privacy controls important.

**Type:** GEMINI / CONNECTED APPS  
**Evidence:** OFFICIAL GOOGLE  
**Last checked:** 2026-09-24

### Details
Google's current help lists Google Workspace content including Gmail, Calendar and Drive among the services that can work with Personal Intelligence.

For Aletheia, the useful pattern is to keep provider-connected personal data where it belongs and pull only task-relevant conclusions into the portable state file.

Example: an Aletheia travel search may use a connected calendar to discover dates, but the resulting handover need contain only the agreed dates rather than a copy of the calendar.

### Sources
- https://support.google.com/gemini/answer/16598406
- https://support.google.com/gemini/answer/16598623

---

## AI-103 | Gemini Spark is Google's current agent-style task surface

### Summary
Gemini Spark can manage longer tasks/workflows and can use a remote browser/computer plus Personal Intelligence where eligible. It is the Gemini feature to watch when comparing ChatGPT Work or Claude's task mode.

**Type:** GEMINI / AGENT  
**Evidence:** OFFICIAL GOOGLE  
**Last checked:** 2026-09-24

### Details
Current Google help says Spark can use a remote browser, computer/code execution data and Personal Intelligence, including memory, instructions and connected Google apps.

An Aletheia Spark adapter should therefore concentrate on:

- task scope and authority;
- untrusted-material handling;
- explicit correction/provenance;
- finished-output requirements;
- a receipt/checkpoint after the run.

The exact feature availability can vary by account and rollout, so a live capability check belongs before any workflow that depends on it.

### Sources
- https://support.google.com/gemini/answer/17094507

---

## AI-104 | Aletheia's five-test Gemini trial remains a useful conformance check

### Summary
A provider adapter is useful only if behaviour improves in practice. The existing Aletheia Gemini trial tests correction handling, inference boundaries, conflict retrieval, freshness and portable handover.

**Type:** GEMINI / ALETHEIA TEST  
**Evidence:** ALETHEIA EXPERIMENT DESIGN  
**Last checked:** 2026-09-24

### Details
The five tests are:

1. **Correction:** explicitly change a fact; the old version must not remain current.
2. **Inference boundary:** a model-generated explanation must not later appear as user-stated fact.
3. **Conflict retrieval:** when two material sources disagree, the unresolved conflict must remain visible.
4. **Freshness:** a changing external fact should be rechecked when a decision depends on its current value.
5. **Handover:** a fresh AI should be able to continue from the portable Markdown without the original chat.

Record pass/partial/fail and distinguish platform limitations from adapter defects.

### Sources
- https://github.com/KarstenEvans/aletheia-protocol
- https://support.google.com/gemini/answer/16598623

---

# Claude / Anthropic

## AI-200 | Claude Code has a strong repository-instruction pattern through CLAUDE.md

### Summary
Claude Code automatically loads project memory/instructions from CLAUDE.md and can use nested instruction files. This is one reason it feels effective on continuing repositories: the durable project rules live beside the code rather than only in the chat.

**Type:** CLAUDE / CODE  
**Evidence:** OFFICIAL ANTHROPIC  
**Last checked:** 2026-09-24

### Details
Anthropic documents project memory at ./CLAUDE.md, user memory at ~/.claude/CLAUDE.md and nested discovery for subdirectories. CLAUDE.md can import other files.

For Aletheia, do not copy the entire protocol into CLAUDE.md. Use it as a short router:

- identify the canonical project guides;
- say what must be read before editing;
- give test/build commands;
- state the source-of-truth hierarchy;
- state approval and publication boundaries.

This closely parallels the useful Codex AGENTS.md pattern. Aletheia can maintain a shared vendor-neutral core and small provider-specific router files.

### Sources
- https://docs.anthropic.com/en/docs/claude-code/memory
- https://docs.anthropic.com/en/docs/claude-code/getting-started

---

## AI-201 | Current Claude combines quick chat and longer task execution

### Summary
Anthropic is merging the older Cowork distinction into a unified Claude experience. Current Claude can choose between a quick answer and a longer task, while retaining projects, connectors, skills, files, browser/computer use and scheduled work where available.

**Type:** CLAUDE / AGENT  
**Evidence:** OFFICIAL ANTHROPIC  
**Last checked:** 2026-09-24

### Details
Anthropic's current guidance says the Cowork capabilities are being rolled into ordinary Claude. Longer tasks can use browser/computer capabilities, connected tools and project context.

That makes the product-level comparison with ChatGPT Work less about "does it have an agent?" and more about:

- how easily the agent gets the right project context;
- how well repository instructions are enforced;
- what connectors/actions are available;
- how clear approvals are;
- how much work the plan allows.

### Sources
- https://support.claude.com/en/articles/16761823-claude-cowork-and-chat-are-one-claude
- https://support.claude.com/en/articles/13345190-get-started-with-claude-cowork

---

## AI-202 | Claude Projects provide files, instructions and scoped memory

### Summary
Claude Projects group related work with their own files, instructions, context and memory. Project memory is scoped to the project rather than automatically becoming global context.

**Type:** CLAUDE / PROJECTS  
**Evidence:** OFFICIAL ANTHROPIC  
**Last checked:** 2026-09-24

### Details
This fits Aletheia's separation between:

- universal user preferences;
- project-specific state;
- transient task context.

Keep important project facts in the canonical Aletheia state/knowledge file rather than assuming an invisible memory system is complete. Project memory is convenience; the ledger is inspectable continuity.

### Sources
- https://support.claude.com/en/articles/14116274-organize-your-tasks-with-projects-in-claude-cowork
- https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context

---

## AI-203 | Claude scheduled tasks can run in the cloud

### Summary
Paid Claude plans can schedule recurring task sessions, including reports, research and connected-tool workflows. Current cloud schedules can run when the user's computer is off, subject to whether the task needs local-only resources.

**Type:** CLAUDE / AUTOMATION  
**Evidence:** OFFICIAL ANTHROPIC  
**Last checked:** 2026-09-24

### Details
Anthropic lists examples such as daily briefings, weekly reports, recurring research and file organisation.

Aletheia should apply the same automation rules across providers:

- low-risk first;
- smallest required permission;
- clear source/time window;
- meaningful-change threshold where appropriate;
- receipt per run;
- no unattended consequential send/purchase/delete unless explicitly authorised and technically safeguarded.

### Sources
- https://support.claude.com/en/articles/13854387-schedule-recurring-tasks-in-claude-cowork
- https://support.claude.com/en/articles/13364135-use-claude-cowork-safely

---

## AI-204 | Claude Code has local loops and cloud jobs for recurring engineering work

### Summary
Claude Code's current power-user guidance includes local recurring loops and cloud scheduled jobs, making repeated PR/documentation/maintenance workflows part of the coding environment itself.

**Type:** CLAUDE / CODE / AUTOMATION  
**Evidence:** OFFICIAL ANTHROPIC  
**Last checked:** 2026-09-24

### Details
Anthropic documents local /loop tasks and cloud /schedule jobs. The exact syntax is provider-specific, but the Aletheia concept is portable: turn a proven manual procedure into a named skill, add a cadence/trigger, then require a result receipt.

Do not automate an unreliable workflow merely to make it frequent. First prove the steps manually and define a rollback/review boundary.

### Sources
- https://support.claude.com/en/articles/14554000-claude-code-power-user-tips

---


## AI-205 | Claude now has both lightweight Projects and longer cloud task workflows

### Summary
Claude Projects are available even on Free accounts, while paid Claude task workflows can run connected, recurring work in the cloud. Treat Projects as reusable context and scheduled/task execution as a separate capability.

**Type:** CLAUDE / PROJECTS / TASKS  
**Evidence:** OFFICIAL ANTHROPIC  
**Last checked:** 2026-09-24

### Details
Anthropic's current Projects help says Projects provide a self-contained workspace with files, instructions and knowledge; a newer Projects beta begins with Claude Code and can spawn parallel cloud threads that inherit project files, repositories, instructions and memory.

Current scheduled tasks are available on paid plans and can use connected tools, skills and plugins for recurring briefings, reports, research and file work.

For Aletheia, keep three layers distinct:

1. portable Aletheia state;
2. Claude Project context and memory;
3. task/Code execution.

Do not treat one layer as proof that another has been saved.

### Sources
- https://support.claude.com/en/articles/9517075-what-are-projects
- https://support.claude.com/en/articles/13854387-schedule-recurring-tasks-in-claude-cowork

---

## AI-206 | Claude's current memory is editable, but Aletheia should still carry canonical state

### Summary
Claude memory now works across chat and its cloud task experience for many personal plans, and Anthropic exposes remembered topics for user review. This improves convenience but does not replace an inspectable project ledger or handover.

**Type:** CLAUDE / MEMORY / ALETHEIA  
**Evidence:** OFFICIAL ANTHROPIC  
**Last checked:** 2026-09-24

### Details
Anthropic's September 2026 release notes say memory is on by default for Free, Pro and Max, with Topics under Settings > Memory that can be edited or deleted; sensitive-topic handling has separate controls.

Aletheia should use provider memory for convenience while preserving:

- explicit corrections;
- project decisions;
- unresolved conflicts;
- source provenance;
- authority boundaries;
- handovers/checkpoints.

Those are project records, not assumptions about what a provider remembers.

### Sources
- https://support.claude.com/en/articles/12138966-release-notes
- https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context

---

# DeepSeek

## AI-300 | DeepSeek V4.1 Flash is the current fast multimodal/agent model

### Summary
DeepSeek released V4.1 Flash on 10 September 2026 with native visual understanding and an architecture focused on speed, throughput, cache efficiency and agent work. The current API model name is deepseek-flash.

**Type:** DEEPSEEK / MODEL  
**Evidence:** OFFICIAL DEEPSEEK  
**Last checked:** 2026-09-24

### Details
DeepSeek's current changelog says V4.1 Flash supports native multimodal input and highlights improvements in coding and agent benchmarks. Earlier V4 Flash names are temporarily routed to V4.1 Flash for compatibility.

This makes DeepSeek interesting as an economical provider in a portable Aletheia/Odysseus model-routing setup. Model cost and availability should still be rechecked before hard-coding routing rules.

### Sources
- https://api-docs.deepseek.com/updates/
- https://api-docs.deepseek.com/news/news260910/

---

## AI-301 | DeepSeek is useful for free/low-cost work, but portable memory files need privacy discipline

### Summary
DeepSeek's consumer app offers search, reasoning and file-upload workflows, but Aletheia should be especially deliberate about what portable personal-memory data is sent to any third-party provider.

**Type:** DEEPSEEK / PRIVACY  
**Evidence:** OFFICIAL DEEPSEEK  
**Last checked:** 2026-09-24

### Details
Use a minimal task-specific Aletheia handover rather than automatically uploading a complete personal profile.

The general rule is provider-neutral: the fact that a memory file is portable does not mean every provider needs every field in it.

For higher-sensitivity data, check the current provider privacy policy, account controls, storage region and training/data-use terms before upload.

### Sources
- https://chat.deepseek.com/
- https://cdn.deepseek.com/policies/en-US/deepseek-privacy-policy.html
- https://api-docs.deepseek.com/updates/

---


## AI-302 | DeepSeek's API is stateless, so Aletheia must supply state explicitly

### Summary
DeepSeek's current Chat Completions and Responses APIs do not store the conversation for you. Every multi-turn or agent wrapper must send the required history/state again, which makes an explicit Aletheia state pack particularly natural.

**Type:** DEEPSEEK / API / ALETHEIA  
**Evidence:** OFFICIAL DEEPSEEK  
**Last checked:** 2026-09-24

### Details
DeepSeek documents both APIs as stateless. The Responses API does not support stored conversations or `previous_response_id`.

A good wrapper therefore sends:

- a compact system/Aletheia bootstrap;
- only the current task-relevant user state;
- required conversation history;
- tool results;
- a checkpoint summary when history is compacted.

DeepSeek's automatic context caching can make repeated stable prefixes cheaper, but caching repeated bytes is not persistent Aletheia memory.

### Sources
- https://api-docs.deepseek.com/guides/multi_round_chat
- https://api-docs.deepseek.com/api/create-response/
- https://api-docs.deepseek.com/guides/kv_cache/

---

## AI-303 | DeepSeek supplies tool-call decisions; the host executes the tools

### Summary
DeepSeek can request external function/tool calls, including in current thinking modes, but the model does not execute the function itself. The host application or orchestrator remains responsible for permissions, execution and returning the result.

**Type:** DEEPSEEK / AGENT / TOOLS  
**Evidence:** OFFICIAL DEEPSEEK  
**Last checked:** 2026-09-24

### Details
This makes DeepSeek a sensible model inside Odysseus or another Aletheia-controlled harness:

1. model proposes the tool call;
2. harness checks authority/permission;
3. harness executes the real function;
4. result is returned to the model;
5. Aletheia records consequential effects.

Do not confuse model tool-call capability with permission to act.

### Sources
- https://api-docs.deepseek.com/guides/tool_calls/
- https://api-docs.deepseek.com/updates/

---

# Odysseus, Aletheia and Thalia

## AI-400 | Aletheia is the evidence and state layer

### Summary
Aletheia's job is to preserve intent, provenance, corrections, conflicts, evidence gaps, decisions and user authority. It should not pretend to be the model, browser, scheduler or tool executor.

**Type:** ALETHEIA PROTOCOL  
**Evidence:** CANONICAL PROJECT DESIGN  
**Last checked:** 2026-09-24

### Details
Aletheia is strongest when it answers questions such as:

- What did the user actually say?
- Which source supports this claim?
- What changed?
- Which old fact is superseded?
- What remains uncertain?
- What decision was made and why?
- What may the agent do without another approval?
- What must be handed to the next AI?

It is a governance/context layer, not a claim that an AI has perfect memory or perfect truth.

### Sources
- https://github.com/KarstenEvans/aletheia-protocol

---

## AI-401 | Thalia is a presentation layer, never an evidence layer

### Summary
Thalia can add warmth, humour, positive framing and a consistent voice, but it must never change evidence strength, provenance, uncertainty, conflicts, safety boundaries or decisions.

**Type:** THALIA PROTOCOL  
**Evidence:** PROJECT DESIGN  
**Last checked:** 2026-09-24

### Details
The clean stack is:

    evidence/state -> Aletheia
    action/tool routing -> agent or Odysseus
    tone/presentation -> optional Thalia

This separation allows serious tasks to switch Thalia down or off without losing the state discipline underneath.

### Sources
- https://github.com/KarstenEvans/aletheia-protocol

---

## AI-402 | Odysseus can be an independent orchestration workspace

### Summary
The current open-source Odysseus project is a self-hosted AI workspace with chat, agents, research, documents, memory, email/calendar-style workflows, local or hosted models, MCP, files, shell and skills. That makes it a plausible independent execution layer for Aletheia rather than another memory protocol.

**Type:** ODYSSEUS / ORCHESTRATION  
**Evidence:** OPEN-SOURCE PROJECT DOCUMENTATION  
**Last checked:** 2026-09-24

### Details
Current Odysseus documentation describes support for local/API model backends including OpenAI, Anthropic and Gemini-compatible routes, with agents that can use tools such as MCP, web, files, shell, skills and memory.

The clean Aletheia relationship is:

    human request
      -> Aletheia intent, evidence and authority
      -> optional Thalia presentation
      -> Odysseus capability/model routing
      -> tool/provider action
      -> receipt
      -> Aletheia state update

That keeps Aletheia portable if the preferred model changes.

Odysseus is powerful self-hosted software and therefore has its own installation, security and maintenance burden. It is an optional capability layer, not a foundation requirement for ordinary Aletheia apps.

### Sources
- https://github.com/odysseus-dev/odysseus
- https://github.com/EdSkamor/odysseusAI

---

## AI-403 | Odysseus with ChatGPT: use OpenAI as a model/tool provider, not the owner of state

### Summary
Odysseus can call OpenAI-backed models while retaining a self-hosted orchestration layer. Aletheia can provide the governed task state, while Odysseus selects tools and the OpenAI model performs reasoning or execution.

**Type:** ODYSSEUS / CHATGPT  
**Evidence:** OPEN-SOURCE DOCUMENTATION + ALETHEIA DESIGN  
**Last checked:** 2026-09-24

### Details
Potential pattern:

1. Aletheia supplies task intent, constraints and source pointers.
2. Odysseus chooses an OpenAI endpoint/model and required MCP/files/browser tools.
3. The model works the task.
4. Odysseus returns outputs/tool results.
5. Aletheia records only verified changes and important unresolved issues.

This is different from using the ChatGPT consumer UI. It is primarily an API/self-hosted orchestration pattern and may incur provider API charges.

A zero-spend mode should therefore refuse a paid API action unless the user has explicitly enabled or approved paid usage.

### Sources
- https://github.com/odysseus-dev/odysseus
- https://openai.com/index/introducing-gpt-6-sol-and-luna/

---

## AI-404 | Odysseus with Gemini: Gemini can be one routed model while Google personal context stays separate

### Summary
Odysseus can use a Gemini model backend, but Gemini's consumer Personal Intelligence is not the same thing as calling a Gemini API from an independent orchestrator. Keep those layers conceptually separate.

**Type:** ODYSSEUS / GEMINI  
**Evidence:** OPEN-SOURCE DOCUMENTATION + OFFICIAL GOOGLE  
**Last checked:** 2026-09-24

### Details
A self-hosted Odysseus job can route a task to a Gemini model endpoint and provide the Aletheia state it needs.

Do not assume that this API call inherits the user's consumer Gemini memory, connected Gmail/Drive context or Personal Intelligence. If the workflow needs data from those systems, provide it through an explicitly authorised connector or task source.

This boundary is useful because it prevents accidental claims that "Gemini knows this from my account" when the actual agent is calling only a model API.

### Sources
- https://github.com/odysseus-dev/odysseus
- https://support.google.com/gemini/answer/16598623

---

## AI-405 | Odysseus MCP support makes tools portable across models

### Summary
Odysseus includes an MCP manager so tools can be added independently of the language model. This is strategically useful for Aletheia because the same capability can survive a switch from OpenAI to Gemini, Claude, DeepSeek or a local model.

**Type:** ODYSSEUS / MCP  
**Evidence:** OPEN-SOURCE PROJECT DOCUMENTATION  
**Last checked:** 2026-09-24

### Details
MCP separates "which model thinks about the task?" from "which tools are available?".

That can support Aletheia features such as:

- browser/research;
- filesystem/project operations;
- governed memory;
- specialist databases;
- email/calendar connectors;
- image/media generation;
- custom Aletheia tools.

However, not every model reliably emits or executes native tool calls in every harness. Test the actual model/tool combination instead of assuming MCP compatibility from a marketing label.

### Sources
- https://github.com/odysseus-dev/odysseus
- https://github.com/odysseus-dev/odysseus/blob/dev/scripts/odysseus-mcp

---

## AI-406 | Odysseus scheduled agents should produce Aletheia receipts

### Summary
Odysseus supports scheduled agent tasks and related task/calendar features. Aletheia should wrap unattended runs with explicit authority, cost and receipt rules so automation does not silently become autonomy without limits.

**Type:** ODYSSEUS / AUTOMATION / ALETHEIA  
**Evidence:** OPEN-SOURCE DOCUMENTATION + PROJECT DESIGN  
**Last checked:** 2026-09-24

### Details
A robust scheduled run should record:

- job name and trigger;
- permitted data/tools;
- cost boundary;
- what was checked;
- what changed;
- what failed or remained uncertain;
- whether human approval is now required.

For Aletheia AUTO mode, a safe default is **£0.00 unapproved spend**. If the required provider/tool would incur a new charge, return APPROVAL_REQUIRED rather than spending silently.

### Sources
- https://github.com/odysseus-dev/odysseus
- https://github.com/KarstenEvans/aletheia-protocol

---


# Kimi / Moonshot AI

## AI-600 | Kimi now spans Chat, Search, Memory, Agent, Work and Code

### Summary
Kimi is no longer just a chat model. Its current product family includes ordinary Chat/Search, a long-term Memory Space, autonomous Agent mode, the local Kimi Work agent and Kimi Code for repository engineering.

**Type:** KIMI / PLATFORM  
**Evidence:** OFFICIAL KIMI  
**Last checked:** 2026-09-24

### Details
Kimi's current new-user guide describes:

- **Chat** for ordinary conversation and files;
- **Search** for current web information;
- **Memory Space** for durable preferences and references to past chats;
- **Agent** for autonomous websites, documents, data analysis and presentations;
- **Kimi Work** as a local knowledge-worker agent;
- **Kimi Code** as its coding agent.

This is a strong match for Aletheia because the portable layer can remain outside all six surfaces.

### Sources
- https://www.kimi.com/en/help/new-user-guide/overview
- https://www.kimi.com/en/help

---

## AI-601 | Kimi's simple Aletheia setup is Memory Space plus a portable file

### Summary
For ordinary Kimi, keep stable personal preferences in Memory Space only when wanted and keep the inspectable `aletheia-memory.md` as the portable source. Use Search for freshness and Agent only when the task actually needs execution.

**Type:** KIMI / PERSONALISATION / ALETHEIA  
**Evidence:** OFFICIAL KIMI + ALETHEIA DESIGN  
**Last checked:** 2026-09-24

### Details
Recommended route:

1. keep the universal bootstrap short;
2. use Memory Space for approved durable preferences, not a complete case archive;
3. attach the portable Aletheia memory/checkpoint when a project needs exact state;
4. use Quick Prompts for frequently reused small instructions;
5. move to Agent mode only for an execution-shaped job.

As with every provider memory, an explicit Aletheia correction outranks an older remembered assumption.

### Sources
- https://www.kimi.com/en/help/new-user-guide/overview

---

## AI-602 | Kimi Work is a local agent with permissions, WebBridge, Skills and schedules

### Summary
Kimi Work can operate local files and browser workflows, install Skills/plugins, use projects and schedule tasks. Its local schedules only run while Kimi Work is open, whereas Kimi's cloud-created scheduled tasks do not require the desktop client to remain running.

**Type:** KIMI / WORK / AUTOMATION  
**Evidence:** OFFICIAL KIMI  
**Last checked:** 2026-09-24

### Details
Kimi Work exposes three permission levels, from routine automatic operation through manual approval to fully automatic execution. WebBridge can click, scroll and extract data in a browser.

Aletheia should map this to a clearer authority ladder:

- read/observe;
- draft/preview;
- modify local reversible state;
- external or irreversible action.

Do not select fully automatic mode merely for convenience when an action can publish, delete, overwrite or transmit private information.

### Sources
- https://www.kimi.com/en/help/kimi-work/overview
- https://www.kimi.com/en/help/kimi-work/kimi-work-faq
- https://www.kimi.com/en/help/kimi-work/release-notes

---

## AI-603 | Kimi Code understands AGENTS.md, Skills, MCP and Markdown-defined agents

### Summary
Kimi Code is especially Aletheia-friendly because it can read project `AGENTS.md`, discover reusable `SKILL.md` workflows, connect MCP tools and define custom agents in Markdown.

**Type:** KIMI / CODE / ALETHEIA  
**Evidence:** OFFICIAL KIMI  
**Last checked:** 2026-09-24

### Details
Kimi documents global and project instruction files and can generate an initial `AGENTS.md` with `/init`. It also supports project/user Skills and custom agents.

That means the same small Aletheia repository router created for Codex can serve Kimi Code too, while detailed workflows stay in canonical docs or Skills.

Security boundary: project agent files are themselves instructions and can be untrusted when a repository is unfamiliar. Review agent/skill configuration before granting broad tools.

### Sources
- https://www.kimi.com/en/help/kimi-code/cli-customization
- https://www.kimi.com/code/docs/en/kimi-code-cli/customization/agents
- https://www.kimi.com/code/docs/en/kimi-code-cli/customization/skills.html

---

## AI-604 | Kimi sub-agents preserve main context but multiply token consumption

### Summary
Kimi sub-agents use isolated context windows, which keeps exploratory work out of the main context and allows parallelism, but each sub-agent consumes its own model tokens. More agents are therefore not automatically more efficient.

**Type:** KIMI / MULTI-AGENT / COST  
**Evidence:** OFFICIAL KIMI  
**Last checked:** 2026-09-24

### Details
This supports an Aletheia rule that should apply across providers: use sub-agents when work is genuinely parallel or needs isolated context; keep simple sequential work in one agent.

A swarm of agents can become a swarm of invoices, duplicated searches and conflicting partial states if orchestration is weak.

### Sources
- https://www.kimi.com/code/docs/en/kimi-code-cli/customization/agents

---

# Manus

## AI-700 | Manus Projects are persistent reusable Aletheia-shaped workspaces

### Summary
Manus Projects provide a master instruction, knowledge files and shared/reusable context for sessions. This is one of the cleanest current places to install an Aletheia project adapter without making the provider memory canonical.

**Type:** MANUS / PROJECTS / ALETHEIA  
**Evidence:** OFFICIAL MANUS  
**Last checked:** 2026-09-24

### Details
A practical Aletheia Manus Project can contain:

- the compact Aletheia bootstrap as Project instruction;
- an approved `aletheia-memory.md` or project-state file;
- relevant source documents;
- selected Skills;
- optional connectors.

Manus can now propose Project instruction/file/skill updates learned from completed work, but official guidance says those context changes require user approval. That fits Aletheia's propose-before-accept pattern well.

### Sources
- https://manus.im/en/blog/manus-projects
- https://manus.im/blog/manus-projects-self-updating
- https://open.manus.im/docs/v2/project.create

---

## AI-701 | Manus Chat is lightweight; Agent mode spends credits on actual execution

### Summary
Manus separates a lightweight Chat mode from Agent mode. Chat does not currently consume Manus credits, while Agent tasks consume credits based on LLM tokens, virtual-machine use and third-party APIs.

**Type:** MANUS / COST / AGENT  
**Evidence:** OFFICIAL MANUS  
**Last checked:** 2026-09-24

### Details
This is closely related to the practical problem seen with limited agent allowances elsewhere: autonomous work has a real execution budget.

Use Chat for discussion/research when execution is unnecessary. Use Agent for work that genuinely benefits from its sandbox/browser/code/file capabilities. Break expensive long jobs into checkpoints rather than asking the agent to rediscover the whole project after a budget interruption.

### Sources
- https://help.manus.im/en/articles/11711128-what-are-the-differences-between-chat-mode-and-agent-mode
- https://help.manus.im/en/articles/11711097-what-are-the-rules-for-credits-consumption-and-how-can-i-obtain-them

---

## AI-702 | Manus Skills can be packaged and imported directly from GitHub

### Summary
Manus Skills use a `SKILL.md` plus optional scripts/references/templates and can be shared as skill packages, ZIPs or public GitHub repositories. That makes the existing Aletheia 11 Skills pack a realistic candidate for a future compatibility test.

**Type:** MANUS / SKILLS / ALETHEIA  
**Evidence:** OFFICIAL MANUS  
**Last checked:** 2026-09-24

### Details
Do not blindly import all eleven.

First test a small low-risk workflow such as Humanizer or GEO/AEO, then test the competitor-monitor skill with read-only public web sources. Review any third-party Skill before enabling it because a Skill can contain executable resources.

### Sources
- https://help.manus.im/en/articles/14753565-how-to-share-and-use-skills-in-manus

---

## AI-703 | Manus Scheduled Tasks 2.0 can keep the context where the recurring work lives

### Summary
Manus schedules can run inside a task, Project or Manus-built web app and reuse that location's instructions, files and results instead of rebuilding context on every run.

**Type:** MANUS / AUTOMATION  
**Evidence:** OFFICIAL MANUS  
**Last checked:** 2026-09-24

### Details
This is a particularly good fit for Aletheia Watch:

- Project holds the business type, postcode/radius, selected competitors and approved watch pages;
- the first run establishes a dated baseline;
- a weekly schedule refreshes the same monitored fields;
- the output records supported changes and unchanged/unknown fields;
- a human decides whether any response is needed.

### Sources
- https://manus.im/blog/manus-schedules

---

## AI-704 | Manus can operate cloud or local computers, so the authority envelope matters

### Summary
Manus offers a persistent Cloud Computer and a Desktop "My Computer" route that can read/edit local files, execute terminal commands and operate workflows. This increases capability and therefore increases the need for narrow permissions and receipts.

**Type:** MANUS / COMPUTER USE / SAFETY  
**Evidence:** OFFICIAL MANUS  
**Last checked:** 2026-09-24

### Details
The Cloud Computer persists files, installed tools and running processes. The desktop app can work in authorised folders and can be remotely tasked.

Aletheia should record:

- which machine/environment is in scope;
- which folders/accounts are authorised;
- whether network/external actions are allowed;
- what irreversible operations still need confirmation;
- what changed during the run.

### Sources
- https://help.manus.im/en/articles/15392111-what-is-the-cloud-computer
- https://help.manus.im/en/articles/14178443-what-is-the-my-computer-feature-capable-of
- https://help.manus.im/en/articles/11711218-how-can-i-take-over-manus-browser-or-vs-code

---

## AI-705 | Manus connectors can turn an Aletheia Project into an action workflow

### Summary
Manus connectors can attach Gmail, Calendar, Drive, GitHub, databases and custom/MCP tools to a Project. Keep the Project instruction stable and connect only the systems required for that workflow.

**Type:** MANUS / CONNECTORS  
**Evidence:** OFFICIAL MANUS  
**Last checked:** 2026-09-24

### Details
For Aletheia, connector configuration belongs in the authority layer, not in a public memory file.

A project may recommend or use connectors while each user's account credentials remain separately authorised. Shared instructions do not imply shared private account data.

### Sources
- https://help.manus.im/en/articles/12231777-how-can-i-use-manus-connectors
- https://manus.im/blog/projects-connectors

---

# Grok / SpaceXAI

## AI-800 | Grok now has a full coding/build surface, not only conversational Grok

### Summary
Grok 4.7 is SpaceXAI's current flagship coding/knowledge-work model, and Grok Build is available across plans for building apps, websites, games and dashboards on web and mobile.

**Type:** GROK / MODEL / BUILD  
**Evidence:** OFFICIAL SPACEXAI  
**Last checked:** 2026-09-24

### Details
For Aletheia, separate:

- ordinary Grok conversation;
- Grok Build for project/code creation;
- Skills for reusable workflows;
- Automations for recurring jobs;
- connectors/MCP for external systems.

The same provider-neutral Aletheia state can sit above all of them.

### Sources
- https://x.ai/news/grok-4-7
- https://x.ai/news/grok-build-for-everyone
- https://x.ai/build/changelog

---

## AI-801 | Grok Skills provide persistent reusable expertise

### Summary
Grok Skills are designed to carry reusable instructions and workflow expertise across conversations, including document, presentation, spreadsheet and PDF work plus custom user-created Skills.

**Type:** GROK / SKILLS / ALETHEIA  
**Evidence:** OFFICIAL SPACEXAI  
**Last checked:** 2026-09-24

### Details
An Aletheia adapter is a natural custom Skill candidate, but keep the Skill small and point it to portable project state where exact provenance/decisions matter.

Do not assume a Grok Skill package is byte-for-byte compatible with Codex/Kimi/Manus Skills. Reuse the workflow meaning; adapt the packaging to the provider.

### Sources
- https://x.ai/news/grok-skills

---

## AI-802 | Grok Automations can run on schedules or email triggers

### Summary
Grok Automations can repeat a saved job on a schedule or when an email arrives, using attached files, connectors and Skills as context.

**Type:** GROK / AUTOMATION  
**Evidence:** OFFICIAL SPACEXAI  
**Last checked:** 2026-09-24

### Details
This is suitable for read-mostly Aletheia monitors such as:

- competitor page changes;
- vacancy scans;
- scheduled research;
- mailbox attention rules.

Use a meaningful-change condition so an automation does not generate noise merely because it ran.

### Sources
- https://x.ai/news/grok-automations

---

## AI-803 | Grok connectors and custom MCP can attach live systems

### Summary
Grok currently lists connectors including GitHub, Notion, Vercel, Box, Canva and others, and supports custom MCP servers. Connector availability is capability; Aletheia still controls whether a particular task is authorised to act.

**Type:** GROK / CONNECTORS / MCP  
**Evidence:** OFFICIAL SPACEXAI  
**Last checked:** 2026-09-24

### Details
For private systems, minimise scope and avoid placing credentials or connection secrets in portable Markdown. Keep evidence links and action authority separate.

### Sources
- https://docs.x.ai/grok/connectors

---

## AI-804 | Grok Build memory separates project notes from global preferences

### Summary
Grok Build now keeps Markdown memory notes for project conventions/decisions and separate global preferences. Current-conversation instructions take precedence over the stored notes.

**Type:** GROK / MEMORY / ALETHEIA  
**Evidence:** OFFICIAL SPACEXAI  
**Last checked:** 2026-09-24

### Details
This is close to Aletheia's desired split, but Grok's memory remains provider-managed working memory.

Keep canonical evidence/conflicts/decisions in the repository or portable Aletheia state. Use Grok memory for convenient coding conventions and durable preferences, not as the sole audit record.

### Sources
- https://x.ai/news/grok-build-memory

---

# Cross-provider design

## AI-500 | Use one portable Aletheia bootstrap plus small provider adapters

### Summary
Do not maintain four unrelated giant prompts. Keep one compact vendor-neutral Aletheia bootstrap and add small provider-specific adapters for features that genuinely differ, such as AGENTS.md, CLAUDE.md, Gemini Gems or ChatGPT Work.

**Type:** CROSS-PROVIDER / ALETHEIA  
**Evidence:** PROJECT DESIGN + PROVIDER DOCUMENTATION  
**Last checked:** 2026-09-24

### Details
Suggested structure:

- aletheia-bootstrap.md — universal evidence, correction, authority and untrusted-material rules;
- aletheia-memory.md — optional user-controlled portable context;
- integrations/chatgpt.md — Work/Codex/plugins/tasks/AGENTS.md notes;
- integrations/gemini.md — Personal Intelligence/Gem boundaries;
- integrations/claude.md — CLAUDE.md/Projects/Claude Code notes;
- integrations/deepseek.md — model/API/privacy notes;
- CHECKPOINT and HANDOVER formats shared by all providers.

Provider features may improve or disappear. The portable core should remain useful even when every integration file is removed.

### Sources
- https://github.com/KarstenEvans/aletheia-protocol
- https://developers.openai.com/codex/guides/agents-md/
- https://docs.anthropic.com/en/docs/claude-code/memory
- https://support.google.com/gemini/answer/15235603

---

## AI-501 | Aletheia worldwide apps should be static-first with optional AI intelligence

### Summary
The proposed worldwide Aletheia site can be a collection of small HTML apps over shared Markdown/JSON knowledge and user-controlled preferences. AI should enhance discovery and synthesis without making the front door disappear when an API is unavailable.

**Type:** ALETHEIA APP ARCHITECTURE  
**Evidence:** PROJECT DESIGN  
**Last checked:** 2026-09-24

### Details
Candidate apps include:

- **A-to-Z:** general local/global discovery.
- **Employment:** skills, location, working pattern, exclusions and live vacancies.
- **What's On:** date, radius, interests and accessibility.
- **Meet:** user-controlled matching with stronger privacy/safety boundaries.
- **Food:** location, diet/allergy, cuisine and budget.
- **Knowledge:** source-traced reusable subject libraries.
- **Storyteller:** portable stories, images, voices and embeds.
- **Music / Song Catchphrases:** linked cultural knowledge.
- further Aletheia tools as separate apps.

Each app can read only the Aletheia preference fields it needs. Public knowledge and private profile data should remain physically/logically separate.

### Sources
- https://karstenevans.github.io/aletheia-knowledge/
- https://github.com/KarstenEvans/aletheia-protocol

---

## AI-502 | Knowledge cards should contain the answer before they contain the search button

### Summary
A card is not useful if it merely restates a title and sends the person to Google. Store the stable explanation, caveats and known capability in the card; use web search to verify freshness or investigate beyond the stored knowledge.

**Type:** ALETHEIA KNOWLEDGE RULE  
**Evidence:** REPOSITORY GUI CONTRACT  
**Last checked:** 2026-09-24

### Details
Every card should provide:

- a meaningful title;
- a substantive preview;
- useful details;
- evidence/status;
- last-checked date for changing information;
- relevant source links;
- an optional live-search path for updates.

This design also makes the knowledge useful to other AIs, local search engines and offline readers.

### Sources
- https://github.com/KarstenEvans/aletheia-knowledge/blob/main/aletheia-knowledge-GUI.md

---

## AI-503 | Community sources are discovery and field experience, not primary truth

### Summary
Reddit, GitHub discussions and public forum posts are valuable for discovering workflows, pain points and emerging tricks. They should be labelled as community evidence and checked against product documentation or direct testing before promotion to a factual capability card.

**Type:** RESEARCH METHOD  
**Evidence:** ALETHEIA METHOD  
**Last checked:** 2026-09-24

### Details
Useful community themes found during this research include:

- Astra allowance can disappear quickly on large high-effort agent/code tasks;
- lower effort can be surprisingly capable for routine coding;
- strong agents can supervise other coding agents;
- too many tools/plugins can make workflows harder to reason about;
- repository-level instructions are often more valuable than repeatedly improving the one-off prompt.

Public Discord content was not reliably searchable enough in this research pass to promote any Discord-specific claims. The correct entry is "not established", not an invented consensus.

### Sources
- https://www.reddit.com/r/ChatGPT/
- https://www.reddit.com/r/OpenAI/
- https://www.reddit.com/r/ClaudeAI/
- https://github.com/openai/codex
- https://github.com/odysseus-dev/odysseus/discussions

---

## AI-504 | Never confuse a confidence number with calibrated probability

### Summary
Prompts that ask an AI to attach "92% confidence" can look scientific without being calibrated. Aletheia should report evidence status, uncertainty and what would change the conclusion rather than inventing numerical certainty.

**Type:** ALETHEIA EVIDENCE  
**Evidence:** RESEARCH METHOD  
**Last checked:** 2026-09-24

### Details
A useful uncertainty report says:

- verified from current primary source;
- supported but not independently reproduced;
- community report;
- inference;
- unresolved conflict;
- unknown / not checked.

If a numeric probability comes from a real statistical model or measured dataset, explain its basis. Otherwise prefer qualitative, inspectable evidence labels.

### Sources
- https://github.com/KarstenEvans/aletheia-protocol

---

## AI-505 | AI capability cards need review dates because the landscape now changes in weeks

### Summary
Sora's discontinuation, Astra's rollout, Gemini's Personal Intelligence changes and Claude's Cowork merger all show that an undated AI guide decays rapidly. Every capability claim should carry a review date and a primary source where possible.

**Type:** RESEARCH METHOD  
**Evidence:** CURRENT PRODUCT CHANGES  
**Last checked:** 2026-09-24

### Details
Recommended freshness:

- model availability, pricing, quotas, connectors and plan access: recheck before consequential use;
- stable workflow concepts such as provenance and selective disclosure: slower review cycle;
- community tips: retain date and never silently convert them into provider facts;
- discontinued features: keep a dated historical note when old tutorials are likely to mislead users.

This is why Aletheia AI Knowledge should be easy to update card-by-card rather than rebuilt from scratch.

### Sources
- https://openai.com/index/introducing-gpt-6-sol-and-luna/
- https://help.openai.com/en/articles/20001152-what-to-know-about-the-sora-discontinuation
- https://support.google.com/gemini/answer/16598623
- https://support.claude.com/en/articles/16761823-claude-cowork-and-chat-are-one-claude
- https://api-docs.deepseek.com/updates/

---


## AI-506 | Capability is a stack: model, interface, tools and context

### Summary
When an AI task fails, do not blame or praise the model alone. The result depends on the model, the interface/harness, available tools and the context supplied to the task.

**Type:** CROSS-PROVIDER / DESIGN  
**Evidence:** USER-SUPPLIED DISCOVERY MATERIAL + CURRENT PROVIDER DOCUMENTATION  
**Last checked:** 2026-09-24

### Details
This explains why the same underlying model can behave very differently in ordinary Chat, Work, Codex, Kimi Work, Manus Agent or an Odysseus harness.

Aletheia debugging should therefore ask:

1. Was the right model chosen?
2. Did the interface preserve enough working state?
3. Did the agent actually have the required tool/permission?
4. Did it receive the right source files, constraints and prior decisions?
5. Did the execution budget last long enough?

This principle was reinforced by the user-supplied *AI Fundamentals* cheat sheet and by current agent-platform documentation.

### Sources
- User-supplied PDF: *AI Fundamentals — The Cheat Sheet* (Property Filter, 2026), discovery source
- https://developers.openai.com/api/docs/guides/agents
- https://www.kimi.com/en/help/kimi-work/overview

---

## AI-507 | Use an action-permission ladder instead of one giant "agent access" switch

### Summary
Aletheia interfaces should distinguish observing from drafting, local modification and consequential external action. "The agent has access" is too vague to be a useful permission model.

**Type:** CROSS-PROVIDER / AUTHORITY  
**Evidence:** ALETHEIA DESIGN + DISCOVERY MATERIAL + PROVIDER PERMISSION MODELS  
**Last checked:** 2026-09-24

### Details
Practical ladder:

1. **READ / OBSERVE:** inspect public or authorised data.
2. **DRAFT / PREVIEW:** prepare a message, change or plan without applying it.
3. **LOCAL / REVERSIBLE WRITE:** modify an authorised working copy with rollback.
4. **EXTERNAL / CONSEQUENTIAL ACTION:** send, publish, delete, purchase, merge, change permissions or affect another system/person.

The higher the rung, the clearer the authority and receipt should be.

### Sources
- User-supplied PDF: *AI Fundamentals — The Cheat Sheet* (Property Filter, 2026), discovery source
- https://www.kimi.com/en/help/kimi-work/overview
- https://github.com/KarstenEvans/aletheia-protocol

---

## AI-508 | Mature AI adoption is workflow integration, not simply adding more agents

### Summary
Across current adoption material, the repeated failure mode is weak context and workflow integration rather than a shortage of AI tools. Add an agent only where it removes a real handoff or recurring workload.

**Type:** CROSS-PROVIDER / ADOPTION  
**Evidence:** USER-SUPPLIED INDUSTRY MATERIAL + ALETHEIA DESIGN  
**Last checked:** 2026-09-24

### Details
Useful progression:

- augment an existing task;
- automate a proven repeatable step;
- integrate context/tools across a workflow;
- only then consider agentic end-to-end operation.

This avoids turning an awkward process into an automated awkward process.

The user-supplied WalkMe and Superside materials repeatedly emphasise workflow context, guidance and integration. Microsoft similarly describes a progression from foundational assistant use to specialised solutions and then agents.

### Sources
- User-supplied PDF: *The State of Digital Adoption 2026* (WalkMe), discovery source
- User-supplied PDF: *The AI Reset* (Superside, 2026), discovery source
- User-supplied PDF: *The IT Guide — Becoming Frontier with Microsoft 365 Copilot and Agents* (Microsoft, 2026), discovery source

---

## AI-509 | Governance should leave evidence, not just a policy statement

### Summary
For AI that can affect people, data or external systems, Aletheia should preserve who authorised the system, what it was allowed to do, what sources it used, what changed and how incidents/corrections are handled.

**Type:** CROSS-PROVIDER / GOVERNANCE  
**Evidence:** USER-SUPPLIED GOVERNANCE MATERIAL + ALETHEIA PROTOCOL  
**Last checked:** 2026-09-24

### Details
The practical minimum is an inventory plus receipts:

- system/workflow identity and purpose;
- owner/operator;
- data and tool scope;
- impact/risk level;
- decision/action logs;
- review/monitoring date;
- incident/correction route;
- source/provenance where decisions rely on external evidence.

This aligns strongly with Aletheia's existing Agentic Systems Profile rather than requiring a new competing governance framework.

### Sources
- User-supplied PDF: *Governing AI in 2026* (OneTrust, 2026), discovery source
- https://github.com/KarstenEvans/aletheia-protocol

---

## AI-510 | Promote a workflow into an app only when the interface adds real value

### Summary
A reusable Skill is enough when the job is mainly an instruction pattern. Create an Aletheia app when users benefit from persistent inputs, visual state, saved baselines, filters, files, scheduled monitoring or a task-specific interface.

**Type:** CROSS-PROVIDER / SKILLS / APP DESIGN  
**Evidence:** ALETHEIA DESIGN + CURRENT SKILL PLATFORMS  
**Last checked:** 2026-09-24

### Details
Examples:

- Humanizer: mostly a Skill.
- Meeting Prep: mostly a Skill plus connectors.
- Competitor Monitor: becomes a better **Aletheia Watch** app because it needs a watch list, geography, baselines, page selection, schedules and change history.
- GEO/AEO Optimizer: can remain a Skill when checking text, but overlaps the richer Site Audit app for full websites.
- Weekly Review: a Skill unless a dashboard/history becomes useful.

The app should not exist merely to wrap a prompt in buttons.

### Sources
- https://developers.openai.com/api/docs/guides/tools-skills
- https://www.kimi.com/code/docs/en/kimi-code-cli/customization/skills.html
- https://help.manus.im/en/articles/14753565-how-to-share-and-use-skills-in-manus

---

# Research queue

The next provider-specific research passes should deepen:

- ChatGPT plugins that materially help Aletheia workflows rather than adding a long catalogue.
- OpenAI Work/Codex practical conformance tests using Aletheia repository rules.
- Gemini Spark conformance against the existing five-test adapter.
- Claude Code versus Codex on the same small Aletheia repository task, with identical acceptance criteria.
- DeepSeek V4.1 practical tool-use tests through an independent harness.
- Odysseus installation/security review before any deployment that can reach private data.
- Cross-provider profile format for the proposed Aletheia worldwide apps.
- A provider capability changelog so retired features do not remain presented as current.
