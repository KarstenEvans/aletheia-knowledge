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
