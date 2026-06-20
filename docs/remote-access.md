# Remote Access

[← Handbook home](../README.md)

At some point you will want to reach your services when you are not at home —
your files from a laptop, your media on the road, your dashboard from your
phone. The naive way to do this is to forward a port on your router to the
service. Do not start there. This page explains the safer approach that has
become the default for self-hosting: connect your remote device into your home
network with an encrypted tunnel, so reaching your services from a café is no
different from reaching them from your couch, and nothing is published to the
open internet.

## Why not just forward a port?

Port forwarding takes a service that was safe on your LAN and exposes it to the
entire internet, where automated scanners probe every address constantly. Now
that service's security depends entirely on it having no exploitable bugs, no
weak default credentials, and prompt patching — forever. Plenty of self-hosted
applications were never written to survive that environment.

A **VPN tunnel** sidesteps the problem. Instead of exposing the service, you
authenticate your device into your private network first; only then can it reach
anything. The service itself stays unexposed, and the attack surface shrinks to
a single, purpose-built, well-audited tunnel endpoint.

## WireGuard: the modern foundation

**WireGuard** is a fast, modern VPN protocol built into the Linux kernel. It is
deliberately small — a few thousand lines of code versus the hundreds of
thousands in older VPNs — which makes it easier to audit and harder to
misconfigure into insecurity. It has become the foundation that most current
self-hosting VPN tools build on.

WireGuard works on a simple model: each device (a **peer**) has a key pair, and
peers are configured to trust each other's public keys. A peer running on your
home network can act as a gateway, so a connected phone or laptop behaves as if
it were physically at home.

The trade-off is setup: raw WireGuard means generating keys, writing
configuration files, and managing the home-side firewall and routing yourself.
That is very doable, and tools make it easier:

- **PiVPN** scripts a WireGuard (or OpenVPN) server onto a Raspberry Pi or
  similar in minutes.
- Router and appliance firmwares — **OpenWrt**, **pfSense**, **OPNsense**,
  **Unraid**, and **Home Assistant** add-ons — can host a WireGuard endpoint
  directly, which is convenient because the router already sits at the network's
  edge.
- Web UIs such as **wg-easy** manage peers and show connection QR codes for
  phones.

## Tailscale and Headscale: WireGuard without the wiring

The hardest part of a self-managed VPN is the networking around it: opening the
right port, dealing with an address that changes, and connecting two networks
that are both behind routers performing NAT. **Tailscale** removes that work. It
builds a private mesh network on top of WireGuard and handles key exchange,
discovery, and NAT traversal for you. Devices join your private network with a
login, and they find each other directly even when both sit behind home
routers — often with no port forwarding at all.

The honest trade-off: Tailscale's free tier relies on a company's coordination
service to broker connections (your actual traffic still flows directly,
encrypted, peer to peer). If you would rather not depend on a third party,
**Headscale** is an open-source, self-hosted implementation of that coordination
server, and **NetBird** is a comparable self-hostable mesh. You keep the
convenience and remove the external dependency, at the cost of running the
coordinator yourself.

**A practical recommendation:** if you want the least friction, start with
Tailscale. If you want full independence, run WireGuard directly (PiVPN or a
router endpoint) or self-host Headscale/NetBird. Either way, you are reaching
home through an encrypted tunnel rather than exposing services — which is the
goal.

## SSH: the administrator's tunnel

**SSH** is the encrypted protocol you use to get a shell on your server and to
move files. A few practices turn it from a liability into a safe tool:

- **Use key authentication and disable password login.** Keys are not
  guessable; passwords are. This single change removes the most common attack.
- **Do not expose SSH to the internet.** Reach it over your VPN like everything
  else. If you must expose it, change nothing about the above and add a tool
  like Fail2ban or a "port knocking" scheme to cut down on noise.
- **SSH can tunnel other services** too: `ssh -L` forwards a remote port to your
  local machine, which is a quick way to reach a single internal service without
  a full VPN.

## When you genuinely need public access

Some services are meant to be public — a blog, a site others must reach, a
webhook endpoint. For those, do not port-forward to the application directly.
Put it behind a **reverse proxy** with automatic TLS (see
**[Networking](networking.md)**), or use an outbound tunnel like a **Cloudflare
Tunnel** that connects to a provider's edge without opening any inbound port on
your router. Then treat the exposed service as hostile territory: strong
authentication, prompt updates, and minimal privileges, as in
**[Security](security.md)**.

## Find software

WireGuard tooling, VPN mesh systems, SSH utilities, and remote-access tools are
in the **[Networking & Remote Access catalog](catalog/networking.md)**.
