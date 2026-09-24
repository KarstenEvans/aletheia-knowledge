# Aletheia Knowledge tasks and cross-AI handover

> **Purpose:** One visible, GitHub-backed task register so work started in one AI conversation or on one device can be continued safely in another.
>
> **Working rule:** Read `README.md`, `aletheia-knowledge-GUI.md`, `aletheia-knowledge-code.md`, this file and the specific current collection/page files before working. GitHub is the shared master, but reconcile any newer local edits rather than silently discarding them.
>
> **Last task-list update:** 2026-09-23. These are project tasks, not scheduled ChatGPT reminders.

## How to use this register

Each task should have a short ID, priority, status, scope/files, acceptance test and concise dated progress notes. Update this file in the **same work session** as accepted code/content changes, whenever possible.

Statuses: `TODO`, `IN PROGRESS`, `DONE`, `BLOCKED`, `VERIFY LIVE`. Only mark `DONE` when the relevant acceptance tests have passed; record any browser/live checks that were not possible.

Before starting: read the current GitHub file and SHA, check for overlapping `IN PROGRESS` work, record your intended scope, and change the smallest relevant files. Avoid parallel writes to the same page. After completion: note which Markdown, HTML and spec files changed; report commit IDs and tested behaviours; log any live-deployment gap.

**User-facing website:** https://karstenevans.github.io/aletheia-knowledge/ . When answering the owner with a knowledge link, give the `.github.io` front door or a published reader app, **not** a GitHub `/blob/` file.

## P0: shared memory and immediate integrity

### AK-001 | DONE | Root GUI guide

Created `aletheia-knowledge-GUI.md` in the repository root. Describes library-home/app/resource hierarchy, mobile-first design, readable main cards before MORE, popup/link rules, affiliate separation, source-of-truth and reconstruction checks.

Acceptance: exists on current GitHub `main`, is linked from this register/README and is readable in a fresh AI session.
Initial commit: `68354e2d51bc32fae6a680716f10b72953e6106d`; Markdown formatting correction: `32d75920e5a835f3e130f4505eca38cbdc8f20ef`.

### AK-002 | DONE | Root shared implementation and prompt guide

Created `aletheia-knowledge-code.md` with the actual repository layout, page-spec template, collection parser differences, safe HTML/JS patterns and five copy/paste collaboration prompts.

Acceptance: exists on current `main`, refers to the actual four collections, gives Pages rather than raw source links for visitors, and does not describe example snippets as already-installed runtime code.
Initial commit: `d8c710edb7550308b4f9c39993388a6aa9e53bfe`.

### AK-003 | DONE | Create cross-AI task register

Created this root file to track work, acceptance, testing level, changed paths, handover notes and known problems. Do not confuse `DONE` for the register itself with completion of the backlog below.

### AK-004 | DONE | Confirm root README onboarding links

Added a compact **START HERE** section to `README.md` linking the three root documents and defining the `*-page.md` convention. Updated stale descriptions of Weird History's published reader and Secret Windows' version. README remains a small entry point.

Acceptance: a fresh collaborator opening README finds GUI, code and tasks immediately and can distinguish current features from proposed work.
Commit: `d18b3bd3e0ffe1b2c765db8e80b2fc2e75f29817`.

## P0: make every HTML page reconstructable

### AK-010 | TODO | Create and reconcile page specifications

Create canonical build specs from each page's **actual current HTML** before doing substantial rewrites:

- `index-page.md` → `index.html`
- `app/aletheia-secret-windows-page.md` → `app/aletheia-secret-windows.htm`
- `app/aletheia-waste-to-garden-page.md` → `app/aletheia-waste-to-garden.htm`
- `app/aletheia-weird-history-page.md` → `app/aletheia-weird-history.htm`
- `app/aletheia-swindon-town-page.md` → `app/aletheia-swindon-town.htm`
- `resources/aletheia-secret-windows-rsc-page.md` → corresponding resource HTML
- `resources/aletheia-waste-to-garden-rsc-page.md` → corresponding resource HTML
- `resources/aletheia-weird-history-rsc-page.md` → corresponding resource HTML
- `resources/aletheia-swindon-town-rsc-page.md` → corresponding resource HTML

