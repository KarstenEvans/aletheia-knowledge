# Aletheia Music index page

**Rendition:** `knowledge/music/index.html`  
**Canonical shelf map:** `knowledge/music/index.md`

## Purpose

Provide a simple public browser front door for the Music knowledge shelf at:

`https://karstenevans.github.io/aletheia-knowledge/knowledge/music/`

The folder URL must resolve directly to this `index.html`, rather than sending ordinary visitors to a GitHub folder listing or raw Markdown.

## Current contents

Cards for:
- Song Catchphrases
- Tears for Fears
- The Beatles
- David Bowie
- Bob Marley
- Roland Orzabal

The current artist/catchphrase material exists as canonical Markdown only. Until dedicated browser readers exist, any GitHub links must be explicitly labelled **SOURCE MD**, never presented as the main visitor experience.

## Behaviour

- Mobile-first responsive card grid.
- Clear route back to the Aletheia Knowledge public root.
- No affiliate conversion or MasterTag required on this index.
- No full copyrighted lyrics.
- Keep descriptions substantive rather than placeholder text.

## Future migration

When `app/aletheia-music.htm` exists, change artist/catchphrase actions to visitor-facing HTML views and leave source Markdown as secondary developer/source links.

A future root subject/burger menu may link to this shelf or its eventual app. Do not build empty subject shelves merely for symmetry.

## Acceptance

1. Opening `/knowledge/music/` loads this page.
2. Android-size viewport has no horizontal scrolling.
3. Root Aletheia Knowledge link resolves correctly.
4. Every listed source file exists.
5. No card claims a browser reader exists when it does not.
