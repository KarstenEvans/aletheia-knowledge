# Aletheia Song Catchphrases app

**Rendition:** `app/aletheia-song-catchphrases.htm`  
**Canonical knowledge:** `knowledge/music/aletheia-song-catchphrases.md`

## Purpose
Search memorable song/album phrases across artists and expose their vibe, language mechanism, chart class and deeper Aletheia walkabout.

## Behaviour
- Fetch canonical Markdown at runtime.
- Parse the Phrase Map table as the complete card inventory.
- Parse `SC-###` detailed sections and attach them to matching phrases.
- Search phrase, artist, vibe and class.
- Artist and class filters.
- `SURPRISE ME` selects a real card and opens MORE.
- Every card has an informative preview immediately.
- MORE renders deeper source text when present; otherwise it explains the stored classification and links to artist knowledge.
- ARTIST opens `aletheia-music.htm?artist=...`.
- WEB SEARCH opens a normal web search in a separate window.
- Query parameter `?artist=...` pre-filters by artist.
- No full copyrighted lyrics.

## Acceptance
1. Card count equals the Phrase Map data rows.
2. No blank/generic preview cards.
3. Search and filters work together.
4. MORE/LESS does not expose raw Markdown syntax.
5. Beatles, Bowie, Marley, Tears for Fears and Sex Pistols filters all return cards.
6. Android width has no horizontal scrolling.
