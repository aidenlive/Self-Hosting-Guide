# Security, Monitoring & Observability

Self-hostable tools for protecting your servers and credentials, diagnosing network and system problems, and tracking the health and usage of your infrastructure and applications. Each entry links to the upstream project.

[← Catalog index](./README.md) · [← Handbook home](../../README.md)

## Password Management

Tools for storing and sharing credentials such as website logins, keys, and notes in encrypted vaults.

- [Bitwarden](https://bitwarden.com/host/) — Open-source password management service that stores credentials in an encrypted vault.
- [Bitwarden Server](https://github.com/bitwarden/server) — APIs, database, and core infrastructure for the backend of Bitwarden client applications; see also the [self-hosted release repository](https://github.com/bitwarden/self-host).
- [Vaultwarden](https://github.com/dani-garcia/vaultwarden) — Unofficial Bitwarden-compatible server written in Rust, formerly known as bitwarden_rs.
- [Passbolt](https://www.passbolt.com/) — Open-source self-hosted password manager for teams, allowing credentials to be shared and stored securely.
- [KeePassXC](https://keepassxc.org/) — Cross-platform password manager that stores usernames, passwords, URLs, attachments, and notes in an offline encrypted file; runs on Windows, macOS, and Linux.
- [AuthPass.app](https://authpass.app/) — Open-source password manager for mobile and desktop that is KeePass 2.x (kdbx 3.x) compatible.
- [pass](https://www.passwordstore.org/) — Open-source unix-based password utility with various [GUI clients](https://www.passwordstore.org/#other).

## Security

Tools for hardening servers against attacks, including intrusion detection, firewalls, honeypots, and secrets management.

- [Blackbox](https://github.com/StackExchange/blackbox) — Stores secrets such as passwords safely in Git/Mercurial with automatic encryption.
- [CrowdSec](https://github.com/crowdsecurity/crowdsec) — Scans log files and requests to detect and block malicious behavior, with AppSec/WAF capabilities and a shared real-time blocklist.
- [Denyhosts](http://denyhosts.sourceforge.net/) — Blocks SSH dictionary and brute-force attacks.
- [Fail2Ban](http://www.fail2ban.org/wiki/index.php/Main_Page) — Scans log files and takes action on IPs that show malicious behavior.
- [fwknop](https://www.cipherdyne.org/fwknop/) — Protects ports via Single Packet Authorization in your firewall.
- [Glastopf](http://glastopf.org/) — Low-interaction web application honeypot that emulates vulnerabilities and gathers attack data.
- [Kippo](https://github.com/desaster/kippo) — Medium-interaction SSH honeypot, usually run as a standalone SSH daemon with a configurable filesystem sandbox.
- [OSSEC](http://ossec.net) — Host-based intrusion detection system that performs log analysis, file integrity monitoring, and rootkit detection.
- [OSQuery](https://osquery.io/) — Queries server status and information using a SQL-like interface.
- [OPNsense](https://opnsense.org/) — Open-source firewall and routing software with an integrated Netflow analyser.
- [pfSense](https://www.pfsense.org/) — Firewall and router FreeBSD distribution.
- [Snort](https://www.snort.org/) — Open-source network intrusion prevention and detection system.
- [SpamAssassin](https://spamassassin.apache.org/) — Email spam filter employing a variety of detection techniques.
- [BounCA](https://bounca.org/) — Personal SSL/Certificate Authority key management tool for creating self-signed SSL certificates from your browser.

## Troubleshooting

Tools for diagnosing network and system problems, capturing traffic, and inspecting running containers and clusters.

- [NETworkManager](https://github.com/BornToBeRoot/NETworkManager) — Tool for managing networks and troubleshooting, with a WiFi analyzer, IP scanner, port scanner, ping monitor, traceroute, DNS lookup, and LLDP/CDP capture.
- [Wireshark](https://www.wireshark.org/) — Network protocol analyzer.
- [Selfspy](https://github.com/selfspy/selfspy) — Daemon for Unix/X11, macOS, and Windows that continuously monitors and stores what you do on your computer for statistics and reminders.
- [Cilium](https://github.com/cilium/cilium) — Networking, observability, and security solution with an eBPF-based dataplane providing a flat Layer 3 network across multiple clusters.
- [Netshoot](https://github.com/nicolaka/netshoot) — Docker and Kubernetes network troubleshooting container.
- [Kubevious](https://kubevious.io/) — Suite of app-centric assurance, validation, and introspection products for Kubernetes that continuously validates manifests, cluster state, and configuration.
- [HOMER](https://github.com/sipcapture/homer) — Packet and event capture system and VoIP/RTC monitoring application based on the HEP/EEP protocol, with search and drill-down capabilities.
- [mitmproxy](https://mitmproxy.org/) — Python tool for intercepting, viewing, and modifying network traffic.
- [Sysdig](https://www.sysdig.org/) — Captures system state and activity from a running Linux instance to save, filter, and analyze.
- [Sysdig Inspect](https://github.com/draios/sysdig-inspect) — Open-source interface for container troubleshooting and security investigation.

## Monitoring

Tools for collecting metrics, logs, and traces; tracking uptime; and alerting when systems or services fail.

- [Proxmox Mail Gateway](https://www.proxmox.com/en/proxmox-mail-gateway) — Open-source email security solution that protects mail servers against email threats.
- [M2MLabs MainSpring](http://www.m2mlabs.com/) — Application framework for building machine-to-machine applications such as vehicle tracking or remote machine monitoring.
- [VictoriaMetrics](https://victoriametrics.com/) — Open-source time series database and monitoring solution available in single and cluster versions, compatible with the Prometheus pull model and many [ingestion protocols](https://docs.victoriametrics.com/#prominent-features).
- [Kestra](https://github.com/kestra-io/kestra) — Orchestration and scheduling platform for creating, running, scheduling, and monitoring complex pipelines.
- [InfluxDB](https://www.influxdata.com) — Open-source time series database for monitoring metrics and events, capturing and storing high volumes of data points.
- [Grafana](https://grafana.com/oss/grafana/) — Tool to query, visualize, and alert on metrics regardless of where they are stored.
- [Prometheus](https://prometheus.io/) — Event monitoring and alerting application that records real-time metrics in a time series database using an HTTP pull model.
- [Loki](https://grafana.com/oss/loki/) — Horizontally scalable, multi-tenant log aggregation system inspired by Prometheus that indexes labels rather than log contents.
- [Thanos](https://thanos.io/) — Set of components for a highly available metric system with unlimited storage, added on top of existing Prometheus deployments.
- [Wyze](https://wyze.com/) — Security and monitoring application to live stream HD video from security cameras.
- [Uptime Kuma](https://uptime.kuma.pet/) — Self-hosted monitoring tool.
- [Gatus](https://gatus.io/) — Developer-oriented health dashboard that monitors services using HTTP, ICMP, TCP, and DNS queries and evaluates results against conditions.
- [Upptime](https://upptime.js.org) — Open-source uptime monitor and status page powered by GitHub Actions, Issues, and Pages.
- [HertzBeat](https://github.com/dromara/hertzbeat) — Open-source, real-time, agentless monitoring system supporting web services, databases, operating systems, and middleware.
- [Tautulli](https://tautulli.com/) — Python web application for monitoring, analytics, and notifications for [Plex Media Server](https://plex.tv/).
- [Flower](https://flower.readthedocs.io/) — Web-based tool for monitoring and administrating Celery clusters.
- [Weave Scope](https://www.weave.works/oss/scope/) — Troubleshooting and monitoring tool for Docker and Kubernetes that generates a map of your application.
- [Statping](https://github.com/statping/statping) — Status page that automatically fetches applications and renders a status page for websites and applications.
- [Vector](https://vector.dev/) — End-to-end observability data pipeline to [collect](https://vector.dev/docs/reference/configuration/sources/), [transform](https://vector.dev/docs/reference/configuration/transforms/), and [route](https://vector.dev/docs/reference/configuration/sinks/) logs, metrics, and traces to any vendor.
- [Open Service Mesh (OSM)](https://openservicemesh.io/) — Lightweight, extensible, cloud-native service mesh that manages, secures, and provides observability for microservice environments.
- [Ciao](https://github.com/brotandgames/ciao) — Checks HTTP(S) URL endpoints for status codes or TCP errors and sends notifications on status change via email or webhooks.
- [Gotify](https://gotify.net/) — Server for sending and receiving messages in real-time over WebSocket.
- [Ngxtop](https://github.com/lebinh/ngxtop) — Real-time metrics for nginx and other servers.
- [Blocky](https://github.com/0xERR0R/blocky) — DNS proxy and ad-blocker for local networks.
- [Dashy](https://dashy.to/) — Self-hostable personal dashboard with status-checking, widgets, themes, icon packs, and a UI editor.
- [Netdata](https://github.com/netdata/netdata) — Real-time infrastructure monitoring agent that collects thousands of metrics from systems, hardware, containers, and applications with zero configuration.
- [Restic](https://restic.net/) — Backup program that backs up files from Linux, BSD, macOS, and Windows to many storage types, transferring only changed parts.
- [Autorestic](https://github.com/cupcakearmy/autorestic) — Wrapper around restic for managing backups across many locations.
- [MinIO](https://min.io/) — High-performance object storage server that can serve as a primary storage tier for workloads such as Spark, Presto, and TensorFlow.
- [Greyhole](https://www.greyhole.net/) — Uses Samba to pool available hard drives and create redundant copies of files to prevent data loss from hardware failure.
- [Falcon LogScale](https://www.crowdstrike.com/products/observability/falcon-logscale/) — Large-scale logging and analysis with low latency at high ingest volumes.
- [Googerteller](https://github.com/berthubert/googerteller) — Makes an audible sound when your computer sends a packet to a Google tracker or service, excluding Google Cloud.
- [TeslaMate](https://docs.teslamate.org/) — Self-hosted data logger for your Tesla.
- [OneUptime](https://oneuptime.com/) — Open-source SRE and DevOps platform that monitors websites, dashboards, and APIs and alerts your team on downtime.
- [Parca](https://parca.dev/) — Continuous profiling for analysis of CPU and memory usage down to the line number and over time.
- [DeviceHive](https://www.devicehive.com) — Open-source IoT platform for data collection, processing, analysis, visualization, and device management.
- [Distributed Services Architecture (DSA)](https://github.com/IOT-DSA) — Open-source IoT platform that facilitates device inter-communication, logic, and applications across the IoT infrastructure with a real-time data model.
- [IoTivity](https://iotivity.org) — Open-source software framework enabling device-to-device connectivity for the Internet of Things.
- [Eclipse IoT Project](https://projects.eclipse.org/projects/iot) — Open-source technology for building IoT solutions for industry and consumers.

## Dashboards

Web interfaces for visualizing monitoring data and managing monitoring systems.

- [Adagios](http://adagios.org/) — Web-based Nagios configuration interface.
- [Dash](https://github.com/afaqurk/linux-dash) — Low-overhead monitoring web dashboard for a GNU/Linux machine.
- [Thruk](http://www.thruk.org/) — Multi-backend monitoring web interface supporting Naemon, Nagios, Icinga, and Shinken.
- [Uchiwa](https://uchiwa.io) — Dashboard for the Sensu monitoring framework.
- [InfluxDB](https://www.influxdata.com) — Open-source time series database for monitoring metrics and events, capturing and storing high volumes of data points.
- [Grafana](https://grafana.com/oss/grafana/) — Tool to query, visualize, and alert on metrics regardless of where they are stored.
- [Prometheus](https://prometheus.io/) — Event monitoring and alerting application that records real-time metrics in a time series database using an HTTP pull model.

## Analytics

Tools for measuring website and product usage, often with a focus on privacy, and for exploring and visualizing data.

- [Plausible Analytics](https://plausible.io/) — Open-source, lightweight, privacy-friendly web analytics.
- [PostHog](https://posthog.com) — Product analytics, session recording, feature flagging, and A/B testing that you can self-host.
- [Ackee](https://ackee.electerious.com) — Self-hosted, privacy-focused analytics tool.
- [AWStats](http://www.awstats.org/) — Generates statistics from web, streaming, FTP, or mail server logfiles.
- [Chartbrew](https://chartbrew.com) — Web application that connects to databases and APIs to create charts.
- [Countly Community Edition](https://count.ly) — Real-time mobile and web analytics, crash reporting, and push notifications platform.
- [Druid](http://druid.io/) — Distributed, column-oriented, real-time analytics data store.
- [EDA](https://eda.jortilles.com/en/jortilles-english/) — Web application for data analysis and visualization.
- [GoAccess](http://goaccess.io/) — Real-time web log analyzer and interactive viewer that runs in a terminal.
- [GoatCounter](https://www.goatcounter.com) — Web statistics without tracking of personal data.
- [Metabase](https://metabase.com/) — Open-source way for everyone in a company to ask questions and learn from data.
- [Offen](https://www.offen.dev/) — Lightweight, open web analytics tool that gives users full access to their data.
- [Open Web Analytics](http://www.openwebanalytics.com/) — Web analytics framework for instrumenting and analyzing the use of websites and applications.
- [Redash](http://redash.io) — Connect and query data sources, build dashboards, and share them across your company.
- [RudderStack](https://rudderstack.com/) — Collect, unify, transform, and store customer data and route it to marketing, sales, and product tools; an alternative to Segment.
- [Shynet](https://github.com/milesmcc/shynet) — Privacy-friendly, detailed web analytics that works without cookies or JS.
- [Superset](http://superset.apache.org/) — Data exploration and visualization platform.
- [Umami](https://umami.is/) — Privacy-focused alternative to Google Analytics.