For every additional HTML page, create its own `*-page.md` alongside it. The root guides contain the template and common patterns. Page-specific files must describe *actual* layout, data parser, actions, dependencies, versioned/source rules, assets, special features and tests. Never erase working features to make the HTML resemble an incomplete template.

Acceptance: another AI can read only the repository documents and reconstruct every page without losing its defining behaviours.

### AK-011 | TODO | Add a non-destructive page/card regression test

A lightweight local test should load each collection's real canonical Markdown, exercise its actual parser (or an intentionally equivalent tested parser), and fail if any intended visible card has missing ID/title, blank/generic introduction, raw markup, missing required sources or duplicates. Test Markdown `###` immediately after section heading, embedded URLs, bullets, code blocks and long paragraphs. Record allowed exceptions like deliberate research/backlog sections per page.

Acceptance: test prints source/visible card counts **by collection** and exits non-zero for empty/placeholder cards; do not hard-code Swindon's historical count into every collection. Use a simple documented offline/static method, not a paid CI or Cloudflare requirement.

### AK-012 | TODO | Cross-page controls and accessible mobile test

At Android phone width and desktop: check search, filters, Jump to Card, Surprise Me, MORE/LESS, keyboard focus, source links, resources, scroll position, popup fallback, footer and download/local MD controls **only where that page actually has them**. Verify one click opens one window, no horizontal scrolling, no broken internal nav, and no missing disclosures.

Acceptance: per-page test status recorded (static/parser, browser/mobile, live Pages); issues go here with affected path and reproducible steps.

## P0: known recent Swindon card issue

### AK-020 | VERIFY LIVE | Swindon Town introductions and MORE

On 2026-09-23, Swindon Town's app and canonical Markdown were updated: 30 section cards now have substantive `**Card preview:**` text, eight additional fact cards received supporting source links, and the reader now displays formatted MORE content rather than literal Markdown. The parser was checked against the actual canonical Markdown: **38 visible cards** in that revision; each had an informative preview.

Files: `knowledge/aletheia-swindon-town.md`, `app/aletheia-swindon-town.htm`.
Known related commits from this work: knowledge `325b1c86e5788a5f793a0f6e5e79d20171a9eab6`; app `22e794264aee59d9c86c4a9f8319ca443ee6806d`.

**Still to verify:** published GitHub Pages behaviour on desktop and Android. Check a card that starts with a `###` heading, such as **Core identity**, plus longer cards, sources, Surprise Me and MORE/LESS. If a phone shows the old version, inspect live deployment/caching before changing the Markdown again. Link: https://karstenevans.github.io/aletheia-knowledge/app/aletheia-swindon-town.htm .

### AK-021 | TODO | Distinguish public knowledge from editorial scaffolding

Review which Swindon sections belong in the public card grid: research leads, source hierarchy, provenance, places-to-expand, pending identification and task/editorial notes. Keep them in canonical Markdown when useful, but give them an intentional label, display rule or separate editorial view instead of casually presenting them as historical facts.

Acceptance: verified Swindon fact cards are visibly distinct from unverified leads, subjective visitor opinion and self-documented Aletheia project provenance. Preserve the real Swindon facts and links.

## P1: preserve knowledge independence and site navigation

### AK-030 | TODO | Audit visitor-facing links

Find GitHub `/blob/`, `/tree/` and raw Markdown links used as **main Knowledge** actions across `index.html`, apps and resources. Replace those *visitor-facing actions* with working GitHub Pages reader/home links while retaining clearly labelled **Source Markdown / Developer** links where genuinely useful. The Weird History resource page currently includes a GitHub `blob` link labelled as opening the free knowledge library and should be checked first.

Acceptance: primary Knowledge buttons open published HTML readers; internal links work from their actual folders; existing source-transparency links remain clearly differentiated. Check all URLs before claiming they are live.

### AK-031 | TODO | Source-safe, common Markdown rendering

Compare Weird History, Swindon, Secret Windows and Waste to Garden readers. Identify formatting drift, literal Markdown, missing/duplicate source links or unsafe `innerHTML` paths. Extract a small shared, portable renderer only if tests show it is warranted. Do not break differing card schemas, local-file workflows or current stable renderers just to reduce lines of code.

