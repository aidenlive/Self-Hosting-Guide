# Taxonomy — Self-Hosting Handbook

This file is the source of truth for naming, structure, rebranding, validation,
and release-readiness decisions. Keep it aligned with the actual repository.

## Identity

| Field | Value |
|---|---|
| Repository name | **Self-Hosting Handbook** |
| Git path | `aidenlive/Self-Hosting-Guide` |
| Project type | Documentation / curated knowledge base (Markdown) |
| Repository state | Rebranded and restructured from an upstream fork |
| Fork origin status | Forked from `mikeroyal/Self-Hosting-Guide`; now independent. Attribution retained for CC BY 4.0 (see `LICENSE`). |
| Usage model | Private, local, offline-first reading; optional local tooling |
| Target users | Individuals and small teams running self-hosted services on home servers, personal hardware, and VMs |

## Primary use cases

- Decide whether and how to self-host a given capability (media, backups, VPN, etc.).
- Learn the core concepts (containers, networking, storage, security) well enough to make sound choices.
- Find a curated, categorized shortlist of software for a need.
- Reference setup-level guidance for common building blocks (WireGuard, Docker, Raspberry Pi).

## Structure

```
README.md                 Lean landing page + index into docs/
LICENSE                   CC BY 4.0 + upstream attribution
CONTRIBUTING.md           Local-first contribution notes (private maintenance)
request.txt               Rebrand request, scope, acceptance criteria
STATUS.md                 Active project log
REBRAND-PROTOCOL.txt      Governing protocol (retained at root)
writer-agent.xml          Writing standard (retained at root)
docs/
  taxonomy.md             This file (source of truth)
  plan.md                 Rebrand/restructure plan
  getting-started.md      What self-hosting is; first decisions; first server
  containers.md           Containers, images, Compose, orchestration basics
  networking.md           Networking concepts, DNS, reverse proxies
  remote-access.md        WireGuard, VPNs, SSH, Tailscale, remote management
  storage-and-backups.md  Storage, filesystems, snapshots, backup strategy
  databases.md            SQL/NoSQL selection and operation
  monitoring.md           Metrics, logs, dashboards, alerting
  security.md             Hardening, secrets, updates, exposure decisions
  home-and-media-server.md  Home server stacks, media, home automation
  hardware-and-os.md      Hardware choices, operating systems, Raspberry Pi
  catalog/
    README.md             Index of the curated software catalog
    infrastructure.md     Containers/CI/CD, cloud, virtualization, automation
    networking.md         VPN, DNS, remote access, proxies, network tools
    data.md               Storage, backups, databases, archiving
    media-and-home.md     Media servers, home automation, photos, audio
    productivity.md       Notes, wikis, bookmarks, collaboration, business
    security.md           Security, monitoring, secrets, privacy
  learning-resources.md   Books, podcasts, channels, communities
@archives/                Retired upstream artifacts (original relative paths)
```

`docs/catalog/` may be built incrementally; `docs/catalog/README.md` always
reflects which sections exist.

## Runtime & configuration requirements

- **Runtime:** none. Content is Markdown; reading requires only a text viewer,
  editor, browser, or git host.
- **Optional local tooling (opt-in):**
  - Markdown linting (e.g., `markdownlint`)
  - Link checking (e.g., `lychee` or `markdown-link-check`)
  - PDF/HTML export (e.g., VS Code "Markdown PDF", or `pandoc`)
- **Configuration:** none required. No environment variables, no secrets, no
  ports, no services.

## External dependencies

- Outbound links to third-party projects (reference only; not fetched to build).
- No package dependencies, no CDN, no analytics, no telemetry.

## Offline / local constraints

- The guide is fully readable offline once cloned.
- External links require connectivity only when a reader chooses to follow them.
- No upstream-hosted images are relied upon; the system is text-first.

## Inherited from upstream

- The curated resource lists (categorized software, learning resources). These
  are preserved in reorganized, rewritten form under `docs/catalog/` and
  `docs/learning-resources.md`.
- The CC BY 4.0 license and the requirement to attribute the original author.

## Intentionally retired

- Upstream author branding: follow buttons, maintenance/last-commit badges,
  "Follow me on GitHub" links, and `mikeroyal`-anchored navigation.
- Hot-linked upstream screenshots/images.
- The non-functional placeholder Dockerfile.
- The public awesome-list contribution workflow (replaced by private-maintenance
  notes).
- All retired items live under `@archives/` with their original relative paths.

## Documentation requirements

- README is an index, not a wall of content.
- Every guide page opens on the subject (no meta-preamble), defines terms on
  first use, and earns each paragraph (per `writer-agent.xml`).
- Governance files (this file, `plan.md`, `STATUS.md`, `request.txt`) stay
  consistent with the tree.

## Testing & validation requirements

- Markdown renders without broken internal anchors.
- No active page links to a file under `@archives/` as if it were current.
- No active branding references the upstream owner except documented attribution.
- Optional: link check and Markdown lint pass (or exceptions documented).

## Definition of done

See `request.txt` → Acceptance Criteria and `REBRAND-PROTOCOL.txt` → Completion
Rules. In short: the Handbook stands on its own, originals are archived, the
docs/ system is navigable and rewritten, governance files are accurate, and
attribution is preserved.
