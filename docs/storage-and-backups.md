# Storage & Backups

[← Handbook home](../README.md)

This is the page that prevents the worst day in self-hosting: the one where a
drive dies and takes your only copy of something irreplaceable with it. A
provider handled durability invisibly. At home, durability is a thing you design
on purpose. The good news is that a sound storage and backup setup is not hard —
it just has to exist *before* you need it, not after.

## Storage: where the bytes live

A few concepts shape every decision here.

- **Drives fail.** Not "might" — will. Plan for it as a certainty with a date
  you do not know.
- **RAID is not a backup.** **RAID** combines several disks so that one (or
  more) can fail without losing data or downtime. That protects against
  hardware failure, but it faithfully replicates your mistakes: a deleted file,
  a ransomware encryption, or a bad write is mirrored instantly to every disk.
  RAID buys availability, not recoverability.
- **Filesystems differ in what they protect.** A modern **copy-on-write**
  filesystem — **ZFS** or **Btrfs** — checksums data to detect silent
  corruption ("bit rot"), takes near-instant snapshots, and can verify
  integrity over time. Traditional filesystems (ext4, XFS) are simpler and
  rock-solid but do less for you. For a storage server holding data you care
  about, ZFS or Btrfs is worth the learning curve.

For a dedicated storage appliance, purpose-built systems like **TrueNAS** (ZFS),
**Unraid** (flexible mixed-disk pools), or a Synology NAS package the hardware
and filesystem decisions into a managed product. Building your own with ZFS or
Btrfs gives more control. Both are valid; the appliance trades flexibility for
not having to think about it.

## Snapshots: instant, local undo

A **snapshot** is a frozen, read-only view of a filesystem at a moment in time,
created almost instantly and cheaply on ZFS and Btrfs because it only records
what changes afterward. Snapshots are the fastest way to recover from the most
common disasters — a fat-fingered delete, a botched upgrade, a configuration
mistake — because rolling back is near-instant.

But understand their limit: a snapshot lives on the same disks as the data. If
the pool dies or the machine is stolen or burns, the snapshots die with it.
Snapshots are excellent *undo*; they are not *backup*. You need both.

## Backups: the 3-2-1 rule

The discipline that actually saves data is captured in one rule:

> **3-2-1** — keep at least **3** copies of anything you care about, on **2**
> different kinds of media, with **1** copy off-site.

Concretely, for a home setup:

1. **The live copy** on your server.
2. **A local backup** to a different disk or machine — fast to make and fast to
   restore from.
3. **An off-site copy** — encrypted, somewhere physically elsewhere (a cloud
   object store, or a drive at another location) — so a fire, flood, theft, or
   ransomware event cannot take every copy at once.

Two properties separate a real backup from a comforting illusion:

- **Versioning.** Backups must keep history. If your backup blindly mirrors the
  source, then a file you accidentally deleted — or one an attacker
  encrypted — is faithfully deleted or encrypted in the backup too on the next
  run. Tools like **Restic**, **BorgBackup**, **Kopia**, and **Duplicati** keep
  deduplicated, encrypted, versioned snapshots specifically to avoid this.
- **Tested restores.** A backup you have never restored is a hypothesis, not a
  backup. Schedule an occasional real restore of a real file. The day you need
  it is the wrong day to discover the job had been silently failing for months.

## What to back up

- **Application data and configuration** — the volumes your containers write to,
  and the Compose files and `.env` that define your stack (keep those in git).
- **Irreplaceable personal data** — photos, documents, anything you created.
  Highest priority; this is the data with no second source.
- **Not** the easily re-downloadable — operating systems, container images, and
  media you can re-acquire. Back up the configuration that reassembles them
  instead, and you save space for what truly matters.

## A minimal, sound setup

1. Keep service data on a checksummed filesystem (ZFS or Btrfs) if you can.
2. Take regular **snapshots** for fast local undo.
3. Run a **versioned, encrypted backup** (Restic/Borg/Kopia) to a second
   on-site location on a schedule.
4. Replicate that backup **off-site**, encrypted.
5. **Test a restore** on a recurring basis and confirm the jobs are actually
   running — monitor them, because silent backup failure is the classic trap
   (see **[Monitoring](monitoring.md)**).

## Find software

NAS platforms, filesystems, snapshot tools, backup programs, and archiving
utilities are in the **[Data catalog](catalog/data.md)**.
