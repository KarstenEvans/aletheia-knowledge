# Aletheia Knowledge GUI

> **Purpose:** One portable design and behaviour contract for every Aletheia Knowledge browser page, regardless of which AI, computer or editor works on it.
>
> **Rule:** KISS unless a feature genuinely improves the result. **Useful knowledge comes first.** Markdown is the memory; the website is its readable front door.
>
> **Status:** Shared working specification. Check the current repository files before changing an existing page.

## 0. Start here in every new AI conversation

Read these root files **from the current GitHub default branch**, not from a previous chat or an old local download:

1. `README.md` and `aletheia-knowledge-GUI.md` (this file).
2. `aletheia-knowledge-code.md` for shared behaviours and reusable build prompts.
3. `aletheia-knowledge-tasks.md` to avoid duplicating, losing or contradicting work.
4. The relevant page's `*-page.md` build specification, once created.
5. The current `knowledge/<collection>.md`, `app/<collection>.htm` and `resources/<collection>-rsc.htm` as relevant.

Do not assume every collection uses the same Markdown schema or JavaScript parser. Read the actual files, compare with this contract, and preserve working features before editing.

**Canonical GitHub source:** `KarstenEvans/aletheia-knowledge`; branch `main` at the time of this specification. Re-fetch immediately before any write. Do not overwrite newer or local-only work. For collaboration, state what was read, what changed and what still needs testing. Where the same file has been changed concurrently, reconcile the diff rather than forcing a replacement.

## 1. Public website, not a GitHub file viewer

**The visitor-facing library entry point is:**

https://karstenevans.github.io/aletheia-knowledge/

It serves the repository's `index.html`. Direct visitor links go to published Pages apps, for example:

- Secret Windows: https://karstenevans.github.io/aletheia-knowledge/app/aletheia-secret-windows.htm
- Waste to Garden: https://karstenevans.github.io/aletheia-knowledge/app/aletheia-waste-to-garden.htm
- Weird History: https://karstenevans.github.io/aletheia-knowledge/app/aletheia-weird-history.htm
- Swindon Town: https://karstenevans.github.io/aletheia-knowledge/app/aletheia-swindon-town.htm

**When giving the owner or visitors a link to Knowledge, use the public `.github.io` website or its relevant app page.** Do not substitute GitHub `/blob/`, `/tree/`, `raw.githubusercontent.com`, an unpublished HTML file, or the canonical `.md` file. Source links may be offered separately for developers. Do not add tracking parameters to our own site links without a reason.

The planned/mirrored Swindon.org.uk resource links are not automatically live just because they appear in metadata. Test a destination before publishing it as a working link.

## 2. Source-to-page architecture

```text
ROOT: aletheia-knowledge-GUI.md
    + aletheia-knowledge-code.md
    + aletheia-knowledge-tasks.md
    + index-page.md                      → index.html
    + app/<slug>-page.md                 → app/<slug>.htm
    + resources/<slug>-rsc-page.md       → resources/<slug>-rsc.htm
    + knowledge/<slug>.md                → portable facts/cards, loaded by app
    + knowledge/knowledge.json             → explicit static inventory of published collections
    + declared assets / local data
```

The `*-page.md` convention is the **target build contract** for each page. Some existing HTML pages predate these specifications; create and reconcile their specifications before a major rebuild. An HTML page is the deployed rendition, but do not discard a working behaviour merely because a newly written specification overlooked it. Update the source documents and the rendition together after review.

Knowledge Markdown is **not** an HTML build specification. A page-specific MD records layout, exact user interactions, dependencies, outbound links, assets, error handling and acceptance tests. Common behaviours belong in the two root shared guides, not copied into every page.

Use Markdown as canonical content, local browser features where appropriate, and static HTML/CSS/JavaScript for the interface. GitHub Pages is the public host; Cloudflare AI, search and Workers are optional enhancements, never foundation bricks.

## 3. Standard page order

