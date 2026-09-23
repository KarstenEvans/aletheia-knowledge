# Aletheia Knowledge code, prompts and implementation patterns

> **Purpose:** Reusable instructions for any AI or developer editing Aletheia Knowledge. This is a **build-time code and prompt handbook**, not a runtime-loaded dependency.
>
> **Priority:** Read `aletheia-knowledge-GUI.md`, this file, `aletheia-knowledge-tasks.md`, the relevant page specification, and the CURRENT repository files before changing code. Do not regenerate a working page from an incomplete prompt.
>
> **Authority:** Canonical content lives in `knowledge/*.md`. Page-specific specifications live beside their HTML renditions. This guide describes cross-page implementation rules and repeatable prompts. When code and documentation disagree, inspect the actual implementation, preserve working behaviour, then reconcile the documents and change deliberately.

## 1. Paths and generated files

```text
Repository: KarstenEvans/aletheia-knowledge
Branch: main (verify before committing)
Public root: https://karstenevans.github.io/aletheia-knowledge/

README.md
index.html
index-page.md                             # target page specification
aletheia-knowledge-GUI.md                 # appearance and interactions
aletheia-knowledge-code.md                # this file
aletheia-knowledge-tasks.md               # work and handover
app/<slug>.htm                            # browser app
app/<slug>-page.md                        # target app build specification
knowledge/<slug>.md                       # canonical knowledge, NOT generated
resources/<slug>-rsc.htm                  # resources/merchant HTML
resources/<slug>-rsc-page.md              # target resource build specification
resources/downloads/                      # relevant downloadable assets
```

Current collections include `aletheia-secret-windows`, `aletheia-waste-to-garden`, `aletheia-weird-history` and `aletheia-swindon-town`. The main index also presents the Windows Debloat Tool as a related entry to Secret Windows. Inspect the actual index before modifying any navigation.

`*-page.md` files are a **new target convention**; missing files must be created from the actual working HTML, not pretended to exist. A new page must acquire its page spec when it is created.

The public URL must be `.github.io/aletheia-knowledge/` or a direct published app/resource route. Do not return a GitHub source/document link in place of the website.

## 2. The page-specific build specification template

For `index-page.md`, `app/<slug>-page.md`, or `resources/<slug>-rsc-page.md`, use and complete this structure:

```md
# PAGE TITLE: canonical build specification

Status: CURRENT / DRAFT / NEEDS RECONCILIATION
Canonical published URL: [exact GitHub Pages URL]
Rendered file: [exact repository-relative HTML path]
Knowledge source: [path, or NONE]
Resource page: [path, or NONE]
Purpose: [what the visitor can actually do]

## Page-specific source of truth and dependencies
[GUI, code, tasks, knowledge, assets, existing components and any live local copy]

## Actual page order
[All major sections, in on-screen order]

## Required controls and their exact behaviour
[Search; filters; Jump to Card; Surprise Me; MORE/LESS; home; local MD,
 offline/cache/update; links; popups; download; disclosures, as applicable]

## Parsing contract
[ID syntax, headings, metadata, preview/summary field, full-body sections,
 what to exclude from visible cards, fallback and parse errors]

## Data and source links
[Actual paths, source requirements and backlink/status rules]

## Visual/UX exceptions
[Theme, mobile behaviour, accessibility, any deliberately unique components]

## External services and affiliate behaviour
[Optional features and what happens when disabled, resource-page disclosure]

## Exact acceptance tests
[Tests derived from this page's current features and known failure cases]

## Change log / unresolved issues
[Date, change, task reference and test status]
```

Never replace a specific page spec with a generic template during later edits. A page can declare exceptions, but must say why.

## 3. Collection formats: read them instead of guessing

Current Markdown formats **differ**; do not impose a universal parser in one unreviewed sweep.