Acceptance: MORE consistently renders headings, paragraphs, bullets, code and clickable normal-source links. User-provided/local Markdown is safely escaped/sanitised, with no script execution.

### AK-032 | TODO | Optional shared popup helper

Consolidate repeated 900 × 760 desktop popup logic after testing the existing pages. Respect touch/mobile and popup blocking, preserve downloads and ordinary primary navigation, and remove double interception. Prefer one small reusable static helper if it reduces drift; otherwise retain documented independent page code.

Acceptance: external/resource click opens one target, leaves the original page available, and has a usable Android fallback.

### AK-033 | TODO | Affiliate and canonical backlink audit

Inspect each `resources/*-rsc.htm` and the root index. Confirm the Awin MasterTag (publisher `3182162`) appears at most once on each page that intentionally uses it, just before `</body>`, and nowhere in factual Markdown. Verify commercial disclosures, `data-awinignore` behaviour for existing Bookshop.org attribution/source links and the reciprocal app ↔ resources page links.

Acceptance: facts and evidentiary sources remain independent of affiliate conversion; unverified/planned Swindon.org.uk mirror URLs are not presented as live.

### AK-034 | TODO | Inspect offline/local-first parity by actual need

Waste to Garden already has browser caching, local Markdown import/save, online update comparison and Jump to Card. Consider which of those options would genuinely benefit the other collections; do **not** claim feature parity that does not exist or force a common cloud/search platform into a static-first library.

Acceptance: current Waste to Garden workflows still work unchanged unless explicitly revised, and any new local option is added to its own page specification and tested offline.

## P1: editorial and research quality

### AK-040 | TODO | Keep collection provenance and versions accurate

For every new research card, record independently checked sources, qualifiers, publication/version context and any resource backlink. Discovery books/articles are topic maps, not automatic evidence. Recheck high-change Windows/security or visitor facts before automating publication. Correct stale version references only against current knowledge files.

Acceptance: citations support exact claims; open leads remain identified; no copied copyrighted book text; no affiliate-led evidence status.

### AK-041 | TODO | Standardise card metadata deliberately, not by destruction

Review whether optional shared fields (ID, title, preview, body, keywords, status, sources, last-checked, resource URL) are useful across the four existing Markdown collections. Propose a migration path that preserves existing IDs, content, sections, readers and human readability.

Acceptance: a fresh AI can recognise each existing format; no one-click rewrite silently strips specialist fields such as Windows risk or gardening caveats.

### AK-042 | TODO | Keep the root library index accurate

When a new collection app and/or resource page is published, add it to `index.html` and its `index-page.md`; remove outdated "not yet published" descriptions in README and other guides. Avoid dead links or adding unpublished ideas as live buttons.

Acceptance: root index remains a useful, mobile-friendly front door with working collection buttons and no raw source-file detours.

## Cross-project: Aletheia Storyteller

### AK-050 | DONE / VERIFY LIVE | Storyteller biographies, index and reusable tag conventions

The separate `KarstenEvans/aletheia-app` repository contains the actual Storyteller; this Knowledge repository contains the shared collaboration rules. Before any future change, fetch the app's current `aletheia-storyteller.htm`, `aletheia-storyteller.md`, `aletheia-storyteller-page.md`, `stories/stories.json` and the exact image/story files.

On 2026-09-23, five independently selectable fictional bio stories were created: `bio-ToomorrowMan.md`, `bio-AI-PI.md`, `bio-Schrodinger.md`, `bio-Elsie.md`, `bio-Prudence.md`. The Storyteller manifest contains the original adventure plus all five bios. The app now presents a searchable story/BIO index and supports deliberate `[bio-ToomorrowMan.md]` includes from the same story directory.

The shared `aletheia-knowledge-GUI.md` and `aletheia-knowledge-code.md` now document the distinct cinematic GUI, screenshot/asset verification discipline, hotspot camera grammar and prompt for authoring a new illustrated bio. App-specific documentation and a new `aletheia-storyteller-page.md` were committed in the app repo.

