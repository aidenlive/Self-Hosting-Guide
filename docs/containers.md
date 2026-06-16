# Containers

[← Handbook home](../README.md)

A **container** packages an application with the libraries, tools, and
configuration it needs, and isolates it from the rest of the operating system.
The application inside sees its own filesystem and dependencies; the host sees a
single, contained process. This solves a problem that otherwise makes
self-hosting painful: two applications that need conflicting versions of the
same dependency can run side by side without either breaking the other, and the
same bundle runs the same way on your laptop, your server, and a friend's
machine.

Containers are not virtual machines. A virtual machine emulates a whole computer
and runs its own kernel, which is heavyweight. A container shares the host's
kernel and isolates only what is above it, which makes it start in seconds and
cost little memory. For most self-hosting, containers are the right default;
reach for full virtualization when you need a different kernel or strong
hardware-level isolation (see **[Hardware & Operating Systems](hardware-and-os.md)**).

## The core vocabulary

- **Image** — a read-only template containing an application and its
  dependencies. You download images from a **registry** such as Docker Hub,
  LinuxServer.io, or Quay.
- **Container** — a running instance of an image. You can start, stop, and
  delete containers freely; the image is unchanged.
- **Volume** — persistent storage that lives outside the container's own
  filesystem. This is how data survives when you recreate or upgrade a
  container. **Anything you care about must live on a volume**, because the
  container's internal filesystem is disposable.
- **Port mapping** — exposes a port inside the container on the host so you can
  reach the service (for example, host `8096` → container `8096`).
- **Network** — containers can share a private network so they can talk to each
  other by name without exposing those ports to the host.

The mental model: images are immutable; containers are disposable; volumes are
where your real data lives. Internalize that and most operational mistakes
disappear.

## Docker and Podman

**Docker** is the most widely used container engine and the de facto standard;
nearly every self-hostable project publishes a Docker image and an example
configuration. **Podman** is a compatible, daemonless alternative that can run
containers without a long-running root service, which some prefer for security.
Their command-line interfaces are close enough that most Docker instructions
work under Podman unchanged.

On Linux, install the engine from your distribution's packages. On macOS and
Windows, you run containers inside a lightweight Linux VM that the tooling
manages for you (Docker Desktop, or alternatives like Lima and Colima).

## Compose: the format you will actually use

Running a single container by hand is fine for experiments. For anything you
intend to keep, use **Docker Compose**: a YAML file that declares the services,
their images, volumes, ports, and environment in one place. You bring the whole
stack up or down with a single command, and the file becomes a readable,
version-controllable record of exactly how the service is configured.

A minimal example — a media server with its configuration persisted to a volume:

```yaml
services:
  jellyfin:
    image: jellyfin/jellyfin:latest
    container_name: jellyfin
    ports:
      - "8096:8096"
    volumes:
      - ./config:/config        # configuration persists here
      - /srv/media:/media:ro    # your library, mounted read-only
    restart: unless-stopped
```

```bash
docker compose up -d     # start in the background
docker compose logs -f   # follow the logs
docker compose pull && docker compose up -d   # update to newer images
docker compose down      # stop and remove the containers (volumes remain)
```

Two habits make Compose safe to live with: keep every Compose file in a git
repository so changes are tracked, and **never store secrets in the file
itself** — use an `.env` file (git-ignored) or a secrets manager, as covered in
**[Security](security.md)**.

## When orchestration is worth it

**Orchestration** automates running containers across one or more machines:
scheduling, restarting failed containers, rolling updates, and scaling.
**Kubernetes** is the industrial-strength option; lighter distributions such as
k3s bring it within reach of a homelab, and **Nomad** offers a simpler
alternative.

Be honest about whether you need it. For a handful of services on one machine,
Compose plus a restart policy is simpler, easier to debug, and entirely
sufficient. Orchestration earns its complexity when you have multiple nodes,
need high availability, or are managing enough services that manual placement
becomes the bottleneck. Adopting Kubernetes for three containers on one box adds
a second system to maintain without solving a problem you have.

## Operating containers well

- **Persist deliberately.** Map a volume for every piece of state. Treat the
  container as throwaway.
- **Pin versions for things that matter.** `:latest` is convenient but moves
  under you; pinning a tag makes upgrades a deliberate, reversible act.
- **Update on a schedule, with backups first.** Pull new images, restart, and
  verify. Tools like Watchtower can automate updates, but automated updates
  without backups are a way to automate data loss.
- **Use a reverse proxy** to put TLS in front of multiple services on one host
  instead of mapping a sprawl of ports. See **[Networking](networking.md)**.
- **Read the logs** when something misbehaves: `docker compose logs -f <service>`
  is the first diagnostic, not the last resort.

## Find software

For container engines, registries, build tools, management UIs, and
orchestration platforms, see the
**[Infrastructure & Platform catalog](catalog/infrastructure.md)**.
