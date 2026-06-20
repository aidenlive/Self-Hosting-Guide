# Databases

[← Handbook home](../README.md)

Most self-hosted applications need somewhere to store structured data, and many
ship with a database alongside them. Often you never touch it directly — the
application's Compose file starts a database container and wires it up for you.
But understanding the basics helps you choose between applications, size your
hardware, and — most importantly — back the data up correctly, because a
database is the one place where copying files while the service runs can quietly
corrupt your backup.

## SQL vs. NoSQL

Databases fall into two broad families, and the distinction is worth knowing
because applications will tell you which they need.

**Relational (SQL) databases** store data in tables with defined columns and
enforce relationships and constraints between them. They are the default for
data with a clear, stable shape — users, orders, posts — and they excel when
correctness and complex queries matter. The common self-hosted choices:

- **PostgreSQL** — the capable, standards-respecting default; a safe choice for
  almost anything, and what a growing share of applications now expect.
- **MariaDB / MySQL** — extremely widely supported; many applications document
  it as their primary option.
- **SQLite** — a database that is a single file, with no server to run. Perfect
  for small single-user applications; many self-hosted apps embed it, which
  makes them trivially simple to back up — just copy the file (while the app is
  stopped or using its backup command).

**NoSQL databases** relax the table model for other shapes of data:

- **Document stores** (**MongoDB**, **CouchDB**) hold flexible, JSON-like
  records — useful when the data's shape varies or evolves.
- **Key-value stores and caches** (**Redis**, **Valkey**, **KeyDB**) hold simple
  pairs in memory for speed; applications use them for sessions, queues, and
  caching rather than as the system of record.
- **Time-series databases** (**InfluxDB**, **TimescaleDB**, **Prometheus**)
  specialize in timestamped measurements and power most monitoring stacks (see
  **[Monitoring](monitoring.md)**).
- **Search engines** (**Elasticsearch**, **OpenSearch**, **Meilisearch**)
  index text for fast full-text queries.

You rarely choose a database in the abstract. You choose an application, and it
tells you what it supports. When it offers a choice, **PostgreSQL is the
low-regret default** for relational needs.

## Running a database, briefly

- **Let the application's Compose file manage it** when one is provided. Pin the
  database image to a major version so an unexpected upgrade does not break the
  application.
- **Put the data on a volume**, like any container state (see
  **[Containers](containers.md)**), and prefer a stable local disk over network
  storage for the database files.
- **Set strong credentials** via environment variables or secrets, never
  defaults — databases are a prime target if ever exposed (see
  **[Security](security.md)**).
- **Keep it off the network.** A database should listen only on the internal
  container network, reachable by its application and nothing else. There is
  almost never a reason to publish a database port to your LAN, let alone the
  internet.

## Backing up databases correctly

This deserves its own warning because it is the most common backup mistake.
**Do not back up a running database by copying its files.** A live database
writes constantly; a file copy taken mid-write captures an inconsistent state
that may not restore. Instead:

- **Use the database's own dump tool** — `pg_dump` for PostgreSQL, `mysqldump`
  or `mariadb-dump` for MariaDB/MySQL — to produce a consistent export, then
  back up that export.
- **Or stop the container** briefly and copy the files while nothing is writing
  (fine for small, personal services and embedded SQLite).
- **Or use snapshot-consistent** mechanisms if your storage and database support
  them.

Whatever you choose, the rule from **[Storage & Backups](storage-and-backups.md)**
still governs: keep versioned copies, store one off-site, and test that the dump
actually restores into a working database.

## Find software

Database engines and management tools are in the
**[Data catalog](catalog/data.md)**.
