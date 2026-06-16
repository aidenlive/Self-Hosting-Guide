# Plan — Self-Hosting Handbook Rebrand & Restructure

## Current fork state summary

A direct fork of `mikeroyal/Self-Hosting-Guide`: a single ~7,150-line README
"awesome-list" with ~2,745 links, 114 upstream-owner references, 135
hot-linked upstream images, a placeholder Dockerfile, and a public-contribution
CONTRIBUTING.md. No LICENSE file, no governance docs.

## Desired independent outcome

An independent **Self-Hosting Handbook**: a lean README index over a navigable
`docs/` system, with rewritten narrative prose and reorganized, curated resource
catalogs. No dependence on the upstream fork identity beyond legally required
attribution. Offline-first, no runtime.

## Goals

- Rebrand fully to "Self-Hosting Handbook".
- Replace the monolith with a `docs/` system (concept guides + catalog).
- Rewrite explanatory prose to `writer-agent.xml` standards.
- Preserve the curated resources, reorganized and de-duplicated.
- Add LICENSE with upstream attribution and proper governance files.

## Non-goals

- Verifying every external link.
- Re-hosting upstream images.
- Adding deployable code or applications.

## Rebrand plan

- Title, descriptions, and metadata → "Self-Hosting Handbook".
- Remove follow buttons, badges, and "Follow me" links.
- Replace `mikeroyal`-anchored "Back to the Top" / issue / PR links with
  relative anchors and local navigation.
- Attribution to the upstream author moves to `LICENSE` and `docs/taxonomy.md`.

## Upstream-reference cleanup plan

- Archive the original README verbatim (it carries all upstream references).
- New content uses relative links and the project's own structure.
- The only retained upstream reference is the CC BY 4.0 attribution.

## File-retirement and archive plan

Move to `@archives/` with original relative paths:
- `README.md` (original monolith) — superseded by the docs/ system.
- `CONTRIBUTING.md` (public awesome-list workflow) — replaced.
- `Getting Started  with Self-Hosting.dockerfile` — non-functional placeholder.

Retained at root (governance/standards, not deliverable content):
- `REBRAND-PROTOCOL.txt`, `writer-agent.xml`.

## Structure and naming plan

See `docs/taxonomy.md` → Structure. Concept guides live at `docs/*.md`; the
curated software catalog lives under `docs/catalog/`; learning resources in
`docs/learning-resources.md`. Filenames are lowercase-hyphenated.

## Dependency and script cleanup plan

- No code dependencies exist; nothing to prune.
- Optional local tooling (lint, link-check, PDF export) is documented as opt-in
  in the README; never required.

## Local / VM / offline usage plan

- Confirm the guide reads fully offline after clone.
- Document optional local commands; ensure none are mandatory.
- No ports, secrets, env vars, or services.

## Documentation update plan

- README becomes an index with a short orientation and a table of contents.
- Each guide page rewritten to open on-subject and define terms on first use.
- Governance files kept consistent with the tree.

## Testing & validation strategy

- Check internal anchors resolve and no active page links into `@archives/`.
- Optional: run a Markdown linter and link checker locally; record results or
  exceptions in `STATUS.md`.
- Grep for residual active upstream-owner branding outside `@archives/` and
  `LICENSE`.

## Acceptance criteria

As in `request.txt`. Work is complete only when the Handbook stands
independently, originals are archived, the docs/ system is navigable and
rewritten, governance files are accurate, attribution is preserved, and
validation has passed or exceptions are documented.

## Phased execution

1. Assess + archive originals. *(done)*
2. Governance files: request.txt, taxonomy.md, plan.md, STATUS.md, LICENSE.
3. Concept guides (`docs/*.md`) + lean README.
4. Curated catalog (`docs/catalog/*`) + learning resources.
5. New CONTRIBUTING.md (private maintenance).
6. Validate; record results in STATUS.md.