On static hosting, do not pretend a browser can enumerate the repository's knowledge folder. `knowledge/knowledge.json` is the explicit machine-readable inventory for tools that need discovery; keep the visible home page independently usable as a simple static front door.

**Library home, `index.html`:** clear title and one-line purpose; immediate collection choices with meaningful descriptions; optional supporting links; discreet footer. Every collection must lead to a working published app and, where present, a resource page.

**Knowledge app, `app/*.htm`:**

1. Page identity and simple link back to the library homepage.
2. One primary search or task control and immediately useful results.
3. Small, understandable filters or Jump to Card where useful.
4. Cards showing the actual knowledge, not a placeholder or instruction.
5. A MORE/LESS disclosure for deeper information, explanation, limitations and sources.
6. Secondary RESOURCES and WEB SEARCH actions where appropriate.
7. Footer and unobtrusive disclosures.

**Resource page, `resources/*-rsc.htm`:** purpose and link back to the working knowledge app; relevant free resources and source material; clearly labelled books/tools/gifts or other commercial offers; relevant affiliate disclosure; quiet navigation/footer. Do not move advertisements above the useful answer.

The exact page composition can vary by subject: gardening's HAVE/WANT tabs need not be imposed on Weird History, and Windows risk badges do not belong on a Roman-history card.

## 4. The card contract: no blank introductions

Every visible card must have:

- a stable ID or stable collection-relative identity and a meaningful title;
- an immediately readable introduction with at least one real, useful piece of information;
- a MORE control for the longer original explanation and source links;
- a visible distinction between verified facts, interpretations, open leads or caution when relevant;
- a functioning resources link when the collection has a published resource page.

**Never show** "Read the full card with MORE", generic filler, raw metadata, a heading with no explanation, or a card that exists only to direct the reader elsewhere.

Do not mistake a `###` subheading for a blank section. When the source uses subheadings at the top, give that card a real `Card preview` (Swindon) or `### Summary` (the schema used by other collections). Keep previews in the canonical Markdown rather than hard-coded into the reader. Show enough information to satisfy a quick read; do not arbitrarily cut a crucial qualifying sentence.

**MORE means more:** formatted headings, lists, paragraphs, source links and qualifications. Do not display literal `###`, `**bold**` or a giant unformatted text dump. Links must be clickable. LESS restores the short card without losing the active search.

Keep sources with the appropriate claim/card; link directly to primary documentation or reliable original research when available. Do not attach unverified claims to a source simply because it discusses the topic.

## 5. Mobile-first visual rules

- Build for an Android-size screen first, then widen gracefully for desktop.
- Responsive card grids; no horizontal page scroll; readable minimum tap targets; sensible line lengths.
- One primary search field per page. A sticky search/filter toolbar is welcome if it does not obscure the top of an opened card.
- Comfortable white or light panels, dark text, rounded cards/buttons and space between actions.
- Use the collection's existing accent: Secret Windows teal, Waste to Garden green, Weird History warm brown, Swindon Town muted teal. Do not flatten every app to one colour or redesign working pages without a task.
- Primary actions use the page accent and clear text; secondary actions are pale/white with an outline.
- Search results before counters, help, advertisements, diagnostics, platform status or AI extras.
- Keyboard focus visible; meaningful form labels; `aria-expanded` on disclosures; announcements for loading/errors.
- Respect reduced-motion preferences. Never rely on colour alone to express evidence or risk.

## Browser capability and enhancement rules

Knowledge readers should remain useful when an optional browser capability fails.

- Feature-detect the capability actually needed; do not infer support from operating-system name.
- Build readable HTML/card content first, then enhance it with sticky controls, popups, local file APIs, graphics or AI.
- If a library/CDN/browser API fails, show an actionable fallback rather than a blank control/surface.
- When an app uses WebGL/Three.js or another graphics layer, Safari/WebKit must be tested by renderer/context capability, not categorically disabled as "Apple unsupported".
- Record STATIC, LOCAL BROWSER, DEVICE and LIVE tests separately.
- Long-running AI/agent maintenance must save durable checkpoints/results so a provider quota interruption does not force the whole research/build to restart.

