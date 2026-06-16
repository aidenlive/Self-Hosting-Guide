# Self-Hosting Handbook

Self-hosting means running the software you depend on — backups, media, notes,
VPN, dashboards — on hardware you control, instead of renting it as a monthly
subscription. This handbook explains how that works and helps you decide what to
run, on what, and how to keep it secure and recoverable.

It is written for people running services on a home server, a spare machine, a
single-board computer, or a virtual machine — for their own use, privately and
offline-first. There is nothing to deploy here: the Handbook is documentation
you read, clone, or export to PDF.

## Start here

- **[Getting Started](docs/getting-started.md)** — what self-hosting is, the
  trade-offs, and how to stand up a first service without regretting it later.

Then follow the path that matches what you want to do.

## Concept guides

Each guide teaches the building blocks and links to a curated shortlist of
software in the catalog.

| Guide | What it covers |
|---|---|
| [Containers](docs/containers.md) | Images, Docker/Podman, Compose, and when orchestration is worth it |
| [Networking](docs/networking.md) | DNS, reverse proxies, TLS, and how requests reach your services |
| [Remote Access](docs/remote-access.md) | WireGuard, VPNs, SSH, and Tailscale for reaching home from anywhere |
| [Storage & Backups](docs/storage-and-backups.md) | Filesystems, snapshots, and a backup strategy that actually restores |
| [Databases](docs/databases.md) | Choosing and running SQL and NoSQL stores |
| [Monitoring](docs/monitoring.md) | Metrics, logs, dashboards, and alerts you'll act on |
| [Security](docs/security.md) | Hardening, secrets, updates, and the exposure decision |
| [Home & Media Server](docs/home-and-media-server.md) | Media, photos, and home automation stacks |
| [Hardware & Operating Systems](docs/hardware-and-os.md) | Choosing hardware, OSes, and the Raspberry Pi |

## Software catalog

A categorized, curated index of self-hostable software. Use it to find a
shortlist for a need, not to install everything at once.

- **[Catalog index →](docs/catalog/README.md)**

## Learning resources

- **[Books, podcasts, channels, and communities →](docs/learning-resources.md)**

## Using this Handbook

The content is plain Markdown. You can:

- Read it on a git host or in any Markdown viewer.
- Clone it and read fully offline — no build step, no runtime, no accounts.
- Export a page to PDF (for example, the VS Code "Markdown PDF" extension, or
  `pandoc page.md -o page.pdf`).

Optional, never required: lint with `markdownlint`, and check links with
`lychee` or `markdown-link-check`.

## Repository map

```
README.md            This index
docs/                Concept guides, catalog, and learning resources
docs/catalog/        Curated, categorized software lists
LICENSE              CC BY 4.0, with attribution to the upstream original
CONTRIBUTING.md      Notes for private maintenance
request.txt          Rebrand request, scope, acceptance criteria
STATUS.md            Project log
docs/plan.md         Rebrand/restructure plan
docs/taxonomy.md     Source of truth for naming and structure
@archives/           The original guide, preserved as inherited
```

## Status and limitations

This Handbook is a rebranded, restructured, and largely rewritten derivative of
an earlier self-hosting list. The original is preserved under
[`@archives/`](@archives/). The curated catalog is broad rather than
exhaustive, and a list of this size will contain links that have moved or gone
dead over time; corrections are made incrementally. See [`STATUS.md`](STATUS.md).

## License

Distributed under the [Creative Commons Attribution 4.0 International (CC BY
4.0)](https://creativecommons.org/licenses/by/4.0/) license. This work builds on
the "Self-Hosting Guide" by Mike Royal; attribution details are in
[`LICENSE`](LICENSE).
