# Aletheia Money Saving reader: canonical build and test specification

Status: INITIAL READER SOURCE COMMITTED; LIVE GITHUB PAGES / REAL DEVICE TEST PENDING
Canonical public URL: https://karstenevans.github.io/aletheia-knowledge/app/aletheia-mse-money-saving.htm
Rendered file: app/aletheia-mse-money-saving.htm
Knowledge source: knowledge/aletheia-mse-money-saving.md
Source receipt file: knowledge/aletheia-mse-money-saving-sources.json
Resource page: NONE (links go straight to original sources)
Related task: AK-MSE-001

## Purpose and scope
Provide a free, static, provider-agnostic knowledge interface across 48 independently written UK money-saving cards. Original 39 cards used MSE topics and links; nine further cards use public Reddit/MSE forum discussions as leads and checked authoritative references. Independent content only; no MSE logos, article duplication, endorsement, copied forum text or YouTube sources.

## Sources of truth
Read `aletheia-knowledge-GUI.md`, `aletheia-knowledge-code.md`, `aletheia-knowledge-tasks.md`, current source Markdown and this build specification before changing app. The canonical content lives in Markdown and is not hardcoded into HTML.

## On-screen order
1. Title, original-content/unaffiliated disclaimer and clear navigation to Knowledge home, libraries, MSE and downloadable source.
2. Search box, single-select category filter populated from the Markdown, My actions toggle, reset button and local Markdown picker.
3. Count/result/status and responsive knowledge cards with title, category, summary and **Try this** actionable information visible before MORE.
4. Original or verified guidance link; MORE / SOURCES expands important limitations and all source links, explicitly marking community leads.
5. Footer with privacy and copyright policies, source index, canonical Markdown and protocols.

## Parsing
Parse only `## MSE-### | Title` headings. Each card reads independent `### Summary`, `### What to do`, `### Limits and watch-outs`, `### Metadata` and `### Sources` sections. Category comes from the exact `- **Category:**` line. Source links are parsed from Markdown `- Label: https://...` lines. Prefer an independently checked guidance link over a community link as the principal action. Do not turn intro/editorial sections into cards. Escape Markdown content and validate external link protocols before HTML insertion. Render no Markdown-derived scripts.

## Functional controls
- Search title, category, summary, action, caveat and ID without external APIs.
- Category filter counts all cards and works with search and action filter.
- My actions is a checkbox per card and one browser-local `localStorage` set of stable card IDs. Do not collect bank details, use analytics or send checklist to a server. Storage failure remains a working per-tab state.
- Copy my action list uses browser clipboard after user action; when blocked it displays text for manual copying.
- Open local Markdown picker reads only a user-selected file, without scanning device storage; online canonical fetch uses the relative repository URL.
- Existing links open the publisher/official source in a regular new tab, without forced popup.
- Reset filters clears search/category/My actions filter, not the underlying saved checklist.
- Preserve functional usability without any AI-specific service, payment or key.

## Safety and maintenance
- 48 cards and 11 categories initially; content grows from Markdown, without hard-coded numeric limits.
- No personalised financial recommendations. Recheck dynamic rates, benefits, country-specific laws and offers at source.
- Forum anecdotes are **unverified discovery leads**, not primary evidence. No inaccessible Discord content is asserted.
- Screenreader role=status, button labels, visible keyboard focus, reduced-motion support, mobile one-column layout.
- No Awin script is needed for this non-commercial reader and no affiliate links are embedded.

## Acceptance tests
- [ ] File exists on GitHub main and GitHub Pages serves 200 status after deployment.
- [ ] Exact parser loads all current 48 unique MSE IDs and 11 unique categories; every card has a visible summary, action, main authoritative external URL and MORE text.
- [ ] Search, category, reset and My actions work together on a browser.
- [ ] Saved checklist survives a same-browser reload when permitted; optional no-storage mode works.
- [ ] Copy action list and manual fallback function.
- [ ] Local user-selected Markdown file loads without a GitHub request.
- [ ] Broken online path produces a clear error and manual load route.
- [ ] External links are valid and community references remain distinguished from independent checks.
- [ ] Keyboard focus/contrast, 360-pixel mobile viewport, desktop layout, no horizontal overflow and no injected markup.
- [ ] Root and Knowledge folder links use published HTML as primary entry; reader and source index appear in explicit manifest.
- [ ] No YouTube research used, no MSE article copying, no provider-specific AI dependency.

## Change history
- 2026-10-13: initial independent 48-card reader created with static plain HTML/CSS/JS. Structural/runtime testing and Pages availability to be recorded separately in the task register.