Static checks passed: app script syntax, 6 manifest items, 5 standalone bio cue counts, inline include, alternative ToomorrowMan spelling, missing include errors and circular include rejection. **A live Android/desktop playback test has not yet been completed.**

Published player: https://karstenevans.github.io/aletheia-app/aletheia-storyteller.htm

### AK-051 | TODO | Recover missing Storyteller art and verify the live player

The first story references four missing GitHub image paths: `Into-the-Forgotten-Mechanics-Institution.webp`, `Youre-Late.webp`, `The-Department-of-Applied-Impossibility.webp`, and `Guardian-of-the-Misty-Primeval-Pond.webp`. Four other story images have been verified present and reused. The Elsie and Prudence bios currently use existing setting illustrations, **not portraits of those characters**.

Ask the owner for the missing originals or agree on new character and scene artwork before changing established visuals. Do not silently substitute branding art that changes ToomorrowMan's established appearance or pretend a missing file is published.

Live acceptance: test the story/BIO index, mobile layout, deep links (e.g. `?story=bio-AI-PI`), audio start/stop, camera focus positions, image-load fallback, optional inline bio test story and local folder import. Insert biography includes into the original adventure only with explicit editorial agreement, since they change its length and camera sequence.


### AK-052 | DONE / VERIFY LIVE | Actor voices, single-sentence captions and local backup

On 2026-09-23, the actual `KarstenEvans/aletheia-app` source was fetched and inspected before any changes. An exact original was committed to `backup/aletheia-storyteller-before-character-voices-20260923.htm` (unchanged original Git blob `9b9f18d544db8ca7234dab49053e57aa882a7250`), and a local self-contained voice-test HTML was prepared before modifying the published app.

The updated app supports compact character profile definitions at the beginning of a story, persistent `[voice:Character]` for quoted dialogue only, automatic narrator voice for unquoted text, and explicit `[voice:]` reset. It falls back when foreign-language/target voices are unavailable. The first story now includes six profiles and editor-specified dialogue changes, with original prose and camera commands preserved. Default captions changed to one spoken cue; 2, 3 and Off remain available. The previously removed “New title” prefix was checked again; the silent 400-ms heading pause remains. Static parser test of the real first story yielded **634 cues** and six profiles. A build marker was added to the app menu.

Future bilingual/dual-language captioning is written as an *idea* in `aletheia-app/ideas.md` and not falsely advertised as available.

**Still to test:** live published HTML and browser TTS on the owner's PC and Android, unavailable foreign voices and fixed MP3 mode. The local downloadable zip currently includes the voice experiment and a Save Local helper; its full-repository ZIP button lets the owner download the entire current source, including the exact backup. It is not itself an offline bundle of all the site's stories and images. Record the user's playback findings and any source-file corrections before closing the live-verification part.

## Cross-collection: free AI onboarding in Secret Windows

### AK-060 | DONE / VERIFY LIVE | ChatGPT Free cards, guide and Voice-vs-Dictation advice

23 September 2026: added 18 `SW-AI-001..018` cards under a newly visible **AI / CHATGPT** category in `knowledge/aletheia-secret-windows.md`; each has an informative summary and source URL. The reader now has an AI tab and a short introductory AI paragraph linking a dedicated ChatGPT Free guide and the existing Aletheia AI Easy setup. `resources/aletheia-secret-windows-rsc.htm` also includes a concise AI section and links.

New source guide: `knowledge/aletheia-chatgpt-free-guide.md`. New visitor-facing page: `resources/aletheia-chatgpt-free-guide.htm`, pre-rendered static content with copyable instructions and primary help references. New rebuild specs: `app/aletheia-secret-windows-page.md` and `resources/aletheia-chatgpt-free-guide-page.md`.

Accuracy boundary: Live Voice **can** web-search and use memory on available experiences, but its conversation-oriented model/tool set, transcription limitations and spoken UX make editable Dictation plus ordinary text preferable for many research, table and document tasks. Shortcuts such as EXECUTE, NO FAFF, ELI5, SEARCH CURRENT and SOURCE CHECK are explicit prompt recipes, **not** built-in privileged modes. Free features and limits were checked against official OpenAI help pages on 23 September 2026.

