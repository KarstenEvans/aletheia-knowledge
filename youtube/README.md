# Aletheia Knowledge / YouTube Library

A library of independently linkable HTML entries. **Folder = library; descriptive HTML title and stable filename = entry.**

- [Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) governs provenance, evidence, uncertainties and human review.
- [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md) is optional and does not replace evidence.

## Public URLs
- [Library entrance](https://karstenevans.github.io/aletheia-knowledge/youtube/) → `youtube/index.html`.
- [7 Videos. 7 Skills.](https://karstenevans.github.io/aletheia-knowledge/youtube/aletheia-7-videos-7-skills.htm) → `youtube/aletheia-7-videos-7-skills.htm`.

## Rules
1. Every entry is a self-contained readable HTML file under `youtube/`, with a descriptive versionless slug, title, metadata, canonical URL and crawlable main text and link anchors. JavaScript may enhance task progress or animation but must never be required to render the core video cards.
2. `index.html` is the explicitly maintained human-readable library index, and **`index.json` is the maintained machine-readable catalogue**. Both must list every reviewed published collection consistently; GitHub Pages does **not automatically generate a directory listing** or extract `<title>` tags. Add the new entry's display title, descriptive filename, exact canonical URL, original source platform and curator to both. See AK-096.
3. Collection provenance is stored alongside each entry: source post platform, original post URL/ID, curator, creator names where verified, original video IDs/URLs and timestamps. One video can appear in multiple independently credited collections.
4. Reference original YouTube videos and preview thumbnails by URL only; no local rehosting, duplicated transcripts or misattributed creator statements. Editorial summaries and tasks must be distinguishable from video content. Fallback text if thumbnail unavailable.
5. Human approval required before publishing or modifying another collection; show status and check date and separate checked evidence from unchecked editorial summaries.
6. Cross-link Aletheia Knowledge, keep any books and gifts optional and separated from free source videos, disclose affiliate ID `18254`, add Awin MasterTag `3182162` exactly once, and exclude source and Bookshop links from Awin conversion.
7. Include local-browser accessibility, reduced motion for decorative stars, keyboard-friendly tasks, meaningful headings, small-screen layout, and stable source buttons.
8. For each entry, maintain an adjacent `*-page.md` page specification. Add library index link and root Knowledge navigation. Check direct page availability, title/metadata/structured data and mobile rendering after deployment.

The YouTube **library subject** is linked media, not necessarily the platform of the original recommendation. Sabrina Ramonov's first seven-link recommendation originated on Instagram and links to YouTube; retain this distinction in the JSON metadata. Preserve direct URLs. A possible future virtual Social Media hub may combine this file with `../linkedin/index.json` without relocating pages.

## Future task

AK-092: import a curator's seven-, eight- or eleven-link list into a draft with link receipts, deduplication and verification, then produce one reviewed static entry and update this index. This is a folder-based library, not an unattended scraper/publisher.
