# Aletheia Music app

**Rendition:** `app/aletheia-music.htm`  
**Canonical shelf:** `knowledge/music/`

## Purpose
Provide the public browser reader for the Aletheia Music shelf. Visitors choose an artist/songwriter and read the canonical Markdown without being sent to GitHub's file viewer.

## Current artist files
- Tears for Fears
- Roland Orzabal
- Beatles
- David Bowie
- Bob Marley
- Sex Pistols

## Behaviour
- Mobile-first artist grid.
- Search artist names/descriptions.
- Artist selection loads its current canonical Markdown from `../knowledge/music/`.
- Query parameter `?artist=<slug>` deep-links an artist.
- Render headings, paragraphs, lists, tables, emphasis and links; do not show raw Markdown markup.
- Clear routes to Aletheia Knowledge, the Music shelf and Song Catchphrases.
- External links open separately; internal navigation remains normal.
- No full copyrighted lyrics are embedded by the app.

## Acceptance
1. Default page shows informative artist cards.
2. Search filters the artist grid.
3. Every artist card opens a readable rendered knowledge page.
4. Browser back returns from an artist to the shelf view.
5. Android width has no horizontal scrolling.
6. Deep links work for each current artist.