**Source checks passed:** 131 total Secret Windows cards including all 18 AI cards; each AI card has a meaningful Summary and at least one official OpenAI source; AI category/tab and resource links are present; both current reader JavaScript blocks parse. A pre-existing literal `\\n` event-handler corruption in the reader was discovered by the syntax check and fixed, rather than shipping a new tab on an already-broken script.

**23 September 2026 follow-up:** Completed an eight-article audit of the current OpenAI Free, Voice, Dictation, Custom Instructions, Memory, Projects, Search and Data controls guides. Added SW-AI-012..018, updated the long-form source guide and regenerated its static HTML, updated the live reader's AI intro to 18 cards, and fixed its card parser to stop before the non-card research backlog. Rechecked the exact repository sources: **131 card starts, 18 AI cards, every AI card has a real Summary, official source and last-checked field**. The reader's two scripts and the standalone guide's script parse successfully. No paid dependency was added.

**Still to verify:** actual GitHub Pages deployment, desktop/Android navigation, source links, AI-tab filtering, search auto-reset, Jump to Card, SURPRISE ME, MORE/LESS, and guide's Copy Prompt fallback. Direct web inspection of the GitHub Pages URLs was unavailable from this session; do not mark browser/live tests complete.

Published routes to check:
- https://karstenevans.github.io/aletheia-knowledge/app/aletheia-secret-windows.htm
- https://karstenevans.github.io/aletheia-knowledge/resources/aletheia-chatgpt-free-guide.htm

**23 September 2026 feedback-training correction:** Verified the current OpenAI Data controls FAQ. Even when a user has switched off model improvement, voluntarily giving thumbs-up or thumbs-down response feedback may allow the *entire linked conversation* to be used for training. Added this warning to SW-AI-018, the canonical ChatGPT Free guide and its published HTML with a visible callout. The companion AI Easy setup displays the same caution. Static checks pass; public browser refresh still to be confirmed.

### AK-061 | DONE / VERIFY LIVE | Remove raw Markdown visitor buttons and add current Copilot book/topic cards

23 September 2026: The user identified the unnecessary `OPEN RAW KNOWLEDGE` (reader) and `KNOWLEDGE .MD` (resources) buttons. Both were removed from the visitor-facing HTML **without deleting the canonical Markdown or changing the reader's internal data fetch**. Kept developer repository access distinct from normal visitor navigation.

Looked up Anand Narayanaswamy's *Microsoft Copilot for Windows 11* (Apress, September 2024): publisher offers legitimate licensed EPUB/PDF and preview; OverDrive lists an ebook, but lending requires a participating library. A freely redistributable full book was not found. Its chapter list was used only for research discovery, with **eight independently worded SW-COP-001..008 cards verified against primary Microsoft documentation**. The older Skype chapter was marked historical because consumer Skype retired 6 May 2025.

Updated the reader's tab to **AI / CHATGPT / COPILOT**, mapped `SW-COP` IDs to the existing AI grouping, added a resource-page digital-book/lending section, recorded publisher provenance in the knowledge registry and reconciled the reader page spec. Created `resources/aletheia-secret-windows-rsc-page.md` to document actual visitor-facing resource behaviours and source/affiliate separation.

**Static acceptance passed:** 139 total Windows knowledge cards, including 18 ChatGPT and eight Copilot cards (26 under AI). Each new Copilot card has an informative Summary, last-checked date and primary source. Both public pages have **zero exposed raw Markdown links**, the reader's internal MD fetch remains, scripts parse, the book links are present, and the existing resource MasterTag appears once.

**VERIFY LIVE:** The GitHub Pages host could not be fetched from the available web viewer (DisabledError). Owner should confirm on PC/Android that the two unwanted MD buttons have disappeared, the AI tab shows 26 cards, Copilot search/Jump/MORE work, and the resource book links open as intended. If a browser still shows the previous build, check deploy status and cache before modifying sources again.

## Next-session handover block

