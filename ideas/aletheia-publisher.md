# Aletheia Publisher — research-led, human-approved publishing system

> **Aletheia Markdown | Consolidated project idea / developer handover**
>
> Status: **APPROVED FOR IDEA STORAGE; NOT IMPLEMENTED OR AUTHORISED TO AUTOPOST**. Recorded 29 September 2026. Related tasks **AK-095** (Creator OS knowledge), **AK-096** (separate library JSON manifests), **AK-097** (this Publisher specification).
>
> [Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) governs evidence, provenance, human authority, corrections, conflicts and receipts. [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md) allows optional authentic humour without replacing useful information.
>
> Ownership: Build on the existing **Aletheia LinkedIn Check / proposed LinkedIn Publisher**, not a competing system. Long-term interface name: **Aletheia Publisher**. LinkedIn is the first proposed output channel; other channels are optional adapters, not separate content brains. GitHub Markdown is the master.

## 1. Purpose and editorial rule

Make it easy to turn useful things discovered online and in the author's own projects into **original, source-traced, readable material**, ready for **human review and explicit publication approval**. Aletheia does not post because a calendar has an empty slot. `NO POST TODAY` is a valid successful outcome.

**One sentence acceptance question:** What can a real reader learn, discover, verify or do differently after seeing this? If the draft cannot answer this, keep it in research, improve it or discard it.

This extends three previously recorded inspirations, without buying or cloning them:

1. **Maistro / automated LinkedIn promotion:** strategic workflow and post/calendar idea, but not generic high-volume templated posts, invented case studies, first-person customer results or unattended social actions.
2. **Agorapulse social-listening material:** use the conceptual loop *listen → analyse → act → measure* with permitted data; do not infer a scraping licence or claim its reported case outcomes as Aletheia results.
3. **Chris Donnelly Creator OS sales page:** one idea inbox, content pillars, author voice, useful audience questions, a central editorial calendar, channel editions, collaboration and measurement. These are transferable organisational ideas, not a need to buy the seller's paid Notion workspace. The displayed $49/$100, 3-million-follower and 100+ hours/month statements remain **attributed promotional claims**; no purchased template or full mini-course contents were inspected. Full ten-card research: [Creator OS Content System](../knowledge/aletheia-creator-os-content-system.md).

Also learn from two completed **collection companions**: [Sabrina Ramonov's seven YouTube videos](../youtube/aletheia-7-videos-7-skills.htm) and [Chris Donnelly's twelve AI resources](../linkedin/aletheia-12-free-ai-guides.htm). Their curator/original-source receipts must survive Aletheia's summaries, exercises and optional gift sections.

## 2. Distinguish the four layers

| Layer | Canonical record | Meaning |
|---|---|---|
| **Discover / Capture** | Proposed private or user-approved inbox | A link, screenshot, user's real observation or question. Not a publication licence or fact. |
| **Knowledge** | `knowledge/*.md`, `knowledge/knowledge.json` | Independently written reusable findings with source receipts, caveats and checked dates; can remain knowledge-only forever. |
| **Published collection** | Existing `youtube/` and `linkedin/` HTML pages + `index.html` and `index.json` per folder | A human-approved, crawlable editorial companion. Original platform and original creator recorded separately from destination/library folder. |
| **Publisher workflow** | Proposed approved-post register and channel-specific renditions | Draws from first-party knowledge and checked material, never rewrites the canonical knowledge as a hidden social-only silo. |

**Folder decision, approved 29 September:** preserve `youtube/` and `linkedin/` and all existing direct URLs. Do **not** move files to a new physical `social-media/` folder now. `youtube/index.json` and `linkedin/index.json` list current entries while the respective `index.html` remains the human-readable folder directory. `knowledge/knowledge.json` already indexes the Knowledge folder. Later a **virtual Social Media hub** can combine these manifests without relocating anything. Only build it if needed and after explicit approval.

### Proposed per-folder JSON index fields
Stable `id`, `slug`, `title`, relative `html` pathname, `page_spec`, optional `knowledge` source, canonical `public_url`, `origin.platform`, `origin.curator`, `origin.original_url`, `origin.source_id`, actual linked media platform, item count, source/assembled/check dates, and status/limitations. Avoid claiming `live` on GitHub Pages until independently checked. Do not discover a directory by guessing file names.

**Original-source example:** Sabrina's seven-video recommendation originated as an **Instagram reel**, although the linked media are YouTube videos and we filed the companion under `youtube/`. “Published in the YouTube folder” is not proof that Sabrina posted the collection on YouTube.

## 3. Publisher pipeline and states

```text
CAPTURE
  → SOURCE / RIGHTS REVIEW
  → DUPLICATE & RELEVANCE CHECK
  → RESEARCH / CLAIM RECEIPTS
  → ORIGINAL DRAFT + PURPOSE
  → VOICE / QUALITY / ACCESSIBILITY CHECK
  → FACT & LINK REVIEW
  → HUMAN APPROVAL OF EXACT REVISION AND DESTINATION
  → OPTIONAL PLATFORM-SPECIFIC EDITION
  → MANUAL COPY / PERMITTED AUTHORISED PUBLISH
  → RECORD ACTUAL URL + MEASURE / CORRECT
```

