# Aletheia AI Knowledge app

**Status:** CURRENT / NEW BUILD  
**Canonical published URL:** https://karstenevans.github.io/aletheia-knowledge/app/aletheia-ai-knowledge.htm  
**Rendered file:** app/aletheia-ai-knowledge.htm  
**Knowledge source:** knowledge/aletheia-ai-knowledge.md  
**Resource page:** NONE at first release

## Purpose

Provide a fast, mobile-first reader for the provider-neutral Aletheia AI capability library. A visitor should learn the useful answer on the card before needing MORE or WEB SEARCH.

## Page-specific source of truth and dependencies

Read before changing:

1. README.md
2. aletheia-knowledge-GUI.md
3. aletheia-knowledge-code.md
4. aletheia-knowledge-tasks.md
5. this file
6. knowledge/aletheia-ai-knowledge.md
7. the current app HTML

Canonical facts remain in the Markdown. The browser app fetches and renders them.

## Actual page order

1. Aletheia AI Knowledge identity and short purpose.
2. Links back to Aletheia Knowledge home and the canonical Aletheia Protocol.
3. Sticky search/filter toolbar.
4. Provider/topic filter and Jump to Card.
5. Search result count/status.
6. Responsive card grid.
7. Footer explaining evidence labels and live-search behaviour.

## Required controls and behaviour

- SEARCH: title, summary, full card and metadata.
- FILTER: All, Aletheia, ChatGPT/OpenAI, Gemini, Claude, DeepSeek, Odysseus, Cross-provider.
- JUMP TO CARD: generated from the loaded card inventory; selecting one narrows to that card and opens MORE.
- SURPRISE ME: chooses a real card, displays it and opens MORE.
- MORE/LESS: MORE renders the full stored card, including limitations and sources, without exposing raw Markdown tokens.
- WEB SEARCH: opens an ordinary Google query for the card title plus "AI" in the existing approximately 900 × 760 secondary popup on capable desktop browsers, with normal-tab fallback.
- Home and protocol links are ordinary navigation; do not intercept the home link with a popup.
- No affiliate code is required on this knowledge reader.

## Parsing contract

Visible cards use:

    ## AI-NNN | Title
    ### Summary
    substantive summary text
    **Type:** ...
    **Evidence:** ...
    **Last checked:** YYYY-MM-DD
    ### Details
    ...
    ### Sources
    - https://...

The app must:
- parse every AI-NNN card;
- take Summary from the explicit Summary section, never invent a generic preview;
- preserve Type, Evidence and Last checked for labels;
- keep all Details and Sources available under MORE;
- classify provider from ID ranges and/or type metadata;
- ignore title/introduction/research-queue material that is not an AI-NNN card.

## Data and source links

Canonical fetch: ../knowledge/aletheia-ai-knowledge.md

The Markdown's normal source URLs remain evidence links and must not be converted into affiliate links.

There is no separate resource page in the first release. The app itself contains the relevant official sources inside each expanded card.

## Visual/UX

- Mobile-first.
- Calm technology accent, readable white cards and dark text.
- Provider filters remain understandable text, not colour-only categories.
- No horizontal scrolling at phone width.
- Sticky controls must not obscure the opened card.
- Respect reduced motion.
- Result count before diagnostics.
- A card must contain useful information before MORE.

## External services

The canonical reader requires only static GitHub Pages plus the Markdown file.

WEB SEARCH is optional enhancement. If popups are blocked it opens as a normal new tab.

No AI API, Cloudflare AI, vector database or provider login is required to read the stored knowledge.

## Acceptance tests

1. Every AI-NNN heading in canonical Markdown becomes exactly one card.
2. Every card has a non-empty substantive Summary.
3. Search finds terms from title, Summary, Details, Type and provider.
4. Provider filters work independently and together with search.
5. Jump to Card selects the intended card and opens MORE.
6. SURPRISE ME produces a real card and opens MORE.
7. MORE renders headings, lists, emphasis and clickable HTTPS source links without literal Markdown markers.
8. Home returns to ../index.html in the same browsing context.
9. Android-width layout has no horizontal scroll.
10. If Markdown fetch fails, show an actionable error rather than empty cards.
11. No source link is rewritten to a merchant/affiliate destination.

## Change log

2026-09-24: initial specification created with the first Aletheia AI Knowledge library.
