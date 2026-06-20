# STATUS — Self-Hosting Handbook

**Current phase:** Rebrand & restructure (active)
**Session date:** 2026-06-16
**Approval status:** New name, structure, and content depth confirmed by maintainer.
**Completion status:** In progress.

## Completed work

- Assessed the fork: monolithic README (~7,150 lines, ~2,745 links), 114
  upstream-owner references, 135 hot-linked upstream images, placeholder
  Dockerfile, public-contribution CONTRIBUTING.md, no LICENSE, no governance.
- Archived original content to `@archives/` with original relative paths.
- Authored governance files: `request.txt`, `docs/taxonomy.md`, `docs/plan.md`,
  this `STATUS.md`.
- Added `LICENSE` (CC BY 4.0) with explicit upstream attribution.
- Built the new `docs/` system: concept guides + curated catalog index.
- Wrote a lean README index and a private-maintenance `CONTRIBUTING.md`.

## Files changed

- Added: `request.txt`, `STATUS.md`, `LICENSE`, `README.md` (new),
  `CONTRIBUTING.md` (new), `docs/*.md`, `docs/catalog/*.md`.
- Retained at root: `REBRAND-PROTOCOL.txt`, `writer-agent.xml`.

## Files archived

- `@archives/README.md` — original monolithic guide (superseded).
- `@archives/CONTRIBUTING.md` — public awesome-list workflow (replaced).
- `@archives/Getting Started  with Self-Hosting.dockerfile` — non-functional
  placeholder (retired).

## Upstream references

- Removed from active content: follow buttons, maintenance/last-commit badges,
  "Follow me" links, `mikeroyal`-anchored navigation, hot-linked images.
- Retained intentionally: CC BY 4.0 attribution to the original author in
  `LICENSE` and `docs/taxonomy.md`.

## Branding decisions

- Active identity is **Self-Hosting Handbook**.
- Navigation uses relative anchors and a local `docs/` index, not upstream URLs.

## Configuration decisions

- No runtime, no env vars, no ports, no secrets. Optional local tooling (lint,
  link-check, PDF export) documented as opt-in.

## Local / VM / offline validation status

- Content is plain Markdown and reads fully offline after clone. No build needed.
- Validation performed this session:
  - All relative internal Markdown links resolve (automated check: pass).
  - No active (non-archived) file carries upstream-owner branding, badges,
    follow buttons, "Back to the Top" anchors, or hot-linked images. The only
    `mikeroyal` mentions outside `@archives/` are deliberate attribution and
    process notes in `LICENSE` and the governance files.
  - Catalog pages render in the standard `- [Name](url) — description.` format
    with no leaked emoji/HTML artifacts (spot-checked).
  - Curated catalog scale: ~1,409 entries across 6 catalog pages, plus 105
    learning-resource entries.

## Offline-readiness status

- Confirmed text-first; no reliance on upstream-hosted images.

## Known limitations / risks

- ~2,745 inherited external links are not all live-verified; link rot is
  expected and tracked. The structure supports incremental fixes.
- The curated catalog reorganizes upstream entries; coverage is broad, not
  exhaustive.

## Pending tasks

- Optional: run Markdown lint and link check locally; record results here.
- Incrementally expand `docs/catalog/` sections as needed.
