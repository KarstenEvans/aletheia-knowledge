# Aletheia Knowledge

Structured, source-traced knowledge libraries and lightweight browser apps for Aletheia. Evidence-checked and usable online or locally.

## Repository structure

- `app/` — lightweight `.htm` interfaces.
- `knowledge/` — Markdown knowledge libraries.
- `resources/` — resource / book / gift pages linked from the apps.

## Current app

### Aletheia Waste to Garden

- App: `app/aletheia-waste-to-garden.htm`
- Knowledge: `knowledge/aletheia-waste-to-garden.md`
- Resources: `resources/aletheia-waste-to-garden-rsc.htm`

The app loads its Markdown library from `../knowledge/` when hosted. It also supports **LOAD .MD LOCALLY** for offline use or local testing.

## Knowledge approach

Sources can include books, scientific papers, public guidance and reputable websites. Copyrighted books are used for topic discovery and provenance, not copied into the repository. Aletheia knowledge cards are independently written, checked and updated.

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
