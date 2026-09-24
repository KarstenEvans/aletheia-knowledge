# Aletheia Knowledge root index

**Rendition:** `index.html`

## Purpose
Public front door for the Aletheia Knowledge GitHub Pages site.

## Current collection cards
- Aletheia AI Knowledge
- Secret Windows
- Waste to Garden
- Weird History
- Swindon Town
- Music
- Windows Debloat Tool (related Secret Windows entry)

## AI route
- **AI KNOWLEDGE** → `app/aletheia-ai-knowledge.htm`
- Canonical source: `knowledge/aletheia-ai-knowledge.md`
- Explicit static collection inventory: `knowledge/knowledge.json`

## Music routes
- **CATCHPHRASES** → `app/aletheia-song-catchphrases.htm`
- **ARTISTS** → `app/aletheia-music.htm`

Do not link ordinary visitors to GitHub folders or raw Markdown as the primary action.

## Behaviour
- Mobile-first responsive card grid.
- Each card has meaningful explanatory text.
- Existing popup behaviour for links is preserved until the cross-page popup task is deliberately reconciled.
- Existing Awin MasterTag remains once near the end of the page.
- Add future subject shelves only after they have a useful public route.
- Keep `knowledge/knowledge.json` as a machine-readable inventory, but do not make the human-facing homepage depend on runtime GitHub folder enumeration or a cloud AI service.

## Future navigation
A compact burger/subject menu may become useful when several true subject shelves exist (for example Music, Health, Pets). Do not hide the current simple collection grid prematurely.

## Acceptance
- No broken primary links.
- No horizontal scrolling on phone width.
- AI Knowledge and Music app links open published HTML.
- Existing collections remain unchanged.
- The homepage remains usable if the JSON manifest is unavailable.
