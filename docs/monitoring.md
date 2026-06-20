# Monitoring

[← Handbook home](../README.md)

Monitoring answers two questions: *is everything working right now*, and *what
happened just before it stopped working*. Without it, you learn your backup job
has been failing for three months on the day you need a restore, and you debug
outages by guessing. With a modest setup, problems announce themselves and
failures leave a trail. The goal is not a wall of beautiful graphs — it is
catching the failures you actually care about, early enough to act.

## The three signals

Operational visibility comes from three kinds of data. You do not need all three
on day one, but it helps to know what each is for.

- **Metrics** — numbers sampled over time: CPU load, free disk space, memory
  use, container restarts, request rates. They are cheap to store and ideal for
  trends and thresholds ("alert me when a disk passes 90%").
- **Logs** — the text records services emit as they run. When something breaks,
  logs usually contain the reason. Centralizing them means you search one place
  instead of SSHing into machines hunting for the right file.
- **Uptime checks** — the simplest and highest-value signal: is this service
  responding at all? An uptime monitor that pings your services and notifies you
  when one stops is the single best return on effort in this whole page.

## A standard metrics stack

The common, well-supported pattern for metrics is:

- **Prometheus** collects (scrapes) metrics from your services and stores them
  as time series.
- **Exporters** expose metrics Prometheus can read — `node_exporter` for host
  stats (CPU, disk, memory), **cAdvisor** for per-container stats, and many
  application-specific exporters.
- **Grafana** queries that data and renders dashboards and alerts.

This trio is the default for a reason: it is open, widely documented, and there
are ready-made dashboards for almost any component. The cost is that it is
several services to run and learn. For a small setup, that may be more than you
need.

**A lighter path:** if you just want to know when something goes down, start
with an uptime monitor — **Uptime Kuma** is a popular, self-hosted choice that
checks your services and sends notifications, with almost no setup. Add the full
metrics stack later, when you have a question that uptime checks alone cannot
answer. Matching the tool to the need beats deploying observability
infrastructure for three containers.

## Centralizing logs

When you outgrow reading per-container logs by hand, a log system collects them
in one searchable place. **Grafana Loki** pairs naturally with the Prometheus
and Grafana stack and is comparatively light. The **Elasticsearch/OpenSearch**
family is more powerful and more demanding to run. Until you feel the pain of
scattered logs, `docker compose logs -f` is a perfectly good starting point.

## Alerts you will actually act on

A monitor that no one looks at is decoration. Alerting turns monitoring into
something that reaches you:

- **Send alerts where you will see them** — push notification, chat, email — via
  a notification gateway. Many tools integrate with services like ntfy,
  Gotify, or Apprise (see the **[Productivity catalog](catalog/productivity.md)**).
- **Alert on symptoms you care about**, not on everything. A flood of alerts
  trains you to ignore them, and the one that matters gets lost. Start with a
  short list: a service is down, a disk is nearly full, a backup job failed.
- **Especially: alert on backup failure.** Backups fail silently by nature. An
  alert is what turns "we have backups" into "we have backups that ran."

## What to watch first

If you do nothing else, watch these four things:

1. **Are services up?** (uptime checks)
2. **Is disk space running out?** (the most common avoidable outage)
3. **Did backups succeed?** (the most expensive thing to get wrong)
4. **Are containers restarting in a loop?** (an early sign of trouble)

Everything else is refinement on top of those four.

## Find software

Monitoring systems, dashboards, log management, and uptime tools are in the
**[Security & Monitoring catalog](catalog/security.md)**; notification gateways
are in the **[Productivity catalog](catalog/productivity.md)**.
