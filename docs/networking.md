# Networking

[← Handbook home](../README.md)

When you self-host, you become responsible for the path a request takes to reach
your service. This page covers the pieces that make that path work — addresses,
names, certificates, and the reverse proxy that ties them together — at the
level of detail you need to run services confidently and secure them correctly.

## Addresses, ports, and what is reachable

Every machine on your network has an **IP address**. A **port** identifies a
specific service on that machine; a web server typically listens on port 80
(HTTP) and 443 (HTTPS). "Exposing a service" means making one of its ports
reachable from somewhere — and *where* it is reachable from is the security
question that matters most.

Three zones, from safest to riskiest:

1. **Localhost only** — the service is reachable only from the machine it runs
   on. Good for components that other local services talk to.
2. **Local network (LAN)** — reachable from other devices in your home. This is
   the right default for most self-hosted services.
3. **The public internet** — reachable from anywhere, by anyone, including the
   bots that continuously scan every address for vulnerable services.

Give your server a **static IP** (or a DHCP reservation in your router) so its
address does not change underneath your configuration. Keep services in zone 1
or 2 unless you have a specific reason to publish them, and even then prefer a
private tunnel over opening a port — see **[Remote Access](remote-access.md)**.

## DNS: names instead of numbers

The **Domain Name System (DNS)** translates names like `jellyfin.home.lan` into
IP addresses. You will use it in two ways:

- **Internally**, to give your services memorable names on your own network
  rather than memorizing IP addresses and ports. A local DNS resolver — often
  combined with a network-wide ad blocker like Pi-hole or AdGuard Home — handles
  this and improves browsing for every device at once.
- **Externally**, if you own a domain and want to reach services by name from
  outside. Because most home internet connections have an IP address that
  changes periodically, **dynamic DNS** keeps a name pointed at your current
  address automatically.

DNS resolvers, ad-blocking resolvers, and dynamic-DNS clients are listed in the
**[Networking & Remote Access catalog](catalog/networking.md)**.

## TLS: encryption and trust

**TLS** is what puts the "S" in HTTPS. It does two jobs: it encrypts traffic so
it cannot be read in transit, and it proves a service is who it claims to be
using a **certificate**. You want TLS on anything carrying credentials or
private data, which is nearly everything.

You do not buy certificates anymore. **Let's Encrypt** issues them free and
automatically, and modern reverse proxies renew them for you without
intervention. For purely internal services you can run your own certificate
authority, though this means installing your authority's root certificate on
each device that should trust it.

## The reverse proxy: one front door

Once you run more than one or two services, mapping a different port to each one
becomes unwieldy and hard to secure. A **reverse proxy** solves this. It is a
single service that accepts incoming connections and forwards each request to
the right backend based on its hostname or path — so `photos.example.com` and
`notes.example.com` can both arrive on port 443 and land on different
containers.

A reverse proxy is the natural place to centralize concerns that would otherwise
be scattered across every service:

- **TLS termination** — obtain and renew certificates in one place.
- **A single entry point** — only the proxy's ports are exposed; backends stay
  private on an internal network.
- **Authentication** — require a login in front of services that have weak or no
  access control of their own.
- **Rate limiting and access rules** — apply consistent policy everywhere.

Common choices range from configuration-light proxies that fetch certificates
automatically (Caddy, Nginx Proxy Manager, Traefik) to the highly configurable
classics (Nginx, HAProxy). All of them are in the
**[Infrastructure catalog](catalog/infrastructure.md)** under web servers and
the networking catalog.

## A working topology

A reliable, secure layout for a single-host setup looks like this:

```
Internet ──▶ (only if truly needed) ──▶ Reverse proxy (443, TLS)
                                              │  routes by hostname
                 ┌────────────────────────────┼────────────────────────┐
                 ▼                            ▼                          ▼
            App A (private)             App B (private)          App C (private)
                          all on an internal container network,
                          no host ports published directly
```

For access from outside your home, you have two defensible options: route
through the reverse proxy with TLS and strong authentication, or — better for
anything that does not need to be public — skip exposure entirely and connect
over a private tunnel as described in **[Remote Access](remote-access.md)**.

## Find software

DNS, dynamic DNS, network tools, and service discovery are in the
**[Networking & Remote Access catalog](catalog/networking.md)**. Reverse proxies
and web servers are in the **[Infrastructure catalog](catalog/infrastructure.md)**.