| Collection | Existing card headings / preview | Notes |
| --- | --- | --- |
| Secret Windows | `## SW-... | Title`, `### Summary` | Windows version, lifecycle, risk, command safety and source labels matter. |
| Weird History | `## WH-... | Title`, `### Summary` | Keep context, original sourcing and evidence labels. |
| Waste to Garden | `## WTG-... | Title`, `### Summary` | Other sections include How, Technical, Pros, Caveats and Sources. |
| Swindon Town | `## N. Topic`, then `**Card preview:** ...` | Its separate `## 30.` block contains eight extra `### CARD:` fact cards. Exclude editorial/research/index sections only as the current page spec states. |

**Every visible card must have a meaningful preview in the Markdown.** In existing content, headings or metadata may precede body text; extracting everything before the first `###` is not a reliable preview strategy. Never hide that bug with "Read the full card with MORE." If a schema lacks a summary, add a concise verified introduction to the canonical Markdown and update the parser intentionally.

Card rendering must avoid swallowing source URLs, turning source references into advertisements, showing raw Markdown tokens, duplicating intro text excessively or promoting an open research lead to a verified fact.

## 4. Safe reader implementation patterns

These examples are **patterns**. Reuse or factor the code already in the relevant page; they are not a command to replace working parsers.

### Canonical Markdown fetch

```js
const libraryPath = "../knowledge/<slug>.md";

async function loadKnowledge() {
  const response = await fetch(libraryPath, { cache: "no-store" });
  if (!response.ok) throw new Error("Knowledge unavailable (HTTP " + response.status + ")");
  const md = await response.text();
  const cards = parseCollection(md); // Collection-specific, reviewed parser
  if (!cards.length) throw new Error("No knowledge cards were found");
  return cards;
}
```

Replace the angle-bracket placeholder before publishing. On `file://`, a browser may block relative `fetch`; a local file picker or local HTTP server is a **deliberate fallback**, not an excuse to pretend direct file loading always works.

Waste to Garden already has additional browser storage, local file import/export and update checks. Do not strip these features during a shared-code refactor or incorrectly claim the other readers all have them.

### Preview and MORE separation

```js
// One parsed card (adapt fields to the collection):
{
  id: "COLLECTION-ID-001",
  title: "Specific, informative title",
  preview: "The actual fact or practical finding, with a necessary qualification.",
  bodyMarkdown: "### Explanation\n... \n### Sources\n- https://example.org/source",
  evidenceStatus: "VERIFIED_WITH_CONTEXT"
}
```

Validation rules: every displayed card gets its actual introduction; `MORE` reveals the complete explanation, limitations and clickable sources; `LESS` collapses that content without clearing the search; `SURPRISE ME` reveals a real introductory paragraph. Don't reduce the page to a grid of headlines or copy a single generic preview to all cards.

### Render Markdown as Markdown

Use a well-reviewed renderer or a tightly scoped, tested Markdown subset appropriate to the actual files. Escape untrusted text before creating HTML; strictly control allowed link protocols; don't inject unchecked Markdown straight into `innerHTML`. Preserve paragraphs, `###` headings, numbered/bulleted lists, emphasis, fenced code and links used in the collection. If a small custom parser cannot handle nested lists or links safely, test and improve it rather than letting visible raw syntax reach users.

Links to real sources must remain clickable. Preserve normal `https:` references, not automatic merchant conversions. On re-render, do not attach duplicate click handlers to the same controls.

### Source and status display

Show the concise useful finding first. Put technical metadata, longer caveats, sources, last-checked dates and background in MORE where that improves readability, **without hiding a safety-critical qualification**. Version-sensitive claims require a supported version/last-reviewed label; open leads need a clear unverified label.

Do not copy source prose wholesale. Summarise independently, distinguish established facts from interpretations and preserve provenance in the canonical Markdown.

## 5. Browser links and one popup helper

The current site commonly uses a separate approximately 900 × 760 resizable, scrollable window for secondary/external links. Keep it optional on mobile and protect downloads. One click must open no more than one destination.

```js
function openKnowledgeWindow(url) {
  const width = Math.min(900, screen.availWidth || 900);
  const height = Math.min(760, screen.availHeight || 760);
  const left = Math.max(0, Math.round(((screen.availWidth || width) - width) / 2));
  const top = Math.max(0, Math.round(((screen.availHeight || height) - height) / 2));
  return window.open(url, "_blank",
    "width=" + width + ",height=" + height +
    ",left=" + left + ",top=" + top +
    ",resizable=yes,scrollbars=yes,toolbar=yes,location=yes");
}
```