## 6. Search, discovery and expansion

- Search currently loaded local/cached knowledge first. Search title, preview, full card body and useful tags.
- Search results change in place; do not navigate to a raw Markdown document.
- Filters and Jump to Card must use the same card inventory and remain usable after a search.
- SURPRISE ME selects a real card and shows its informative introduction immediately. It should not require a user to open MORE just to learn anything.
- Preserve the current selection/scroll context when opening and closing details. A home/top button may assist long collections.
- If knowledge cannot load, show a clear actionable message and any available local-file loader, not an empty grid or a fabricated answer.
- Do not report cached cards as freshly verified.

## 7. Link and window behaviour

Use ordinary, accessible links with useful anchor text. Primary home/library navigation must reliably reach the published website.

The existing Aletheia/Swindon pattern opens **secondary resources, source links and external searches** in a separate, approximately **900 × 760**, resizable and scrollable window on capable desktop browsers, leaving the current task underneath. On Android or when popups are blocked, a normal new tab is an acceptable fallback; do not create two windows for one click. Download links, anchor links and `mailto:`/`tel:` keep their intended behaviour.

Implement the popup behaviour once per page (and eventually as one shared helper), not once for buttons and again for all links. Create popups synchronously from the user click when browser activation is required. A new page must not quietly break back navigation on phones.

Keep source links and ordinary reference links non-commercial; never allow the affiliate converter to rewrite evidence citations.

## 8. Resources, backlinks and affiliate separation

The reusable collection loop is:

```text
Aletheia Knowledge home → knowledge app ↔ resources page
                                 ↓
                     source-traced Markdown library
```

The Markdown must remain useful when copied into another AI or indexed by a third party. Give it a plain-text `resource_url` or equivalent backlink **only after the destination exists**. An AI/agent reusing a card should preserve or append the appropriate published resources link when technically possible; do not substitute a merchant affiliate URL for the source.

Put books, gifts and affiliate-ready merchant links in resource HTML, not in factual card content. Pages that deliberately carry relevant merchant links use the existing **Awin Publisher MasterTag** (publisher `3182162`) **once, near `</body>`**, not inside a visible footer fragment. The current project uses `data-awinignore` for links that must retain attribution or avoid conversion where supported; verify actual converter behaviour. Make page-level affiliate disclosures clear near commercial material and maintain an Affiliate Disclosure link.

Commercial relationships must never affect knowledge evidence labels, rankings of evidence or the wording of factual claims. Resource pages may also point to relevant Bookshop.org lists and free materials.

## 9. Rebuild protection

Before editing or regenerating a page, inspect the deployed HTML, canonical Markdown and any existing page spec. Inventory working features: search, filters, Jump to Card, Surprise Me, details, resource/web actions, popups, mobile layout, local file/offline controls, metadata, footer and MasterTag. **Only retain controls actually present or required by the page specification.** Do not promise an unimplemented feature as though it exists.

For substantial changes, write the page-specific `*-page.md` first, update shared guides if the behaviour is common, make the smallest HTML change needed, and test. A change made in one app does not silently propagate to the others; log cross-collection follow-up in `aletheia-knowledge-tasks.md`.

## 10. Reconstruction/acceptance test

In a fresh AI session, the current repository and these documents must suffice to reconstruct the page without hunting through old chats. A rebuilt page fails if it loses a required feature, shows placeholder cards, displays literal Markdown, misroutes resource links, points a visitor at GitHub source instead of Pages, breaks mobile controls, or depends on a paid service for ordinary card reading.

**One-line test:** a visitor opens a card, learns something immediately, and can choose MORE for the evidence.

## Storyteller and cinematic story pages (cross-repository convention)