When another ChatGPT or AI joins this project, start by reading the three root guides **and current target files**. Pick one task ID; announce the files you intend to change; preserve concurrent work. Do not regenerate HTML from memories of a previous chat. Source Markdown, approved shared guides and a matching page specification are the durable instructions; HTML is the rendered website. GitHub Pages is how the owner should open or share the library.

Before leaving a session, add a note directly under the task worked on:

```text
YYYY-MM-DD | Task AK-___ | STATUS
Files read:
Files changed:
Git commit(s):
Tests passed:
Not tested / still uncertain:
Next action:
```

The next person should be able to finish the next task without asking where the code, latest facts or active decisions went.


## P1: Music knowledge shelf

### AK-070 | APP PUBLISHED / VERIFY LIVE | Music shelf, catchphrase graph and future subject navigation

2026-09-24: created a dedicated canonical music shelf at `knowledge/music/` rather than adding more files to the general `knowledge/` root.

Published source files:
- `knowledge/music/index.md`
- `knowledge/music/aletheia-song-catchphrases.md`
- `knowledge/music/aletheia-tears-for-fears.md`
- `knowledge/music/aletheia-roland-orzabal.md`
- `knowledge/music/aletheia-beatles.md`
- `knowledge/music/aletheia-david-bowie.md`
- `knowledge/music/aletheia-bob-marley.md`

The music index defines the subject-shelf model: sufficiently large domains may later use subfolders such as Music, Health or Pets, each with its own internal index. Do **not** reorganise existing Knowledge collections merely to make the taxonomy look symmetrical.

Next build:
1. Create `app/aletheia-music-page.md` from the actual music knowledge structure.
2. Create `app/aletheia-music.htm` as the visitor-facing Music shelf/search page.
3. Add the Music app to the root public index only after the published app exists and works.
4. Consider a compact mobile burger/subject menu for the root library **only when enough subject shelves exist to justify it**; preserve direct card/search access and do not hide the primary task behind navigation chrome.
5. Add a dedicated resource page later for legitimate listen, lyrics, books, physical music, official merch and live links, with factual sources kept separate from affiliate conversion.

Research boundary: short lyric/catchphrase quotation only; no full copyrighted lyrics. Separate formal songwriter credit, documented intent, chart facts and Aletheia interpretation. The current Beatles/Bowie/Marley files are first-pass corpora and should deepen through primary sources rather than folklore.

Static source check on 2026-09-24: all seven paths fetched successfully from the default branch after publication.


2026-09-24 | Task AK-070 | APP PUBLISHED / VERIFY LIVE
Files read: root GUI/code/task guides; current Music index/source files; Weird History reader as implementation reference.
Files changed: `knowledge/music/index.md`, `knowledge/music/index.html`, `knowledge/music/index-page.md`, `knowledge/music/aletheia-song-catchphrases.md`, `knowledge/music/aletheia-beatles.md`, new `knowledge/music/aletheia-sex-pistols.md`, new `app/aletheia-music.htm`, new `app/aletheia-music-page.md`, new `app/aletheia-song-catchphrases.htm`, new `app/aletheia-song-catchphrases-page.md`, root `index.html`, new root `index-page.md`.
Key commits: Sex Pistols `dca40d70f76b04825fffa1d5af582ec396a146f4`; catchphrase update `e02c2f4e0dd6ce780ed4f766a45e8174b2bb16b8`; Music app `480a7b3326eec4c9d92c09857b7e52514071d915`; Catchphrases app `1585b58b9a186fd56dcfdbd4b4660831287c02d2`; root index `ecf18c71c94c88f72cab99e6c175f0e9ebf2baaa`.
Tests passed: both new inline JavaScript blocks compile via V8 `new Function`; canonical Phrase Map parses to **54 phrase rows** spanning Tears for Fears, Beatles, David Bowie/Queen & Bowie, Bob Marley and Sex Pistols; all new GitHub paths refetched successfully.
Not tested / still uncertain: GitHub Pages live deployment and Android/desktop interaction. The available web viewer could not fetch the Pages host, so do not mark live verification complete.
Next action: owner test `app/aletheia-music.htm` and `app/aletheia-song-catchphrases.htm` on Android/desktop; then continue phrase/artist research or start Aletheia Improve.