Bind **one** delegated handler, only to intentionally secondary/external links. Let a normal `target="_blank"` link work if a popup is blocked. Exclude anchors, `mailto:`, `tel:`, downloads and ordinary in-page navigation. Do not blanket-intercept every link **and** also intercept the same link through a separate button handler. Where clipboard/AI popups are used, open from the original click before async work.

Suggested public navigation links:

```html
<a href="../index.html">Aletheia Knowledge</a>
<a href="../resources/<slug>-rsc.htm">Resources</a>
```

Use relative paths only after confirming the HTML's actual folder. The site URL is also suitable for share buttons and responses to the owner.

## 6. HTML shell, SEO and resource-page MasterTag

A new standalone app should at least have valid HTML5, `lang="en-GB"`, viewport, unique title/description, visible main content, one main heading, labelled search, accessible buttons and its published canonical URL when appropriate. Do not cargo-cult a full Swindon.org.uk site header into every portable knowledge app.

Simple resource-page shell:

```html
<!doctype html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>COLLECTION Resources | Aletheia Knowledge</title>
  <meta name="description" content="ACTUAL DESCRIPTION">
</head>
<body>
  <header><!-- knowledge-app link and useful introduction --></header>
  <main id="main"><!-- free resources first; commercial offers disclosed --></main>
  <footer><!-- Home · Resources · Privacy · Affiliate Disclosure where applicable --></footer>
  <!-- Only on pages deliberately carrying affiliate-capable commercial links: -->
  <script src="https://www.dwin2.com/pub.3182162.min.js"></script>
</body>
</html>
```

This is a **build template**, not a request to add MasterTag to every Markdown/reader. In existing repository resources and the homepage, inspect whether the tag is already present before changing anything. Use it **once, before `</body>`**, not in `footer.html`. Keep plain factual citation links and explicitly attributed Bookshop.org links out of Convert-a-Link according to the site's `data-awinignore` convention, and verify the conversion rules against actual Awin behaviour before assuming they are guaranteed. Put a visible affiliate disclosure near commercial content; the MasterTag is not a disclosure.

Do not embed affiliate tags in `knowledge/*.md`, convert scholarly sources, or use a merchant link as the only citation. The HTML resource page may include its own books/gifts/tools and a link back to the running knowledge app.

## 7. Shared ready-to-paste AI prompts

Prompts are **procedures**, not evidence. The receiving AI must read actual repository files and verify new facts itself.

### Prompt A: bootstrap a new AI/chat

```text
Work on KarstenEvans/aletheia-knowledge, current main branch.
Before answering or editing, read the current README.md and the three root guides:
aletheia-knowledge-GUI.md, aletheia-knowledge-code.md,
aletheia-knowledge-tasks.md.
For this task read the actual collection knowledge Markdown, app HTML,
resource HTML and any matching *-page.md.
Use GitHub as the shared canonical source; reconcile newer/local edits.
Keep Markdown knowledge portable; GitHub Pages serves the visitor-facing site.
Do not send me raw GitHub files when I request a link to the library:
use https://karstenevans.github.io/aletheia-knowledge/ or its live app route.
Carry out the requested task first, test relevant features, then update the
task log with what changed, evidence, commit(s) and what remains unverified.
If an essential file cannot be accessed, say so rather than inventing it.
```

### Prompt B: add a research-backed knowledge card

```text
Read the current collection schema, index and relevant nearby cards.
Extract candidate claims from the supplied discovery material without copying
the author's prose. Check each factual claim against appropriate primary or
reliable independent sources, including date/version/scope when necessary.
Mark uncertainty and keep research leads separate from verified claims.
Give every new visible card a stable ID, meaningful title and a substantive
preview/Summary in canonical Markdown. Add a full explanation, limitations,
source URLs, status and appropriate resource backlink only where published.
Do not alter evidence decisions to fit affiliate links.
Check the existing app parser can display every new card before committing.
Update any relevant page spec and aletheia-knowledge-tasks.md.
```