Storyteller itself lives in a **different GitHub repository**, `KarstenEvans/aletheia-app`, at the repository root. Before writing or rebuilding it, read its actual `aletheia-storyteller.htm`, `aletheia-storyteller.md`, `aletheia-storyteller-page.md`, `stories/stories.json` and any current story/artwork being edited. Treat the app's own page specification as authoritative for its cinematic exceptions.

**Visitor-facing app:** https://karstenevans.github.io/aletheia-app/aletheia-storyteller.htm . This must open the runnable HTML, not the GitHub repository browser or a raw `.md` story.

Its GUI intentionally differs from ordinary Knowledge cards: full-screen image stage, unobtrusive transport controls, lower-third readable captions and an upper-right menu. The **initial screen must show a searchable library of stories and biographies**, not start speaking the first story before the reader has selected it. The index is driven by the explicit `stories/stories.json` manifest on static GitHub Pages, not by pretending a web page can list a server folder.

The reader selects one complete Markdown story. Each story may contain square-bracket camera directives that load an image and move between named image hotspots via smooth zoom, pan, wide and hold commands. Keep image text legible, contrast behind captions, unobstructed mobile controls and a reasonable reduced-motion fallback. Source image coordinates are image-specific percentages: test actual artwork, not assumed coordinates.

Every character biography is itself a selectable **BIO** story with a meaningful opening, illustration and narration. Optional inclusion inside another story is explicit via a standalone `[bio-ToomorrowMan.md]` line; Storyteller resolves the file from the same `stories/` folder and narrates it at that point. Do **not** automatically append all character bios to an existing story; expanding a bio also brings in its own image and camera commands. For current details, see the app repo's `aletheia-storyteller.md` and `aletheia-storyteller-page.md`.

Five biographies were added in September 2026: ToomorrowMan, AI-PI, Schrödinger, Elsie Brake and P.R.U.D.E.N.C.E. Before referencing a previously generated picture, verify the exact file is actually in GitHub. As last checked on 23 September, the main story references four missing image filenames, and dedicated Elsie and Prudence portraits have not been verified. Do not present a shared scene illustration as a character portrait without disclosure. Reconcile original assets before a full cinematic release.


### Storyteller voice-cast and quiet-caption contract (23 September 2026)

Narration now has two parallel roles. The **app's selected voice** reads every heading, unquoted narrative passage and unattributed quote. A story-specific `[voice:AI-PI]` or `[voice:TM]` selects the character who reads subsequent text **inside paired double quotation marks** only; text outside them stays with the narrator automatically. A new `[voice:...]` changes the actor; `[voice:]` clears the actor. The runtime must not guess from punctuation or search a full biography for every line.

The first adventure has six `[voice-profile;NAME;lang=...]` declarations at its very beginning, with optional matching/fallback, rate and pitch. Profiles select voices already installed on the device. Thai, Egyptian Arabic, Japanese and English voices vary across Android and desktop browsers; gender labels are only best-effort. If an appropriate voice is absent, fall back to the configured name or to the user-selected narrator. For a story narrated in a different language, the owner simply chooses another **narrator** from the app's existing dropdown; actor profiles remain separate.

Default caption display is now **one spoken sentence/cue**, adjustable to two, three or off. The still-image pans and zooms remain deliberately gentle for low-intensity storytelling. The heading reader does not insert “New title” or a spoken “pause”: it reads the heading as written, then waits silently for 400 ms. An optional *bilingual learning captions* concept is documented in the app repository's `ideas.md`, not presented as an implemented feature.

To prevent accidental overwrites, fetch the exact GitHub source and save a byte-equivalent copy before a substantial app rewrite. The pre-voice Storyteller original lives at `KarstenEvans/aletheia-app/backup/aletheia-storyteller-before-character-voices-20260923.htm`. A self-contained local voice-test file was created before publishing the changes; a complete offline story bundle remains a separate task. New AI sessions should read the app's updated `aletheia-storyteller-page.md` before altering this behaviour.
