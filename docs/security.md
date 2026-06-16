# Security

[← Handbook home](../README.md)

Security in self-hosting is less about exotic attacks and more about a handful
of habits that, kept consistently, prevent almost all real-world compromise. The
threat is not a targeted hacker studying your setup; it is automated scanners
that sweep the entire internet looking for exposed services, default passwords,
and unpatched software, and exploit whatever they find. Defending against that
is mostly about not being the easy target. This page is the short list of habits
that get you there.

## The exposure decision comes first

Every other security question is downstream of one choice: **what is reachable
from the internet?** A service confined to your home network has a tiny attack
surface — an intruder would already need to be on your network. The same service
exposed to the internet is reachable by every bot on Earth, continuously.

So the foundational rule, repeated from across this Handbook because it matters
most: **do not expose services to the internet unless you must.** Reach them from
outside through a VPN tunnel instead (see
**[Remote Access](remote-access.md)**). When something genuinely must be public,
treat it as a hardened, internet-facing server, not a casual LAN service.

## Authentication: close the easy doors

- **Replace every default credential.** Default admin passwords are the first
  thing scanners try, because they work astonishingly often. Change them before
  a service ever leaves localhost.
- **Use a password manager and unique passwords.** A self-hosted manager like
  **Vaultwarden** (Bitwarden-compatible) or **KeePass** lets every service have
  a strong, unique password without you memorizing any of them.
- **Turn on multi-factor authentication** wherever a service supports it,
  especially anything reachable from outside.
- **Put an authentication layer in front of weak apps.** Some self-hosted
  applications have minimal access control. A reverse proxy with an
  authentication gateway (or an identity provider like Authelia or Authentik)
  can require a login before a request ever reaches them — see
  **[Networking](networking.md)**.

## Updates: the patch you skip is the hole they use

Most successful intrusions exploit a vulnerability that already had a fix the
operator had not applied. Staying current is unglamorous and it is the single
most effective technical defense.

- **Update the host OS regularly** — enable automatic security updates on your
  base system.
- **Update container images on a schedule**, and *back up before you do* (see
  **[Storage & Backups](storage-and-backups.md)**). Automated updaters like
  Watchtower help, but automated updates without backups automate the risk of a
  bad release breaking your data.
- **Pin versions for critical services** so updates are deliberate and
  reversible rather than surprises.

## Secrets: keep them out of your files

- **Never commit passwords, API keys, or tokens to git.** Use a git-ignored
  `.env` file for Compose, and add `.env` to `.gitignore` before the first
  commit, not after.
- For more than a few secrets, use a dedicated secrets manager (Infisical,
  Vault, or your platform's secret mechanism) rather than scattering them across
  Compose files.
- **Treat backups as secret too.** A backup contains everything sensitive your
  services hold, so encrypt it — which the backup tools in
  **[Storage & Backups](storage-and-backups.md)** do by default.

## Reduce the blast radius

Assume any single service might be compromised, and limit what that would cost:

- **Run services as non-root** with the least privilege they need. Containers
  help here by isolating each service.
- **Segment the network.** Keep databases and internal components on a private
  container network, not published to your LAN. Consider a separate VLAN for
  untrusted devices like IoT gadgets.
- **Expose only what is needed.** Every published port is a door; do not open
  one you are not using.

## Watch for trouble

Hardening reduces the chance of compromise; monitoring tells you when something
slips through or breaks. At minimum, know when a service goes down, when a disk
fills, and when a backup fails — see **[Monitoring](monitoring.md)**. For
internet-facing services, a tool like **Fail2ban** that blocks repeated failed
logins, and **CrowdSec** for community-shared threat intelligence, cut down the
constant background noise of automated attacks.

## A practical checklist

1. Nothing exposed to the internet unless deliberately decided.
2. Remote access over a VPN, not forwarded ports.
3. No default credentials anywhere; unique passwords from a manager; MFA where
   possible.
4. Host and containers updated on a schedule, with backups taken first.
5. Secrets in git-ignored `.env` or a secrets manager — never committed.
6. Encrypted, tested, off-site backups.
7. Monitoring that alerts on downtime, full disks, and failed backups.

None of this is advanced. Done consistently, it puts you well outside the
population of easy targets that automated attacks depend on.

## Find software

Password managers, authentication and identity tools, security and intrusion
defense, and monitoring are in the
**[Security & Monitoring catalog](catalog/security.md)**.