### Prompt C: build or update a browser page

```text
Read the root GUI/code/tasks guides, current HTML, matching page spec and
declared knowledge/assets. If there is no *-page.md, reverse-engineer the
current working HTML into one BEFORE a major rewrite. Preserve all documented
and actually working features. Update the page spec for accepted changes.
Make the smallest appropriate HTML/CSS/JS change; don't duplicate common code.
Knowledge cards must show meaningful information before MORE, and MORE must
render formatted detail and clickable sources. Keep mobile usability, search,
filters, navigation, resources, accessibility and popup fallback intact.
Keep runtime optional services optional. Test the page with the real Markdown,
report any failure or deployment uncertainty, then log the work in tasks.
```

### Prompt D: audit or repair empty cards

```text
Load the current actual knowledge Markdown and the app parser.
Enumerate all cards the app is intended to display. For each card, assert that
its visible introduction is substantive, factually qualified where needed,
non-duplicated, and not a placeholder or metadata-only string.
Test cards beginning with a ### subheading and cards with links, bullets,
fenced code and sources. Click/open MORE and verify formatting and clickable
source URLs. Add missing previews to the canonical Markdown, not a separate
JavaScript patch list. Test search and Surprise Me again. Keep the entire
editorial backlog out of the public fact-card grid unless intentionally shown.
Record parsed/visible counts and any intentionally excluded sections.
```

### Prompt E: verify a page before publishing

```text
Compare the current *-page.md and actual HTML with root GUI/code guides.
Check URLs point to GitHub Pages for visitors, not /blob/ Markdown.
Test the actual canonical Markdown and all visible cards; show previews,
MORE, search, filters/Jump if present, Surprise Me if present, sources,
working resource links, keyboard focus, Android-width layout and no overflow.
Test popup fallback and ensure one external click opens one destination.
Check offline/local behaviour only for apps that actually implement it.
Check resource-page affiliate disclosure and one MasterTag where appropriate,
and that factual sources are not affiliate-converted. Do not claim live
deployment was verified unless it actually was. Update tasks with results.
```

## 8. Operational test checklist

- Count actual source cards and compare with app-rendered cards; **do not hard-code one collection's count into another**.
- No empty/placeholder previews; no editorial or unverified text shown as a verified fact.
- Title and introduction explain something *before* MORE; MORE displays the appropriate full card and valid source links.
- Search finds title/body/tag matches, returns a clear no-results state, and does not erase data. Test keyboard and mobile.
- All links resolve relative to the real published page; visitor-facing Knowledge links open the web reader, never raw Markdown.
- No surprising destructive commands, unsupervised AI publishing or secret keys in static client code.
- Track test status separately: code inspection, parser/unit test, browser/mobile test, live GitHub Pages check. One is not proof of the others.
- Re-fetch SHA before a GitHub update; use normal history/commits, no blind forced overwrite. One task's code edit should not silently delete another task's feature.

## 9. Reusable snippets versus deployed code

The examples above are **not** shared assets being fetched at runtime today. Existing apps contain collection-specific CSS/JS; standardising popup, Markdown rendering or cards into actual shared files is a future task, subject to testing and preserving offline/portable use. Avoid introducing bundlers, paid APIs, Cloudflare dependencies or complicated frameworks for a problem that static HTML and Markdown already solve.

## 10. Storyteller Markdown and camera prompt (cross-repository)

The executable Storyteller is in **`KarstenEvans/aletheia-app`**, not in this knowledge repository. Read the current root `aletheia-storyteller.htm`, `aletheia-storyteller.md` and `aletheia-storyteller-page.md`, then `stories/stories.json` and the exact target `.md` and illustration files **directly from GitHub before editing**. When an anticipated file is absent, identify what is missing and ask for or plan the original artwork rather than inventing a file path.

Its published app link is:
https://karstenevans.github.io/aletheia-app/aletheia-storyteller.htm

### Literal story and image tags

Put commands on their own lines inside the narrative Markdown. The image path is relative to the selected story's directory and must match a confirmed filename on GitHub.

