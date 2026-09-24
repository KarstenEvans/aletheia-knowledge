# Aletheia Knowledge

Structured, source-traced knowledge libraries and lightweight browser apps for Aletheia. Evidence-checked, vendor-neutral and usable online or locally.

## START HERE: multi-AI collaboration

- **Public knowledge website:** https://karstenevans.github.io/aletheia-knowledge/ . Send visitors here or to a published app page, not to the raw `.md` or GitHub file viewer.
- **[GUI and behaviour contract](aletheia-knowledge-GUI.md):** layout, mobile use, substantive card previews, MORE, links and resources.
- **[Common code and reusable prompts](aletheia-knowledge-code.md):** HTML patterns, safe parsing, page-spec template and fresh-chat work prompts.
- **[Shared task register](aletheia-knowledge-tasks.md):** handover, active work, verification and follow-up.

Before editing, read those three guides **and** the current target Markdown/HTML. Every HTML page should have a matching `*-page.md` build specification (see the task register for legacy pages still awaiting theirs). The GitHub source is shared master; reconcile more recent local edits rather than overwriting them. Canonical facts live in `knowledge/`; the runnable website lives on GitHub Pages.


## Repository structure

- `app/` — lightweight `.htm` interfaces.
- `knowledge/` — Markdown knowledge libraries.
- `knowledge/knowledge.json` — explicit machine-readable inventory of published collections; the static site must not pretend it can enumerate a GitHub folder at runtime.
- `resources/` — resource / book / gift pages linked from the apps.

## Current app

### Aletheia Waste to Garden

- App: `app/aletheia-waste-to-garden.htm`
- Knowledge: `knowledge/aletheia-waste-to-garden.md`
- Resources: `resources/aletheia-waste-to-garden-rsc.htm`

The app loads its Markdown library from `../knowledge/` when hosted. It also supports **LOAD .MD LOCALLY** for offline use or local testing.

## Knowledge libraries

### Aletheia AI Knowledge

- Public app: https://karstenevans.github.io/aletheia-knowledge/app/aletheia-ai-knowledge.htm
- Knowledge: `knowledge/aletheia-ai-knowledge.md`
- Scope: current AI capabilities and practical workflows across ChatGPT/OpenAI, Google Gemini, Claude/Anthropic, DeepSeek, Odysseus and the provider-neutral Aletheia/Thalia layers.
- Method: primary product documentation for capability facts; community reports are explicitly labelled as field notes; time-sensitive claims carry a last-checked date.
- Design: useful information lives in each card before MORE or WEB SEARCH. Live search refreshes changing facts rather than substituting for stored knowledge.
- Discovery: `knowledge/knowledge.json` gives static tools and future apps an explicit collection inventory without making the library depend on GitHub API folder listing.


### Aletheia Weird History

- Knowledge: `knowledge/aletheia-weird-history.md`
- Discovery sources: *Stick a Flag in It*, selected *Horrible Histories* books, and *All About History: Book of Weird History*.
- Status: curated library with a published GitHub Pages reader and resource page.
- Method: books provide topic discovery only. Claims are independently checked, source-traced, context-qualified and stored as self-contained retrieval cards.
- Portable design: stable IDs, plain Markdown metadata, evidence/confidence fields, review dates and a normal resource backlink. Cloudflare AI Search or other retrieval services may add capabilities, but are optional.
- Resources: `resources/aletheia-weird-history-rsc.htm`

### Aletheia Windows Debloat Tool

- Public tool: https://karstenevans.github.io/aletheia-app/aletheia-windows-debloat/aletheia-windows-debloat.htm
- Role: read-only planning front end while the earlier Windows Rescue V1.0 scripts await an Aletheia Improve pass.
- Linked knowledge: `knowledge/aletheia-secret-windows.md`

### Aletheia Secret Windows

- Knowledge: knowledge/aletheia-secret-windows.md
- Scope: Windows 7 legacy context, Windows 10/11, supported Windows Server, CMD, PowerShell, repair/recovery, networking, safe debloat, administration, Chrome and a small web-admin crossover.
- Discovery sources: supplied Windows command, Server, PowerShell and beginner guides are used as topic maps only.
- Status: curated library with a GitHub Pages knowledge reader and live resource page. Check the current Markdown front matter for its version.
- Method: every time-sensitive or version-sensitive claim is independently checked against current primary documentation and tagged for lifecycle/risk.
- Safety design: read/observe first, reversible changes before destructive ones, no blind service/AppX/registry debloat scripts.

## Knowledge approach

Sources can include books, scientific papers, public guidance and reputable websites. Copyrighted books are used for topic discovery and provenance, not copied into the repository. Aletheia knowledge cards are independently written, checked and updated.

The canonical knowledge is plain Markdown and must not depend on a particular AI, cloud service, database or affiliate network. Optional services may index, search or distribute it. Resource pages may contain clearly disclosed affiliate links, while the knowledge cards themselves contain only ordinary backlinks.

## Planned licence model

- `/app/`: GNU GPL v3 or later
- `/knowledge/` and original resource content: CC BY-NC-SA 4.0
- Third-party source material remains the copyright of its respective owners.


## Offline/local-first behaviour

Aletheia Waste to Garden now:
- loads a stored browser copy of the knowledge library first when available;
- falls back to the repository-relative Markdown file and then the public GitHub raw file;
- can store the current knowledge library in browser storage for offline use;
- can save a separate `.md` file using the browser's save picker/download behaviour;
- can reload a local `.md` file manually and remembers it for later sessions;
- checks the GitHub copy when online and reports when it differs;
- provides a section-aware `JUMP TO CARD` selector in addition to search and card browsing.

Browser security does not allow a webpage to silently scan a user's Downloads folder or write beside the `.htm` file. The app therefore uses browser storage for automatic local-first loading and a user-selected file save for portable backups.
