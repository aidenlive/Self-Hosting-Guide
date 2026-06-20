# Networking & Remote Access

Tools for reaching, connecting, and managing your machines and networks: remote desktops, SSH, VPNs, directory services, log handling, DNS, general network utilities, and service discovery. Use this page to find the building blocks for secure access and a healthy self-hosted network.

[← Catalog index](./README.md) · [← Handbook home](../../README.md)

## Remote Access

Software for viewing or controlling a computer's desktop from elsewhere, plus gateways and tunnels that expose those sessions securely.

- [FreeRDP](https://github.com/FreeRDP/FreeRDP) — Free remote desktop protocol (RDP) library and clients.
- [Rustdesk](https://rustdesk.com/) — Open source remote desktop infrastructure for displaying and controlling Windows, macOS, Linux, and Android devices.
- [TinyPilot](https://tinypilotkvm.com/) — Tool that enables KVM over IP to control any computer remotely.
- [X2Go](https://wiki.x2go.org/) — Remote desktop software for Linux using a modified NX 3 protocol to give remote access to a system's GUI.
- [Apache Guacamole](https://guacamole.apache.org/) — Clientless remote desktop gateway supporting VNC, RDP, and SSH.
- [Remmina](https://remmina.org/) — Remote access and file sharing client with plugins for RDP, SSH, SPICE, VNC, X2Go, and HTTP/HTTPS.
- [Remotely](https://github.com/immense/Remotely) — Remote control and remote scripting solution built with .NET 6, Blazor, SignalR Core, and WebRTC.
- [P2P Remote Desktop](https://github.com/miroslavpejic85/p2p) — Portable remote desktop tool that needs no configuration or installation.
- [MeshCentral](https://meshcentral.com/) — Web-based computer management server for remotely managing and controlling computers on a local network or over the internet via an installed agent.
- [VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/) — Remote desktop application for iPhone, iPad, Mac, Windows, and Linux.
- [TightVNC](https://www.tightvnc.com/) — Remote desktop application to view and control a remote machine with your local mouse and keyboard.
- [KRDC](https://apps.kde.org/krdc/) — Client application to view or control the desktop session on another machine; supports VNC and RDP.
- [Krfb Desktop Sharing](https://apps.kde.org/krfb/) — Server application to share your current session with a user running a VNC client.
- [wayvnc](https://github.com/any1/wayvnc) — VNC server for wlroots-based Wayland compositors that exposes a single display via the RFB protocol.
- [Waypipe](https://gitlab.freedesktop.org/mstoeckl/waypipe/) — Proxy for Wayland clients that forwards Wayland messages and serializes shared memory buffer changes over a single socket.

## SSH

The Secure Shell Protocol (SSH) is a cryptographic network protocol for operating network services securely over an unsecured network.

- [Advanced SSH config](https://pypi.python.org/pypi/advanced-ssh-config/) — Tool that enhances ssh_config file capabilities transparently.
- [AutoSSH](https://www.harding.motd.ca/autossh/) — Tool that automatically respawns an SSH session after network interruption.
- [ContainersSSH](https://containerssh.io/) — SSH server that launches containers in Kubernetes and Docker on demand.
- [Cluster SSH](https://sourceforge.net/projects/clusterssh/) — Tool that controls a number of xterm windows via a single graphical console.
- [DSH](https://www.netfort.gr.jp/~dancer/software/dsh.html.en) — Dancer's shell / distributed shell for executing multiple remote shell commands from one command line.
- [Flightplan](https://github.com/pstadler/flightplan) — Node.js library for streamlining application deployment or systems administration tasks on local and remote hosts.
- [Mosh](https://mosh.org/) — Command-line program like SSH usable inside xterm, gnome-terminal, urxvt, Terminal.app, iTerm, emacs, screen, or tmux.
- [Parallel SSH](https://parallel-ssh.org/) — Asynchronous parallel SSH library designed for large scale automation.
- [SSH Audit](https://github.com/jtesta/ssh-audit) — Tool for auditing SSH server and client configuration, including banner, key exchange, encryption, MAC, and compression.
- [Sshwifty](https://sshwifty-demo.nirui.org/) — SSH and Telnet connector for the web, deployable on your computer or server to provide access through a standard browser.
- [SSHrc](https://github.com/Russell91/sshrc) — Tool that sources ~/.sshrc on your local computer after logging in remotely.
- [StormSSH](https://stormssh.readthedocs.org) — Command line tool to manage SSH connections.
- [Tailscale SSH](https://tailscale.com/kb/1193/tailscale-ssh/) — Service that lets Tailscale manage the authentication and authorization of SSH connections on your tailnet.

## VPN

A VPN (Virtual Private Network) encrypts your internet traffic on unsecured networks to protect your identity, hide your IP address, and shield your data from third parties.

- [Wireguard](https://www.wireguard.com/) — Minimal, fast VPN solution.
- [OpenVPN](https://community.openvpn.net) — VPN using a custom security protocol that utilizes SSL/TLS for key exchange.
- [Pritunl](https://pritunl.com/) — OpenVPN-based VPN solution.
- [SoftEther](https://www.softether.org/) — Multi-protocol software VPN.
- [sshuttle](https://github.com/apenwarr/sshuttle) — Lightweight VPN-like proxy over SSH.
- [strongSwan](https://www.strongswan.org/) — Complete IPsec implementation for Linux.
- [tinc](https://www.tinc-vpn.org/) — Distributed peer-to-peer VPN.

## LDAP

LDAP (Lightweight Directory Access Protocol) servers store and serve directory information such as users and groups; the tools below run or manage such directories.

- [389 Directory Server](https://port389.org) — Directory server developed by Red Hat.
- [Apache Directory Server](https://directory.apache.org/) — Apache Software Foundation directory server written in Java.
- [Fusion Directory](https://www.fusiondirectory.org) — Management of services and a company directory based on OpenLDAP.
- [OpenDJ](https://opendj.forgerock.org/) — Directory server, a fork of OpenDS.
- [OpenDS](https://opends.java.net/) — Directory server written in Java.
- [OpenLDAP](https://openldap.org/) — Directory server developed by the OpenLDAP Project.
- [Apache Directory Studio](https://directory.apache.org/studio/) — Eclipse-based LDAP browser and directory client.

## Log Management

Tools for collecting, shipping, indexing, analyzing, and visualizing logs and event data.

- [Echofish](https://echothrust.github.io/echofish/) — Web-based real-time event log aggregation, analysis, monitoring, and management system.
- [Fluentd](https://www.fluentd.org/) — Log collector and shipper.
- [Flume](https://flume.apache.org/) — Distributed log collection and aggregation system.
- [Graylog2](https://graylog2.org/) — Pluggable log and event analysis server with alerting options.
- [Heka](https://hekad.readthedocs.org/en/latest/) — Stream processing system that may be used for log aggregation.
- [Elasticsearch](https://www.elasticsearch.org/) — Lucene-based document store used for log indexing, storage, and analysis.
- [Kibana](https://www.elasticsearch.org/overview/kibana/) — Visualizes logs and time-stamped data.
- [Logstash](https://logstash.net/) — Tool for managing events and logs.
- [Octopussy](https://www.octopussy.pm) — Log management solution for visualizing, alerting, and reporting.

## DNS

The Domain Name System (DNS) maps hostnames to IP addresses; this section covers name servers, resolvers, and dynamic-DNS services.

- [Duckdns](https://duckdns.org/) — Free service that points a DNS subdomain of duckdns.org to an IP of your choice.
- [dnsmasq](http://www.thekelleys.org.uk/dnsmasq/doc.html) — Lightweight service providing DNS, DHCP, and TFTP for small-scale networks.
- [MagicDNS](https://tailscale.com/kb/1081/magicdns/) — Tool that automatically registers DNS names for devices in your network.
- [Bind](https://www.isc.org/downloads/bind/) — Widely used name server software.
- [djbdns](http://cr.yp.to/djbdns.html) — Collection of DNS applications, including tinydns.
- [Designate](https://wiki.openstack.org/wiki/Designate) — DNS REST API that supports several DNS servers as its backend.
- [Knot](https://www.knot-dns.cz/) — High performance authoritative-only DNS server.
- [Lexicon](https://github.com/AnalogJ/lexicon) — Tool that manipulates DNS records on multiple DNS providers in a standardized way.
- [NSD](http://www.nlnetlabs.nl/projects/nsd/) — Authoritative-only, high performance name server.
- [PowerDNS](https://www.powerdns.com/) — DNS server with a variety of data storage back-ends and load balancing features.
- [CoreDNS](https://coredns.io/) — DNS server/forwarder written in Go that chains plugins, each performing a DNS function.
- [Unbound](http://unbound.net/) — Validating, recursive, and caching DNS resolver.
- [Yadifa](http://yadifa.eu/) — Lightweight authoritative name server with DNSSEC capabilities.

## Network Tools

A broad set of utilities for messaging, monitoring, proxying, network modeling, and connectivity.

- [MQTT](https://mqtt.org/) — OASIS standard lightweight publish/subscribe messaging protocol for the Internet of Things.
- [Mongoose](https://github.com/cesanta/mongoose) — Networking library for C/C++ with event-driven non-blocking APIs for TCP, UDP, HTTP, WebSocket, and MQTT.
- [Nautobot](https://github.com/nautobot/nautobot) — Network source of truth and network automation platform built on Django with a PostgreSQL or MySQL database.
- [Eclipse Mosquitto](https://github.com/eclipse/mosquitto) — Open source server implementing MQTT versions 5.0, 3.1.1, and 3.1.
- [Ejabberd](https://ejabberd.im/) — Realtime platform built on Erlang/OTP that includes an XMPP server, MQTT broker, and SIP service.
- [Nebula](https://github.com/slackhq/nebula) — Scalable overlay networking tool that connects computers anywhere, running on Linux, OSX, Windows, iOS, and Android.
- [LibreSpeed](https://librespeed.org/) — Network speed test tool that can run on your LAN or be hosted in the cloud.
- [SmokePing](https://oss.oetiker.ch/smokeping/) — Latency measurement tool that measures, stores, and displays latency, latency distribution, and packet loss using RRDtool.
- [Tailnet](https://tailscale.com/kb/1136/tailnet/) — Your private Tailscale network, created on first login, where each device gets a private IP in the CGNAT range and can talk directly to every other device.
- [Tailscale Funnel](https://tailscale.com/kb/1223/tailscale-funnel/) — Feature that routes traffic from the wider internet to one or more of your Tailscale nodes.
- [Cockpit](https://cockpit-project.org/) — Web-based graphical interface for servers that uses your system's normal user logins and privileges, with single-sign-on support.
- [NetBox](https://docs.netbox.dev/) — Solution for modeling and documenting networks, combining IP address management (IPAM) and datacenter infrastructure management (DCIM) with APIs and extensions.
- [Network UPS Tools (NUT)](https://networkupstools.org/) — Project providing a common protocol and tools to monitor and manage power devices such as UPSes, PDUs, and transfer switches.
- [Dnsmasq](https://dnsmasq.org/) — Lightweight network infrastructure tool providing DNS, DHCP, router advertisement, and network boot for small networks.
- [Nginx proxy manager (NPM)](https://nginxproxymanager.com/) — Reverse proxy management system running on Docker that does not require knowledge of Nginx servers or SSL certificates.
- [Netdata](https://github.com/netdata/netdata) — Real-time infrastructure monitoring agent that collects thousands of metrics from systems, hardware, containers, and applications with zero configuration.
- [Pi-hole](https://pi-hole.net/) — DNS sinkhole that blocks unwanted content for devices on a private network without client-side software.
- [OWASP Amass](https://owasp.org/www-project-amass/) — Tool for network mapping of attack surfaces and external asset discovery using open source information gathering and active reconnaissance.
- [Smap](https://github.com/s0md3v/Smap) — Port scanner built on shodan.io's free API that takes the same arguments and produces the same output as Nmap.
- [ORY Oathkeeper](https://github.com/ory/oathkeeper) — Identity and Access Proxy and Access Control Decision API that authorizes HTTP requests based on sets of access rules.
- [Ory Kratos](https://github.com/ory/kratos) — Identity, user management, and authentication system with MFA, FIDO2, TOTP, WebAuthn, profile management, social sign in, registration, and account recovery.
- [Ory Hydra](https://github.com/ory/hydra) — OpenID Certified OAuth 2.0 server and OpenID Connect provider that connects to your existing identity provider through a login and consent app.
- [Ory Keto](https://github.com/ory/keto) — Go implementation of Google's Zanzibar authorization system, shipping gRPC and REST APIs and supporting ACL, RBAC, and other access models.
- [AdGuard Home](https://github.com/AdguardTeam/AdGuardHome) — DNS relay station with ad/tracker blocking, IP address redirections, and DNS-over-HTTPS.
- [NetBird](https://netbird.io/) — Open source VPN management platform built on top of WireGuard for creating secure private networks.
- [Supabase](https://github.com/supabase/supabase) — Open source Firebase alternative built using open source tools.
- [Plik](https://github.com/root-gg/plik) — Scalable temporary file upload system written in Go.
- [Restify](https://github.com/restify/node-restify) — Framework using connect-style middleware for building REST APIs.
- [Traefik](https://traefik.io/traefik/) — Open source edge router that receives requests and automatically discovers the configuration for the services responsible for handling them.
- [Traefik Mesh](https://traefik.io/traefik-mesh) — Container-native service mesh for Kubernetes supporting the Service Mesh Interface (SMI) specification.
- [Trust-DNS](https://github.com/bluejekyll/trust-dns) — Rust-based DNS client, server, and resolver built to be safe and secure.
- [Hugo](https://github.com/gohugoio/hugo) — Static HTML and CSS website generator written in Go that renders a directory of content and templates into a full website.
- [sshuttle](https://github.com/sshuttle/sshuttle) — Transparent proxy server that works as a VPN-like tool forwarding connections over SSH, with DNS tunneling support on Linux and macOS.
- [NetHopper](https://www.nethopper.io/) — Multi-cloud application network as a service for connecting, securing, and monitoring microservices across clusters, sites, clouds, or networks.
- [Cypress](https://cypress.io/) — Tool for testing anything that runs in a browser.
- [Kimchi](https://github.com/kimchi-project/kimchi) — HTML5-based management tool for KVM to create and manage guests.
- [ION](https://github.com/pion/ion) — Distributed real-time communication system for chat across devices.
- [Pimox](https://github.com/pimox/pimox7) — Port of Proxmox to the Raspberry Pi for building a Proxmox cluster of Raspberry Pis or a hybrid cluster of Pis and x86 hardware.
- [PiKVM](https://github.com/pikvm/pikvm) — Raspberry Pi-based KVM over IP.
- [Firezone](https://firezone.dev/) — Self-hosted WireGuard-based VPN server and Linux firewall.
- [Monoid](https://github.com/monoid-privacy/monoid) — Open source suite of tools for automating data privacy.
- [Pinecone](https://matrix-org.github.io/pinecone/) — Experimental overlay routing protocol suite underpinning P2P Matrix demos, providing end-to-end encrypted multi-hop peer-to-peer connectivity over TCP, WebSockets, or Bluetooth Low Energy.

## Service Discovery

Service discovery lets applications and services find and connect to one another automatically; this section covers discovery, coordination, and service-mesh tools.

- [Consul](http://www.consul.io/) — Tool for service discovery, monitoring, and configuration.
- [Linkerd](https://linkerd.io/) — Security-first service mesh for Kubernetes that adds security, observability, and reliability with no code change required.
- [Doozerd](https://github.com/ha/doozerd) — Highly-available, consistent store for small amounts of important data.
- [Admiral](https://github.com/istio-ecosystem/admiral) — Tool that provides automatic configuration and service discovery for multicluster Istio service mesh.
- [ScaleCube](https://github.com/scalecube/scalecube-services) — Embeddable microservices library that connects distributed microservices and simplifies asynchronous programming.
- [DPS (dns-proxy-server)](https://github.com/mageddo/dns-proxy-server) — Lightweight DNS server for service discovery that resolves hostnames from local configuration and Docker containers, with a graphic interface for managing A/CNAME records.
- [ZooKeeper](http://zookeeper.apache.org/) — Centralized service for maintaining configuration information, naming, distributed synchronization, and group services.
