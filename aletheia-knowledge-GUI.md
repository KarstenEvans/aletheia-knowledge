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
    + declared assets / local data
```

The `*-page.md` convention is the **target build contract** for each page. Some existing HTML pages predate these specifications; create and reconcile their specifications before a major rebuild. An HTML page is the deployed rendition, but do not discard a working behaviour merely because a newly written specification overlooked it. Update the source documents and the rendition together after review.

Knowledge Markdown is **not** an HTML build specification. A page-specific MD records layout, exact user interactions, dependencies, outbound links, assets, error handling and acceptance tests. Common behaviours belong in the two root shared guides, not copied into every page.

Use Markdown as canonical content, local browser features where appropriate, and static HTML/CSS/JavaScript for the interface. GitHub Pages is the public host; Cloudflare AI, search and Workers are optional enhancements, never foundation bricks.

## 3. Standard page order

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
