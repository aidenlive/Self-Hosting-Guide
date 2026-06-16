# Contributing & Maintenance Notes

This is a privately maintained handbook, kept for personal and local use rather
than run as a public, open-contribution project. These notes exist to keep edits
consistent over time, whether by the maintainer or anyone they share it with.

## Writing standard

All prose follows [`writer-agent.xml`](writer-agent.xml). In practice:

- **Open on the subject.** No throat-clearing or descriptions of the writing
  itself.
- **Define a term the first time it appears.** Assume an intelligent reader, not
  an expert in this niche.
- **Prefer concrete over abstract.** Show the mechanism; give an example.
- **Cut filler.** Remove "amazing", "simply", "powerful", "easily", and
  qualifiers that add no information. Every paragraph earns its place.
- **Be honest about trade-offs.** State what a choice costs, not only what it
  gives. Recommend, but show the reasoning.

## Catalog entry format

One link per line, in the established em-dash style:

```
- [Resource Name](https://example.com) — one concise, factual sentence.
```

- Add to the most fitting existing category; keep categories in their current
  order.
- Suggest software you have actually used or have good reason to trust.
- Keep descriptions short, factual, and free of marketing language.
- Do not duplicate an entry that already exists in another category unless it
  genuinely belongs in both.
- Check spelling and that the link resolves.

## Structure rules

- Concept guides live at `docs/*.md`; the software catalog lives under
  `docs/catalog/`; learning resources in `docs/learning-resources.md`.
- Filenames are lowercase-hyphenated.
- The README stays a lean index — new long-form content goes in `docs/`, not the
  README.
- Keep the governance files consistent with reality:
  [`docs/taxonomy.md`](docs/taxonomy.md) (source of truth),
  [`docs/plan.md`](docs/plan.md), [`STATUS.md`](STATUS.md), and
  [`request.txt`](request.txt).

## Before committing

No build or runtime is required to use the Handbook. Optional local checks:

```bash
# Markdown style (optional)
markdownlint '**/*.md'

# Link checking (optional; expect some known dead inherited links)
lychee --no-progress 'docs/**/*.md' README.md
```

Record any notable validation results or decisions in
[`STATUS.md`](STATUS.md).

## Archived material

The original upstream guide is preserved under
[`@archives/`](@archives/) with its original paths. Do not edit archived files
or link to them as if they were current; they exist for reference and
attribution only.

## License & attribution

Contributions are accepted under [CC BY 4.0](LICENSE). This work is a derivative
of the "Self-Hosting Guide" by Mike Royal; the attribution in
[`LICENSE`](LICENSE) must be preserved.
