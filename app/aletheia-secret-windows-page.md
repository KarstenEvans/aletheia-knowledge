# Aletheia Secret Windows reader — page specification

Status: CURRENT SOURCE / LIVE BROWSER CHECK PENDING
Reviewed: 2026-09-23
Rendered file: `app/aletheia-secret-windows.htm`
Canonical knowledge: `knowledge/aletheia-secret-windows.md`
Resource page: `resources/aletheia-secret-windows-rsc.htm`
Standalone AI guide: `resources/aletheia-chatgpt-free-guide.htm`
Source guide: `knowledge/aletheia-chatgpt-free-guide.md`
Public URL: https://karstenevans.github.io/aletheia-knowledge/app/aletheia-secret-windows.htm

## Exact source / working hierarchy

Read the repository README and root GUI, code and task guides, then the **current** HTML and canonical Markdown. Keep the working reader rather than replacing it with a generic card template. The page is a static HTML/CSS/JS client: it first loads `../knowledge/aletheia-secret-windows.md`, then falls back to the matching public GitHub raw URL. No account, paid AI, API, database or Cloudflare Worker is needed to use ordinary cards. Direct `file://` use may be restricted by browser fetch security.

## Current visible page order and controls

1. Title, search and SURPRISE ME.
2. Sticky category tabs: ALL; UPDATE / DRIVERS; DEBLOAT / SECURITY; REPAIR / RECOVERY; CMD / POWERSHELL; NETWORK; SERVER; WEB / CHROME; **AI / CHATGPT**.
3. Jump to Card selector, populated from the loaded Markdown.
4. Reader notice, resources / Windows Debloat / raw source / repository links.
5. 'AI without the faff' short introduction with links to the public ChatGPT Free guide and Aletheia AI Easy setup.
6. Search note, load/result status, responsive knowledge card grid and footer.

Cards display a stable ID, evidence/status/risk badges when provided, applicability, an informative Summary, MORE / LESS expandable detail, and source links. Search automatically resets the active tab to ALL; Jump opens the card and scrolls to it; Surprise Me samples the active category. Keep the established teal theme, keyboard-focus controls and mobile layout. Secondary links use the existing one-popup-on-desktop / new-tab-fallback pattern; never bind a second popup handler to the same link.

## Exact collection-specific parse contract

A card starts with `## SW-PREFIX-000 | Meaningful title`. The reader parses `### Summary` (or `### Claim` / `### Why useful` fallback), evidence/risk/status/lifecycle fields and `### Sources` URL bullets. NEW: `SW-AI-###` belongs to group `AI`. All 18 current AI cards have `### Summary` and original official provider sources. The guide article `knowledge/aletheia-chatgpt-free-guide.md` is a separate Markdown document, **not** a set of Secret Windows cards; do not make the card parser swallow its article headings.

Current parser renders only whitelisted detail headings and simple Markdown-like bold, code and line breaks. Improve only with a tested formatter that does not break existing multiline cards or clickable source links. Literal two-character `\\n` sequences in the reader's JS handler previously caused a syntax error and were corrected on 23 September 2026. Add a JavaScript syntax regression check before every deployment.

## AI content and accuracy exceptions

ChatGPT Free product capabilities and limits are time-sensitive; maintain LAST_CHECKED and primary help sources on SW-AI-001..018. Distinguish documented capabilities from Aletheia methods. Do not call plain-language prompt recipes built-in commands or imply EXECUTE/TRUTH forces truth or tool use. Live Voice can do web search and use memory where enabled; the recommendation to use editable Dictation plus normal text for research is workflow advice, not a claim Voice is incapable. Custom Instructions, Memory and Projects have separate persistence and privacy boundaries.

## Acceptance tests

- Parse the **actual current Markdown**, assert all intended cards render and all SW-AI-001..018 cards have an informative Summary and clickable primary source.
- Syntax-check both real `<script>` blocks; no literal escaped-newline regressions or duplicate event handlers.
- Activate AI / CHATGPT; only the 11 AI cards should appear. Search AI terms while another category is selected and confirm automatic ALL reset.
- Check Jump to Card, SURPRISE ME, MORE/LESS, risk badges, source links, sticky toolbar, responsive card sizes and keyboard focus.
- Guide, AI Easy, Resources and Knowledge links must open the **working public page**, not an unhelpful GitHub source viewer. Do not claim live tested until Android and desktop checks.
- Keep affiliate tags off canonical knowledge and off the non-commercial AI guide.

## Change log

2026-09-23: Added AI / CHATGPT tab, short AI paragraph, 18 checked cards and a companion public ChatGPT Free guide. Repaired pre-existing literal escaped line breaks in the search input's event handler. Source-level cards, links and JavaScript syntax validated. GitHub Pages behaviour on the owner's PC/Android still requires confirmation.

## OpenAI eight-guide audit (23 September 2026)

Additional verified topics now include Free GPT usage and 500 MB Library; 1,500-character Custom Instructions on Free; Project memory, instructions and sharing boundaries; Memory sources and full removal; Live/Advanced/Standard voice distinctions and Dictation retention; web search privacy; and separate Data controls. The companion public HTML guide was regenerated from its canonical Markdown after this audit. Static parser/script validation passed with 131 total Windows cards and 18 AI cards. Live desktop/mobile checking remains open.