```text
[image;Toomorrow-Mystery-in-the-Abandoned-Mechanics-Hall.webp;tm=29,22,2.2;aipi=41,31,2.5;schrodinger=67,62,2.4]
[wide;dur=1.7]

The old lift opened on an unfamiliar floor.

[zoom;schrodinger;dur=2.3]

The cat was already waiting.

[pan;aipi;dur=2.0]

AI-PI checked the sign.

[hold;1.0]
[wide;dur=2.0]
```

Image focus values `name=x%,y%,preferredZoom` are **estimated against each particular image**. Use the actual published image to verify named character positions. `zoom` centres a named hotspot and uses its preferred zoom; `pan` moves toward the named hotspot at approximately the current zoom; `wide` returns to the whole image; `hold` waits before the next spoken cue. Duration is in seconds. These commands already exist in the app; do not describe planned `fade`, `sound` or `quiz` tags as implemented.

### Biography include grammar

Independent biography files are named `stories/bio-ToomorrowMan.md`, `bio-AI-PI.md`, `bio-Schrodinger.md`, `bio-Elsie.md` and `bio-Prudence.md`. They are selectable as ordinary story entries under `type: "bio"` in the explicit manifest. Inside another story, optional **inline inclusion** uses:

```text
[bio-ToomorrowMan.md]
```

The requested alternate spelling `[bio-TomorrowMan.md]` is a supported alias for the canonical two-o filename. The include loads and narrates the other Markdown *including its image and camera cues* at that exact location. Do not insert it into an existing long story merely because the bio file exists. Keep MP3/VTT narration limited to stories whose speech-cue timing is known to match; dynamic bio inclusion defaults to browser TTS.

Security and portability rule: accept only a plain `bio-*.md` name from the selected story's own directory, not `../`, external URLs or arbitrary user-controlled paths. Check for missing files, include cycles and excessive expansion. A static website cannot automatically enumerate all GitHub folder entries: every new published `.md` story/bio must be entered into `stories/stories.json`. User-selected OPEN FOLDER is the separate local enumeration route.

### Ready-to-paste prompt F: write an illustrated Storyteller biography

```text
Work in the current KarstenEvans/aletheia-app main branch.
Fetch the real aletheia-storyteller.htm, aletheia-storyteller.md,
aletheia-storyteller-page.md, stories/stories.json, original story Markdown,
and exact proposed image files from GitHub before editing. Do not rely on
files mentioned in another chat if they are missing from the repository.

Write an original, concise, narratable bio as stories/bio-CHARACTER.md.
Preserve the original story's established canon. Clearly distinguish new
fictional extensions from facts about an external public figure or channel.
Use one confirmed illustration for an opening [image;...] tag. Add only
verified image-specific hotspots and [zoom], [pan], [wide], [hold] camera
commands at meaningful narrative beats. Avoid placing long narrative text
inside a command tag.

Add the standalone bio to stories/stories.json as type "bio", and verify it
appears in Storyteller's visible, searchable story index. Implement a literal
[bio-CHARACTER.md] inline include only when asked to place it in a host story;
a new biography must not silently lengthen the first adventure. For any
missing image, name it exactly and ask about the original asset or record a
pending dedicated portrait, rather than saying it has been published.

Test the parsed cue count, every referenced image filename, hotspot names,
direct ?story=bio-... link and safe optional include. Update the Storyteller
page spec and relevant shared task/handover record. Give the user a
.github.io app URL as the primary result, not a raw GitHub .md file.
```

### Example manifest entry and URL

```json
{
  "file": "stories/bio-Schrodinger.md",
  "title": "BIO: Schrödinger the Dragonfold",
  "type": "bio"
}
```

Public deep link:
https://karstenevans.github.io/aletheia-app/aletheia-storyteller.htm?story=bio-Schrodinger

The first adventure currently depicts ToomorrowMan as a human, and AI-PI as a floating robot; alternate Robot PI branding should not silently retcon the characters. Verify original artwork before designing new portraits. The existing YouTube channel link for ToomorrowMan was supplied by the project owner, but channel contents must be independently inspected before treating them as biographical evidence.