Record explicit states: `CAPTURED`, `RESEARCHING`, `DRAFT`, `FACT_CHECKED`, `NEEDS_HUMAN_REVIEW`, `APPROVED`, `SCHEDULED`, `PUBLISHED`, `MEASURED`, `ARCHIVED`; also `DUPLICATE`, `NO_POST`, `REJECTED`, `BLOCKED`, `EXPIRED`, `CORRECTION_REQUIRED`.

Approval is bound to the **exact revision, content, media rights, selected destination and time window**. If the content changes materially, require reapproval. Scheduled time never implies authorisation. An edited or revoked approval must stop pending publication. Keep actual publication status separate from merely queued/approved status; never invent successful post URLs.

## 4. Features to carry forward (all proposals, not installed code)

### P1. Source-first idea inbox and near-duplicate guard
- Save `source_url`, original creator/publisher, original post/platform, screenshot or note provenance, origin date if known, date found, category/pillar, rights status, evidence needed and a single clear proposed takeaway.
- Detect repeated URLs/content ideas across the user's archives, current `knowledge/`, the two collection libraries and previous drafts. Flag similarity for human review, do not delete unrelated material automatically.
- Distinguish `social inspiration` from `permission to reproduce`. Add sources and explanatory notes without copying full paid articles, transcripts, course slides or media.

### P2. Authentic editorial profile and subject lanes
- A voluntary voice/style card describing the real author, purpose, subject pillars, sentence rhythm, audiences, tone, and what must never be implied (invented customers, fake “we achieved X”, invented first-person anecdotes, fabricated testimonials or engagement).
- Retain genuine technical, local/history, knowledge-checking and creative lanes without using personal secrets or inferring political views.
- A post has **one principal purpose**. Optional Thalia humour is a seasoning, not a quota. It must not turn source uncertainty into a punchline.
- Use `Aletheia LinkedIn Check` as the first compatibility target; review actual files before implementation.

### P3. Reader question and useful original writing
- Start from real observed questions, relevant firsthand experience, user-approved project developments and verifiable external documents.
- Lightweight brief: who is this for, what do they need to do, which real source supports it, why now, what is the original contribution, and why should it exist as a post rather than only a knowledge card?
- “Follower personas” can be illustrative editorial thinking; never invent actual audience demographics, sensitive traits, testimonials or follower motivations as facts.
- Suggested accessible structure: **specific opening → direct answer or useful result → evidence/example → practical step → caveat/source → optional question**. No promise that a hook formula causes reach.

### P4. Source and claim checking
- Use Aletheia evidence statuses: verified with context / source assertion / plausible-unverified / conflicting / unsupported / not checked. Preserve source title, publisher, URL, original language where relevant, checked date, change history and any author connection to the material.
- Re-check changing product, legal, medical, price or recruitment statements from appropriate official/primary sources before release.
- Check each destination is really the intended resource. A free guide, completion certificate, paid function and signup/upsell are different labels.
- Protect original source links from affiliate conversion tagging. Separate **Ad** links, books/gifts and editorial recommendations. No invented endorsements.

### P5. Editorial/calendar view
- A task-oriented view for ideas, research, draft, fact check, human approval, scheduled/manual handoff, published and measured. Due dates are prompts, not instructions to generate filler.
- Optional related assets: media permission, alt text, image dimensions, caption, source link, OG description, canonical HTML URL and publisher name.
- Retain a correction log and easy `NO_POST`/pause state. GitHub/Markdown remains canonical; Notion or another UI may be a *view*, not an obligatory paid database.

### P6. One parent item, optional channel editions
- The same `content_id` can have LinkedIn, newsletter, website, Instagram, YouTube or other *reviewed* format variants with their own length, heading, media, alt text, relevant outbound links and publication status.
- Do not assume that a social calendar is itself a multi-platform publishing API or that permitted posting/DM abilities are interchangeable.
- Only authorised integrations or manual copy/schedule handoff. No unsolicited DMs, fake social interactions or unattended mass posting.

### P7. Publisher quality gate
Ask, on every draft: Is the original creator identified? What does the reader actually learn? Does the post merely recycle a link? Are the sources accessible and relevant? Have claims been checked? Are outcomes/testimonials real and permissioned? Does it sound recognisably human? Is it new relative to recent output? Are image rights/alt text handled? Is the destination known? Is there an approval receipt?

Block or flag: source-only marketing, manufactured urgency, copied paid material, generic list churn, invented metrics, false quotes, unsupported “best”/growth promises, repeated links/posts, and inexplicable AI verbosity. **A documented NO POST is a feature.**

### P8. Real measurement and correction
- Keep actual publication URL, date, platform, approved revision and observed metrics *with date and population*, where lawfully available.
- Prefer meaningful replies, helpful questions, source corrections, reader task use and real page referral to follower-count mythology.
- Record author effort and error corrections; measure time savings against an observed baseline rather than copying a seller's `100+ hours/month` claim.
- If a fact changes, amend source Markdown and the affected edition, preserving provenance and correction history.

