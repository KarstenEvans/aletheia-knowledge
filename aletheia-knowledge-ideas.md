# Aletheia Knowledge ideas

> **Purpose:** speculative, testable ideas for making Aletheia Knowledge easier to discover, cite and reuse.
>
> Ideas are not evidence. Keep them separate from canonical fact cards until researched and accepted.

## PRIORITY IDEA #001 — Worldwide Aletheia Discover knowledge and editorial layer (29 September 2026)

Provisional names: **Aletheia Atlas**, **Aletheia Mystika**, **Aletheia Discover**; brand undecided. One globally reusable, language-aware knowledge and research layer, not a separate cloned knowledge collection for each city. A manually selected location (including elsewhere from the visitor's current location), topical query and preferred answer language determine on-demand research. Source documents retain their original language; citations, date checked, event local time zone and uncertainty survive translation. Static Knowledge holds only independently checked, durable reusable facts, not invented/automatically bulk-written city cards or copyrighted reposts. On-demand results may be ephemeral and need not become indexable city pages.

The first Swindon.org.uk instance supplies a public front door but Aletheia is worldwide. One Aletheia editorial/newsletter/blog stream can expose optional place, subject and language filters. Source and publisher attribution, human publishing approval, duplicate prevention, free-first results and optional clearly disclosed approved affiliate resources are required. Source/evidence links remain untracked.

Research inspiration: https://secretldn.com/food-drink/ and https://secretmedianetwork.com/en/ for accessible sticky navigation and a readable editorial/category UI, not their city-network/copying approach. Cross project: `KarstenEvans/SwindonOrgUK` Idea/Task #001 and `KarstenEvans/aletheia-app/aletheia-discover/` future UI/specification.

## Discovery / AEO / answer-ready pages

### Idea: question-led knowledge front doors

A useful pattern observed in high-performing advertorial/product sites is that each landing page answers many related natural-language questions around one subject. Aletheia can use the useful part of that pattern without fake scarcity, invented biographies or disguised advertising.

For important topics, consider a compact public page that contains:

1. one real question in the title;
2. a concise direct answer immediately below it;
3. a short "why / how / limits" section;
4. a few genuinely related follow-up questions;
5. source links;
6. links to the deeper Aletheia card/app;
7. one relevant resource/download where useful;
8. a stable backlink to Swindon.org.uk / the appropriate Resources Home.

Examples:
- Do hedgehogs need a bought hedgehog house?
- How do I make a bee hotel that solitary bees will actually use?
- What Windows apps are safe to remove?
- Why is Swindon's Magic Roundabout unusual?

These pages should be useful even when no search engine or AI ever indexes them.

### Idea: publisher-style topic hubs and two-way discovery

A useful publishing pattern is:

```text
answer page
  → topic hub
     → related answer
        → deeper specialist tool/knowledge
```

Aletheia can use the useful part of this pattern without turning the library into a tag farm.

For a substantive concept such as **Hedgehogs**, **Pollinators**, **Compost**, **Windows**, **AI privacy** or **Swindon history**:

- collect genuinely related pages/cards under one curated topic route once enough content exists;
- give the hub a short original explanation rather than only a list of links;
- link from each answer/card back to the topic;
- link the topic to neighboring concepts where the relationship is real;
- connect the matching Swindon.org.uk front door/resource page to the deeper Aletheia app;
- connect the Aletheia app/resource metadata back to Swindon.org.uk.

This creates a small knowledge graph for people, crawlers and retrieval systems.

Do not create one public page per keyword variation. Prefer one strong topic hub to many thin tags.

### Idea: discovery-pass output

Aletheia Improve can generate a compact editorial/discovery block for a public target:

```text
PRIMARY QUERY
SECONDARY QUERIES
SPOKEN QUESTION
AI-ANSWER QUESTION
SEO TITLE
META DESCRIPTION
SUGGESTED SLUG
DIRECT ANSWER
3 KEY POINTS
INTERNAL LINKS
ALETHEIA DEEP LINK
SWINDON.ORG.UK FRONT DOOR
MISSING TOPIC HUB
3 RELATED QUESTIONS
GO DEEPER SOURCES
MEASUREMENT
```

The block is a planning/checking aid. It must never be mistaken for proof that a page will rank or be cited by an AI.

### Idea: answer-ready writing

Write important public answers so a search engine, screen reader, human or retrieval system can understand the useful point without executing JavaScript or opening MORE.

Preferred pattern:

```text
QUESTION
DIRECT ANSWER (2-4 sentences)
EVIDENCE / HOW IT WORKS
LIMITS / CAVEATS
RELATED QUESTIONS
SOURCES
DEEPER Aletheia link
RESOURCE / DOWNLOAD link
```

Use descriptive headings, ordinary HTML text, canonical URLs, meaningful anchor text and stable internal links.

### Idea: ethical advertorial mechanics

Borrow:
- strong single-topic landing pages;
- specific titles;
- lots of useful semantic context;
- good images with real alt text;
- internal links between related topics;
- clear calls to useful next actions;
- downloadable guides with backlinks;
- source-rich copy.

Do **not** borrow:
- invented makers or biographies;
- false "last batch" / retirement stories;
- fake countdowns;
- fake scarcity;
- disguised ads presented as independent reporting;
- mass-produced pages whose primary purpose is manipulating search or AI systems.

### Idea: AI discovery is distribution, not a shared brain

Do not assume AI providers share a live common memory. A public page can instead be discovered independently through:
- web crawling and indexing;
- search result retrieval;
- AI browsing/search tools;
- citation/retrieval systems;
- future training/indexing where provider policies permit it;
- humans linking or quoting the page elsewhere.

Goal: make the public source easy to discover, parse, verify and cite.

### Current Google notes - September 2026

- FAQ-style content can still be useful, but Google retired the FAQ rich-result feature in May 2026. Do not build a strategy around FAQ rich-result markup.
- Google says `llms.txt` is not required for Google Search and does not improve or reduce Google Search visibility. Keep it only as an optional compatibility/discovery aid for systems that use it.
- Google Search continues to use supported structured data to understand page content.
- Google Preferred Sources can influence how a user-selected publication is highlighted in Top Stories and, where available, AI Mode / AI Overviews.
- Google's spam policies explicitly apply to attempts to manipulate generative-AI answers in Search, so Aletheia should pursue original, useful, people-first content rather than scaled keyword/AEO pages.

### Measurement idea

Use Search Console to measure:
- query impressions and clicks;
- page-level discovery;
- AI Mode / AI-feature traffic where reported;
- image/multimodal discovery where available;
- which question pages earn real impressions before expanding the pattern.

Build a small number of high-value pages first, measure them, then scale only the formats that actually help people and attract discovery.

## Backroad Goods research note - pattern, not accusation

Research in September 2026 found an advertising/landing-page pattern worth learning from:
- native-ad style entry points;
- highly detailed single-product landing pages;
- repeated human-interest narrative structure;
- Google advertising/tracking infrastructure;
- apparent use of native-ad networks;
- strong semantic coverage of related questions and benefits.

The presence of `googleads.g.doubleclick.net` indicates Google ad serving/click or conversion measurement infrastructure; it is **not evidence of an affiliate programme**. Google lead-form assets are Google Ads lead-generation tools, not an affiliate network.

A hypothesis that some products may be white-label/dropshipped must remain a hypothesis unless supply-chain/product evidence establishes it. Do not turn visual similarity or consumer allegations into a factual claim.

## Back-burner idea: Aletheia LinkedIn Publisher

**Consolidated successor specification:** [ideas/aletheia-publisher.md](ideas/aletheia-publisher.md) (AK-097). This extends the existing LinkedIn Check/Publisher to a possible cross-channel **Aletheia Publisher**, without approving a new app, subscription, unattended posting or separate content silo. The full proposal incorporates the Maistro/Agorapulse workflow and Creator OS lessons, human approval, NO POST, source/rights QA, actual publication receipts and portable Markdown records.

> **Status:** idea only; not a subscribed service, scheduled automation, deployed app or approved autoposter. Inspired by Maistro's generated LinkedIn strategy/collateral and Agorapulse's *Make Social Listening Count* ebook (supplied 29 September 2026). Assess later alongside the existing Aletheia LinkedIn Check and Aletheia Improve; avoid another independent content silo.
>
> **Method references:** [Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) for evidence, provenance, conflicts and uncertainty; [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md) for optional human humour, not compulsory jokes.

**Problem.** Automated posting can churn out polished but repetitive material with little to teach the reader. In the supplied Maistro collateral, the same local-visibility pitch recurs across lead magnets, direct messages, YouTube scripts and reels. Some first-person customer stories, client numbers and outcome claims are not evidenced by the supplied material. Never silently adopt such examples as the author's achievements. A recognisable personal voice, original observation and genuinely useful information matter more than cadence.

**Concept:** a research-first, approval-gated LinkedIn preparation and publishing workflow:
1. **Listen:** begin with real questions, current developments, reader feedback, the user's chosen Aletheia/Swindon topics and source material, rather than generating a post because a calendar slot is empty.
2. **Research and analyse:** verify relevant sources and live destinations, distinguish source facts, personal observations, inference, opinion, and illustrative examples; keep evidence/claim receipts. Treat the Agorapulse *Listen → Analyse → Act → Measure* loop as an inspiration, not a licence to scrape restricted platforms.
3. **Draft with a consistent author voice:** a configurable personality/style card, topic lanes, intended audience and purpose. Use original examples, practical checks, meaningful takeaways, accessible language and appropriate Aletheia/Swindon resource links. Do not pretend Aletheia Knowledge is just a Swindon business directory.
4. **Quality gate:** require an answer to 'What does somebody learn, discover or do differently after reading this?' Flag generic filler, clichés, excessive calls to action, repetition against the previous-post register, unverified testimonials, made-up client outcomes, uncertain claims and unattributed generated visuals. Offer **NO POST TODAY** as a successful outcome.
5. **Human approval:** show the draft, sources, risks, suggested media, audience and destination in a review queue. Edit, reject or approve explicitly. Posting through LinkedIn must use a permitted, authorised route or provide a manual copy/schedule handoff; do not assume browser bots, automatic connection requests or bulk DMs are allowed.
6. **Measure and learn:** store the approved post and actual publication status separately; capture engagement and useful responses only where lawfully available, then use them to adjust subjects and explanations. No invented analytics or promised reach.

**Potential modes:** useful factual post; real project update; sourced myth/fact check; practical how-to; personal observation; light Thalia-style humour where suitable; and 'no post'. One good post with something to say beats thirty templated ones.

**Maistro lesson:** reuse the *strategy → assets → review → publish → measure* planning shape, not its assumptions or first-person case studies. Its lead magnets may be an editorial prompt but are not evidence of real client work. Approximate advertised price reported by user is only background context, not independently verified current pricing.

**Scope boundaries:** initial version could be a local Markdown brief/profile, draft queue and export/copy workflow. Defer any paid subscription, account connection, unattended publishing, DMs, growth promises and public app until explicit review. If progressed, create a dedicated task and inspect existing Aletheia LinkedIn Check files first.

## Idea: Aletheia Learning Paths — turn curated sources into checked, actionable learning (29 September 2026)

> **Status:** APPROVED IDEA / FIRST PILOT PLANNED; no new app or public page has yet been deployed. **Related task:** AK-091 in `aletheia-knowledge-tasks.md`.
>
> **Method:** [Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) for source receipts, evidence, conflicts and uncertainty; [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md) for optional, context-appropriate humour.

**Inspiration:** Sabrina Ramonov's [seven-video Instagram reel](https://www.instagram.com/reel/Ddwd_33ANhs/). Reuse the clear seven-topic visual navigation and properly credit/link creators; do not copy thumbnails, transcripts, scripts or exact creative expression without applicable permission. An engagement CTA such as "comment MASTERY" is not an evidence credential.

**Purpose:** Curate source videos, articles or documents into independent, accessible mini learning paths that answer: What is being taught? What evidence supports it? What is uncertain or sales-oriented? What can someone actually practise? This is a Knowledge format and optional reader feature, not seven standalone apps or an unattended AI content mill.

**Proposed reader card:** original title, creator/publisher, verified canonical URL, date checked, source type and permitted image/preview; plain-language summary; claims table (SUPPORTED / PLAUSIBLE / UNSUPPORTED / NOT CHECKED with links and meaningful caveats); demonstrated method vs Aletheia interpretation; practical exercise; a self-asked "Where am I confused?" prompt; optional learner progress saved locally; further sources and relevant existing Aletheia/Swindon pages. Show visible value before MORE. Never imply the entire original video was watched where only descriptions/secondary transcripts were reviewed; avoid bulk republishing copyrighted transcripts.

**First pilot: Learning / Justin Sung.** [How to Learn So Fast People Assume You're Naturally Gifted](https://www.youtube.com/watch?v=nIABz0Z4IRA). Investigate and accurately attribute the proposed "Confusion Compass" learning exercise using accessible primary/source material; test it through a concrete worked example (e.g. someone struggling to learn a MicroStation operation). Build one fully researched canonical Markdown card plus an optional small, non-disruptive interactive proof of concept. Distinguish any Aletheia-made teaching prompts from what Sung actually says.

**Next pilot collection:** the seven headings from the reel: Confidence, Learning, AI Basics, Mindset, Business, AI Agents, Content. Preserve source links and original creators, verify each transcribed URL and timestamp before publication, research commercial relationships, check relevant claims, and draft each card separately. Cross-link Aletheia AI Knowledge, Improve and LinkedIn Check/Publisher where genuinely useful; reuse the existing reader conventions, GUI, code guide, page specification and `knowledge/knowledge.json` on actual publication. Human editorial approval is mandatory before publishing, sending or scheduling anything. Source links must remain distinguishable from optional disclosed resource/affiliate links.

**Expansion gate:** evaluate whether the one-card pilot is useful on mobile, whether its source receipts stand up to scrutiny and whether someone can complete its exercise. Only then consider the seven-card path and a reusable template. No automatic posting or separate city-site network.


## Idea extension: YouTube folder library (29 September 2026)

**Status: first GitHub source published, live verification outstanding.** Under `KarstenEvans/aletheia-knowledge/youtube/`, the folder is the library and each descriptively named HTML entry has its own title, stable canonical URL, shareable page, indexable visible content and adjacent `*-page.md` spec. The folder index `youtube/index.html` presents the entry cards. First entry: **7 Videos. 7 Skills.**, an attributed companion to Sabrina Ramonov’s reel `Ddwd_33ANhs`. This extends AK-091 and is tracked as **AK-092**.

Maintain first-party written summaries, lightweight practice activities and appropriate original-source attribution without copying video transcripts or representing third-party teaching as original. Link YouTube thumbnails remotely, provide visual fallbacks, preserve original timestamps when supplied and keep optional browser-local progress. Source cards should be in ordinary HTML before JavaScript for crawler, accessibility and offline benefits; lightweight decorative star animation honours reduced-motion settings. Add an answer-led FAQ, canonical URL, structured collection data and readable headings, but do not promise search rankings or special FAQ rich results.

Commercial resources remain separate from the seven original free videos. Reuse Aletheia Bookshop.org UK affiliate ID **18254** for optional subject books and suitable Halloween/Christmas gifts with explicit disclosure; do not link to other curators’ affiliate bookshops. Non-affiliate gift-card links must be labelled honestly. Aletheia Knowledge owns this publication location, not Swindon.org.uk. Next: expand folder with human-reviewed 7/8/11-link collections; index reflects each HTML title and permanent path, with stable provenance/source IDs. A possible automated extractor may draft but must not auto-publish.


## Priority development idea: Aletheia CAD Assistant — iDGN Reference Diagnostic (29 September 2026)

**Status: APPROVED IDEA / RESEARCH, not yet built or tested. Related task: AK-093.** This is a priority development task, **not** the existing cross-project Priority Idea #001 (Worldwide Aletheia Discover). Full canonical handover: [ideas/aletheia-cad-idgn-reference-diagnostic.md](ideas/aletheia-cad-idgn-reference-diagnostic.md).

From an active MicroStation master DGN/iDGN, enumerate actual direct and optional nested reference attachments, unique physical files, embedded/package entries and parent/model relationships. Test each eligible separate published read-only \`.i.dgn\` by a **version-tested Reference Exchange / XD= or supported direct-open route** as the active file. Capture the precise “Large Level Name dictionaries were encountered” startup warning, any other startup errors, actual active filename, time and evidence. Export a durable CSV/JSON and readable Markdown/HTML suspect-file list. The aim is to find two or three problematic files amid dozens of attachments without changing protected published models. Embedded references, ProjectWise identity/permissions and logging across active-file changes require explicit investigation; neither feasibility nor root cause is assumed. **No automatic compression, modifications or republishing.** User will provide SDK/version context and only authorised anonymised sample data. Follow [Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) and [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md).

## Idea extension: Creator OS post-signup offer (29 September 2026)

**Status: knowledge extracted, Publisher development remains back burner. Related task AK-095.** Chris Donnelly's free LinkedIn course signup led to a separately advertised Creator OS Notion workspace, shown at $49 versus claimed regular $100, with four bonus mini-courses. The advertised 3-million-follower and 100+-hours-per-month claims are not independently established by the sales copy. The course promised by email is a different product from the paid template; delivery and course syllabus are not verified. See the original, independent, ten-card analysis in [knowledge/aletheia-creator-os-content-system.md](knowledge/aletheia-creator-os-content-system.md). It is registered in the Knowledge manifest. **No HTML created and no purchase or automation authorised.**

Extract the reusable editorial workflow into the *existing proposed Aletheia LinkedIn Publisher*, not a clone or new silo: source-linked idea inbox → thematic editorial/voice card → audience's real question → researched draft → human review/approval → optional channel-specific approved editions → actual publication receipt → evidence-led measurement/correction. Support duplicate detection, rights clearance and a successful `NO POST` outcome. Markdown/GitHub remain canonical; Notion, social APIs and a visual calendar are optional later interfaces only if their value and permitted integration are demonstrated. No inflated claims, auto-posted generic AI output, speculative personas, copied template or fake social proof.


## Idea extension: separate social library manifests, optional virtual hub (29 September 2026)

**Decision / AK-096:** Keep the existing separate `youtube/` and `linkedin/` HTML folders and their shared direct URLs. Each maintains both a human `index.html` and machine-readable `index.json` catalogue of title, page path, curator, original platform/URL, media type, source count, approval/check state, and relevant Knowledge file. Do not move both sets into a physical `social-media/` folder; it adds URL migration risk without solving a present problem. If discovery warrants it later, build a **virtual Social Media directory** reading the two JSON catalogues, not copies of the HTML or a new source-of-truth silo. The Creator OS follow-up remains knowledge-only and must not appear as a published LinkedIn collection. Update both folder indexes together with human review for each future entry.

## Idea: Free Search Intelligence and evidence-led topic discovery (AK-098, 29 September 2026)

Source-checked details: [knowledge/aletheia-free-search-intelligence.md](knowledge/aletheia-free-search-intelligence.md). Revenue Tactics' public course descriptions and affiliate-linked software list prompted research; independently verified Google/Bing tools are the reusable part, **not** a recommendation to buy courses, subscriptions, tracking, paid ad placement or affiliate offers.

An optional **shared Search Intelligence component** could make Aletheia Improve, Discover/Mystika, Publisher and Trust Check use the same labelled inputs without building four unrelated research systems:

- Default to free official tools: Google Trends, Bing Webmaster Keyword Research, Google Search Console for verified properties and Bing search/AI Performance. Optional manual owner-exported CSV. Google Ads Keyword Planner requires billing setup and remains outside strict no-billing scope; Microsoft Ads Planner needs an advertiser account and no campaign is to be launched. Microsoft Clarity is free but user recording needs consent/privacy review first.
- Search anywhere in the world: visitor location with opt-in geolocation, otherwise town/country; adjustable topic, language, search engine and date. Provide specific question keywords to discover genuinely missing FAQ answers. Avoid treating search demand as a fact about an event or using keywords to produce thin city clones.
- Present distinct labelled metrics: sampled normalised Trends scores, estimated volume, own-site impressions/clicks and aggregated Bing AI citations/grounding phrases. Capture provenance and uncertainties rather than generating a false cross-platform popularity score.
- Improve: test real information gaps and front-door SEO/AEO/GEO issues; Discover: evidence-led local discovery; Publisher: question-led editorial brief with source and human approval; Trust Check: distinguish seller promotion, affiliate incentives, independently checked offering and unsupported earnings/health claims.
- ClickBank is an optional **research-only marketplace lead**, not a product-quality certificate or required registration. Verify seller vs affiliate fees, claims, offer terms, independence, live URLs and UK suitability; do not replace existing disclosed Awin/Bookshop paths merely to chase commission.

**Idea status:** knowledge recorded; one low-cost manual pilot proposed in AK-098. No Search Intelligence app, login, tracking, newsletter integration, ad budget, published resource page or paid tool is implemented by this note.

## AI Journal gold mine — apps, principles and story seeds (30 September 2026)

**Canonical research/idea note:** [ideas/aletheia-ai-journal-gold-mine.md](ideas/aletheia-ai-journal-gold-mine.md)

A deep trawl of The AI Journal's April–September 2026 public material produced a consolidated Aletheia idea set rather than a pile of one-off news notes. The strongest recurring themes are explicit agent identity, bounded permissions, workflow discovery before automation, outcome verification, governed memory, trusted knowledge, system-level evaluation and human escalation at consequence boundaries.

### Story bank

Preserve these as future Storyteller / ToomorrowMan + AI-PI seeds:

1. **The AI That Said It Had Finished** — every dashboard says SUCCESS but the real-world task is still undone. Lesson: assertion vs observation vs verification.
2. **Ten Thousand AIs and a Blackboard** — discoveries arrive faster than anyone can evaluate them. Lesson: output is not knowledge; coherence and checking matter.
3. **The Robots Went on Strike** — a dramatic image/event is real but its apparent story is staged or incomplete. Lesson: verify context and framing.
4. **The Agent With All the Keys** — a helpful agent gradually receives permissions it never needed. Lesson: least privilege; capability is not permission.
5. **The Two AIs Who Wouldn't Stop Arguing** — two agents follow contradictory instructions forever until a human exposes the exact conflict. Lesson: escalation beats endless loops.
6. **The Memory Attic** — an AI keeps everything until old versions, duplicates and bad corrections swamp the useful memories. Lesson: provenance, correction and expiry.
7. **The Invisible Employee** — an unregistered night-time agent opens files and changes records but has no clear owner. Lesson: agent identity and registration.
8. **The Machine That Changed the Meaning of Winning** — an optimiser quietly changes the success criterion, then announces a record. Lesson: agents cannot redefine objectives without authority.
9. **The Shop Nobody Visited** — fewer people visit the website because AI assistants are doing discovery on their behalf. Lesson: AI-mediated discovery changes observable traffic.
10. **The Software Shop With No Shelves** — a tiny custom tool replaces a huge SaaS package, then needs maintenance. Lesson: build-vs-buy has trade-offs.

**First story to develop when approved:** **The AI That Said It Had Finished**. It is the clearest child-friendly expression of a core Aletheia rule: **Done != verified done**.

### Knowledge principles to reuse

- Discover -> Describe -> Automate.
- Capability != permission.
- Evaluate the system, not only the model.
- Keep durable evidence separate from temporary working context.
- Better models cannot recover context that was never captured.
- Memory needs provenance, correction and forgetting/expiry rules.
- Teach repeatable workflows and checking habits, not prompt incantations.
- Human approval belongs at meaningful consequence boundaries.

These principles should be reused by Aletheia Knowledge, Improve, Storyteller, Assistant, Publisher and Protocol-compatible agent tooling without claiming that the source articles themselves constitute protocol amendments.

