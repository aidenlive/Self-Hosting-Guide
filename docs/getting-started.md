# Getting Started

[← Handbook home](../README.md)

Self-hosting is running software on hardware you control rather than paying a
provider to run it for you. Instead of a monthly subscription to a photo
service, a notes app, or a password manager, you run an equivalent program on a
machine in your home or on a virtual server you rent, and you own the data it
holds.

That ownership is the point, and it is also the cost. You gain control,
privacy, and freedom from recurring fees. In exchange you take on the work a
provider used to do for you: updates, backups, security, and being the person
who gets paged when something breaks. This page is about making that trade
deliberately rather than discovering it later.

## What you actually get, and what you give up

The honest case for self-hosting:

- **Control and privacy.** Your data sits on your disk, not in a company's
  analytics pipeline. You decide retention, access, and when to migrate.
- **Cost over time.** A single small machine can replace several subscriptions.
  The savings are real once the hardware is paid off and you are not counting
  your own time.
- **Learning.** Running real services teaches networking, Linux, and operations
  in a way no tutorial does.
- **Longevity.** A service you host does not get discontinued, sold, or
  enshittified out from under you.

The honest case against:

- **You are now the operations team.** Updates, certificate renewals, failed
  disks, and 2 a.m. outages are yours.
- **Backups are not optional.** A provider quietly replicated your data across
  data centers. At home, an un-backed-up service is one dead drive away from
  permanent loss.
- **Security is your responsibility** the moment anything is reachable from the
  internet.
- **Time is the real price.** The dollar savings can evaporate if you value the
  hours spent maintaining the system.

A reasonable rule: self-host the things you care about controlling, and keep
paying for the things where the provider's reliability is worth more than your
control. You do not have to host everything to benefit from hosting something.

## How most self-hosted software is run

Most self-hosted applications today are distributed as **containers**. A
container bundles an application together with the exact libraries and
configuration it needs, isolated from the rest of your system. The practical
benefit: you can run ten applications that each expect a different version of
some dependency without those versions colliding, and you can move the whole
bundle to another machine and have it behave the same way.

The dominant tool for this is **Docker** (or the compatible, daemonless
**Podman**). You describe what you want to run in a small text file and start it
with one command; the container engine downloads a prebuilt **image** and runs a
copy of it. Because almost every project ships an image and an example
configuration, containers are usually the fastest path from "I read about this
app" to "it is running."

You do not have to start with containers — many applications also install
natively — but learning the container basics early pays off, because it is the
common language of the ecosystem. See **[Containers](containers.md)**.

## A sensible first project

Resist the urge to build the whole homelab in week one. Pick one low-stakes
service, get it running, and learn the loop of install → configure → back up →
update on something you can afford to break.

Good first services share three traits: they are useful to you, they do not need
to be exposed to the internet, and losing them for an afternoon costs nothing.
A dashboard, a read-it-later app, or a bookmarks manager all qualify. A
suggested sequence:

1. **Choose hardware you already have.** A spare laptop, a mini PC, or a
   Raspberry Pi is plenty. See **[Hardware & Operating Systems](hardware-and-os.md)**.
2. **Install a stable Linux base.** A long-term-support server distribution is
   the path of least resistance.
3. **Install a container engine** (Docker or Podman) and run one application
   from its official Compose example.
4. **Reach it on your local network first.** Do not expose anything to the
   internet yet.
5. **Set up a backup before you depend on it**, and test that the backup
   restores. An untested backup is a guess. See
   **[Storage & Backups](storage-and-backups.md)**.
6. **Only then consider remote access**, and do it with a VPN rather than by
   opening ports. See **[Remote Access](remote-access.md)**.

This order is deliberate: it puts recoverability and safety before convenience,
which is the opposite of how most people learn — usually right after losing
data or exposing an unpatched service.

## The exposure decision

The single highest-stakes choice in self-hosting is whether a service is
reachable from the public internet. As long as everything stays on your home
network, a mistake is mostly your own problem. The moment you open a port to the
world, you are running an internet-facing server that bots will find within
minutes.

The safe default is to **not** expose services directly. Reach them from outside
through a private network instead — a WireGuard or Tailscale tunnel makes your
phone behave as if it were at home, with nothing published to the open internet.
When you genuinely need public access (say, a site others must reach), put it
behind a reverse proxy with automatic TLS and treat hardening as mandatory, not
optional. Both paths are covered in **[Remote Access](remote-access.md)** and
**[Security](security.md)**.

## Where to go next

- Understand the runtime: **[Containers](containers.md)**
- Understand how traffic reaches services: **[Networking](networking.md)**
- Reach home safely from anywhere: **[Remote Access](remote-access.md)**
- Make it recoverable: **[Storage & Backups](storage-and-backups.md)**
- Find software for a need: **[Catalog](catalog/README.md)**