### P9. Useful content-collection publishing support
- Approved source collections (e.g. 7-video or 12-guide) have individual static, titled, linkable HTML pages and one shared place in their **existing** folder manifests.
- Capture original curator, original platform, exact original URL/source ID, individual content links and dates/limits. Aletheia exercises, FAQ and cross-topic knowledge are original companion content, not a source transcript.
- Optional seasonal resource books and gifts must be independent, disclosed, edition/URL verified and not obscure free originals.
- JSON manifests are maintained on *publication or material metadata change*, with a reviewed update of the corresponding human `index.html`. A future aggregated “Social Media” view reads these manifests, without URL migrations.

### P10. Free-first, portable and locally testable
- Start with a Markdown brief, source receipts and a simple register before a polished app or paid connector.
- Can export an approved post, short excerpt, image/alt text, source links and publication checklist. Records should survive a change of AI platform.
- Any future app must be justified by real benefits such as visual state, comparison, calendar and evidence/history. Don't make a button-heavy wrapper around a prompt.

## 5. Suggested portable data contract (future, not created)

```yaml
content_id: AL-PUB-0001
origin_platform: linkedin
origin_url: https://example.org/actual-source
origin_creator: Verified source or UNKNOWN
source_receipts: []
primary_question: One real reader question
pillar: research
audience: broad description, not inferred personal profile
purpose: one real learning or action outcome
rights_status: REVIEW
evidence_status: NEEDS_RESEARCH
draft_revision: 1
content_status: DRAFT
human_approval:
  state: NOT_GRANTED
  approved_revision: null
  approved_destinations: []
editions: []
published_receipts: []
metrics_status: NOT_MEASURED
```

Possible future source layout (only after implementation approval):

```text
publisher/
  publisher-profile.md
  ideas.md
  register.csv
  posts/<content-id>.md
  editions/<content-id>-linkedin.md
  reviews/<content-id>.md
```

**Do not create or deploy these directories merely by reading this proposal.** Link to existing `knowledge/`, `youtube/` and `linkedin/` instead of copying all their content into the publisher.

## 6. Acceptance tests before any Publisher rollout

1. A known duplicate Sabrina/Chris source is correctly flagged while retaining the original collection's provenance.
2. A helpful original project observation becomes a source-backed draft; a vague generic hook ends in `NO_POST`.
3. Unverified testimonial, follower number and invented case study are flagged rather than adopted as personal achievements.
4. Draft with a third-party graphic or confidential/project data is held for rights/privacy review; never sent to public AI without authorisation.
5. Edited text after approval reopens review, and blocked/pending drafts cannot be published merely on a calendar event.
6. Publisher can export manually usable LinkedIn copy, original source credits and optional link preview without requiring a paid app.
7. Published receipt stores the *real resulting URL*, not just the intended URL or a fabricated engagement estimate.
8. A corrected fact updates canonical knowledge and affected edition without deleting the earlier evidence receipt.
9. `youtube/index.json` and `linkedin/index.json` enumerate their existing independently named pages and preserve source-platform distinctions; folder `index.html` stays readable without JS.
10. Any future cross-library Social Media hub reads existing manifests and preserves all established share URLs.

## 7. Tasks / scope / non-goals

**Now (AK-096 and AK-097):** retain separate folders; create and check their JSON catalogues; record this consolidated idea, cross-reference previous Maistro and Creator OS lessons and existing Aletheia LinkedIn Check/Improve. Do not move old URLs.

**Later, only after explicit development approval:** inspect the actual LinkedIn Check files, agree on real content schema/author voice, prototype Markdown-only stages and test the synthetic workflows above. Decide whether a shared publisher UI, manual copy output or lawful provider integration adds value.

**Excluded without separate approval:** a subscription to Creator OS/Maistro/Notion, cloning a commercial template, unattended posting, scraping LinkedIn profiles, bulk DMs, automatic follower growth, invented first-person proof, moving the social folder pages, or adding a public Publisher HTML app.

## Source trail and handover

- Original existing idea: root `aletheia-knowledge-ideas.md` / “Back-burner idea: Aletheia LinkedIn Publisher”.
- Source-traced Creator OS lessons and ten original knowledge cards: [knowledge/aletheia-creator-os-content-system.md](../knowledge/aletheia-creator-os-content-system.md).
- Earlier twelve-resource source receipts: [knowledge/aletheia-12-free-ai-guides.md](../knowledge/aletheia-12-free-ai-guides.md).
- Existing collection page specs: `youtube/aletheia-7-videos-7-skills-page.md` and `linkedin/aletheia-12-free-ai-guides-page.md`.
- Read `README.md`, `aletheia-knowledge-GUI.md`, `aletheia-knowledge-code.md`, `aletheia-knowledge-tasks.md` and the *actual current existing app files* before coding. GitHub is the shared text master. Document tests, blocked source access and any live deployment uncertainty.

This is a proposal and original analysis. It is not a claim that the Creator OS course, template, or a Publisher app was purchased, inspected or built.
