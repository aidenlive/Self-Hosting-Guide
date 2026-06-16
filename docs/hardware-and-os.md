# Hardware & Operating Systems

[← Handbook home](../README.md)

You do not need to buy anything to start self-hosting, and you should not start
by buying anything. The most common mistake is over-investing in hardware before
you know what you will run. This page covers how to choose a machine and an
operating system in proportion to what you actually need — which, for a first
server, is very little.

## Start with what you have

Almost any computer made in the last decade can run a useful home server: a
retired laptop, a mini PC, an old desktop, or a single-board computer. A laptop
has a built-in screen, keyboard, and — usefully — a battery that acts as a tiny
uninterruptible power supply. Begin there, learn what you actually run and how
much it demands, and let that experience tell you what to buy, if anything.

When you do buy deliberately, weigh four things:

- **Power efficiency.** A home server runs 24/7, so idle power draw matters more
  than peak performance — you pay for it every hour, forever. Low-power mini PCs
  and single-board computers shine here.
- **RAM.** The resource you run out of first. Many small services are happy with
  little, but a few (databases, search indexes, photo AI, virtualization) are
  hungry. RAM is usually the best place to spend.
- **Storage.** Capacity and redundancy for your data — covered in
  **[Storage & Backups](storage-and-backups.md)**. An SSD for the operating
  system and databases plus larger drives for bulk media is a common split.
- **Transcoding, if you stream media.** Hardware-accelerated video (such as
  Intel Quick Sync) does far more for a media server than extra CPU cores — see
  **[Home & Media Server](home-and-media-server.md)**.

### Classes of machine

- **Single-board computers (Raspberry Pi and kin)** — cheap, tiny, near-silent,
  very low power. Ideal for focused, light jobs: a VPN endpoint, Pi-hole, Home
  Assistant, or a first service or two. Covered in detail below.
- **Mini PCs** — the sweet spot for most home servers. An x86 mini PC delivers
  far more performance per watt than a tower, runs all standard software, and
  fits on a shelf.
- **Repurposed desktops/laptops** — free if you have one; great for learning.
  Watch idle power on older hardware.
- **NAS appliances** — purpose-built storage boxes (TrueNAS, Synology, Unraid)
  that many people also use to run containers, consolidating storage and
  services in one device.
- **Used enterprise servers** — maximum power per dollar, but loud, power-hungry,
  and overkill for most homes. A trap for newcomers chasing specifications they
  will never use.

## Operating systems

The OS is the base everything else runs on. Favor boring and stable over new and
exciting.

- **A long-term-support (LTS) Linux server distribution** — Debian or Ubuntu
  Server LTS — is the path of least resistance. The largest community, the most
  tutorials, and the longest support windows. For a first server, this is the
  recommendation.
- **Container-and-VM platforms** — **Proxmox VE** turns a machine into a manager
  for virtual machines and containers with a web UI, which is excellent once you
  want to run several isolated environments on one box.
- **Storage-first systems** — **TrueNAS** (built on ZFS) and **Unraid** lead
  with storage and add application support on top; a good fit when the data is
  the point.
- **Appliance OSes** — **Home Assistant OS** and similar are purpose-built
  images you flash and use, trading flexibility for a turnkey experience.
- **The BSDs** — FreeBSD and derivatives are stable, coherent server systems
  with first-class ZFS; a smaller ecosystem, but well regarded by those who run
  them.

A reasonable default for most people: Debian or Ubuntu Server LTS, with Docker
on top. Reach for Proxmox when you want virtualization, or a NAS OS when storage
is the centerpiece.

## The Raspberry Pi

The **Raspberry Pi** is a credit-card-sized single-board computer that became
the on-ramp to self-hosting for a generation, because it is inexpensive, sips
power, and has an enormous community behind it. It is genuinely capable for
focused workloads, and it has real limits worth knowing before you lean on it.

**What a Pi is great at:**

- A VPN endpoint (PiVPN/WireGuard) — see **[Remote Access](remote-access.md)**.
- Network-wide ad blocking and local DNS (Pi-hole, AdGuard Home).
- Home Assistant and other home-automation hubs.
- One or a few lightweight containerized services.

**Where a Pi struggles:**

- **Heavy work** — video transcoding, large databases, search indexing, or
  many services at once will overwhelm it. Use a mini PC for those.
- **Storage durability.** Cheap microSD cards are the classic Pi failure point:
  they wear out and corrupt under constant writes. **Boot from an SSD** (over
  USB or, on newer models, NVMe) rather than a microSD card for anything you
  intend to rely on, and back it up like any other server.

**Getting started on a Pi:**

1. Write a 64-bit OS image to your boot media with the official Raspberry Pi
   Imager, which can preconfigure SSH and Wi-Fi before first boot (headless
   setup, no monitor needed).
2. Give it a static IP or DHCP reservation so its address is stable.
3. Update the system, install Docker, and run your first service.
4. Move off the microSD card to an SSD before you depend on it.

A Pi is an excellent place to learn and a fine permanent home for light,
always-on jobs. When you outgrow it, the skills transfer directly to a bigger
machine — the software and the habits are the same.

## Find software

Operating systems, NAS platforms, virtualization, hardware tools, and
Raspberry Pi utilities are in the
**[Infrastructure catalog](catalog/infrastructure.md)** and the
**[Data catalog](catalog/data.md)**.
