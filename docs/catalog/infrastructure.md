# Infrastructure & Platform

Tools for building and operating the platform layer of a self-hosted stack: containers and orchestration, CI/CD pipelines, development and provisioning, web servers, self-hosted LLMs, automation engines, configuration management, cloud storage and platforms, object storage, and virtualization.

[← Catalog index](./README.md) · [← Handbook home](../../README.md)

## Containers

A container packages application code with all its dependencies so it runs consistently across computing environments. A container image is the standalone, executable package that includes the code, runtime, system tools, libraries, and settings.

- [DockerHub Container Images](https://hub.docker.com/search?image_filter=official&q=&type=image) — registry of official Docker container images.
- [LinuxServer.io Container Images](https://fleet.linuxserver.io/) — community-maintained collection of container images.
- [Quay Container Images](https://quay.io/search) — searchable registry of container images.
- [Docker Compose](https://github.com/docker/compose) — tool to define and run multi-container applications from a YAML file with a single command.
- [Docker Include](https://docs.docker.com/compose/compose-file/14-include/) — Compose feature that lets one Compose application declare a dependency on another to reuse Compose files.
- [Kompose](https://kompose.io/) — conversion tool from Docker Compose to orchestrators such as Kubernetes or OpenShift.
- [Kubernetes](https://kubernetes.io/) — container orchestration platform.
- [OpenShift](https://openshift.com/) — container application platform.
- [SwarmKit](https://github.com/moby/swarmkit) — toolkit for orchestrating distributed systems with node discovery, raft-based consensus, and task scheduling.
- [Containerd](https://containerd.io/) — daemon that manages the complete container lifecycle on Linux and Windows, from image transfer and storage to execution and networking.
- [ContainerSSH](https://containerssh.io/) — SSH server that launches containers in Kubernetes and Docker on demand.
- [Podman](https://podman.io/) — daemonless, Linux-native tool to find, run, build, share, and deploy OCI containers with a Docker-compatible CLI.
- [Lima](https://github.com/lima-vm/lima) — launches Linux virtual machines with automatic file sharing, port forwarding, and containerd; an open-source alternative to Docker Desktop.
- [Colima](https://github.com/abiosoft/colima) — container runtimes on macOS and Linux with minimal setup.
- [Portainer Community Edition](https://github.com/portainer/portainer) — service delivery platform to manage Docker, Swarm, Kubernetes, and ACI environments.
- [Yacht](https://github.com/SelfhostedPro/Yacht) — container management UI focused on templates and one-click deployments.
- [Kitematic](https://kitematic.com/) — GUI for managing Docker containers on Mac, Linux, and Windows.
- [HashiCorp Nomad](https://www.nomadproject.io/) — scheduler and orchestrator for containerized and non-containerized applications across on-premises and clouds.
- [Open Container Initiative](https://opencontainers.org/about/overview/) — open governance structure for industry standards around container formats and runtimes.
- [OpenNebula](https://opennebula.io/) — open-source platform to build and manage enterprise clouds for virtualized services, containerized applications, and serverless computing.
- [Buildah](https://buildah.io/) — command-line tool to build OCI images, usable with Docker, Podman, and Kubernetes.
- [Red Hat Universal Base Images (UBI)](https://developers.redhat.com/products/rhel/ubi) — OCI-compliant base images built on Red Hat Enterprise Linux software, freely redistributable.
- [Red Hat Quay](https://quay.io/) — builds, stores, and distributes applications and containers.
- [ctop](https://ctop.sh/) — terminal overview of real-time metrics for multiple containers, with built-in support for Docker and runC.
- [runc](https://github.com/opencontainers/runc) — CLI tool for spawning and running containers on Linux per the OCI specification.
- [container-images](https://github.com/opencontainers/container-images) — collection of container images used in CI across OpenContainers projects.
- [Clair](https://github.com/quay/clair) — static analysis of vulnerabilities in OCI and Docker application containers.
- [Shipwright](https://github.com/SelfhostedPro/Shipwright) — web UI to generate templates for Yacht, Portainer, Docker-Compose, and Unraid.
- [Alnoda Workspaces](https://docs.alnoda.org/) — portable, browser-based development environments running in Docker containers.
- [Autoheal](https://hub.docker.com/r/willfarrell/autoheal) — monitors and restarts unhealthy Docker containers.
- [Dozzle](https://hub.docker.com/r/amir20/dozzle) — web interface for live monitoring of Docker logs without storing log files.
- [Diun](https://crazymax.dev/diun/) — sends notifications when a Docker image is updated on a registry.
- [WatchTower](https://hub.docker.com/r/containrrr/watchtower) — automates Docker container base image updates.
- [Kasm Workspaces](https://www.kasmweb.com/) — container streaming platform to deliver containerized desktops and applications over the web.
- [Nginx Proxy](https://github.com/nginx-proxy/nginx-proxy) — automation that runs nginx with docker-gen to generate reverse proxy configs and reload as containers start and stop.
- [Visual Studio Code Dev Containers](https://github.com/microsoft/vscode-dev-containers) — extension that uses a Docker container as a full development environment defined by a devcontainer.json file.

## CI/CD

CI/CD stands for Continuous Integration and Continuous Delivery: automated pipelines that build, test, and ship code changes.

- [Drone](https://drone.io/) — continuous delivery system built on container technology, configured with a YAML file and run inside Docker containers.
- [Woodpecker](https://woodpecker-ci.org/) — CI service that is a community fork of Drone.
- [Travis CI](https://travis-ci.org/) — hosted continuous integration service to build and test projects hosted on GitHub.
- [Circle CI](https://circleci.com/) — continuous integration and continuous delivery platform.
- [Buddy](https://buddy.works/) — DevOps platform with CI/CD tooling.
- [Buildbot](https://www.buildbot.net/) — continuous integration tool that queues and executes compile or test jobs and reports results.

## Development & Provisioning

Tools for development environments, source control hosting, project management, and provisioning infrastructure.

- [Proxmox VE (Virtual Environment)](https://www.proxmox.com/en/proxmox-ve) — open-source virtualization platform with a web interface to manage VMs, containers, storage, networking, and clustering.
- [Terraform provider plugin for Proxmox](https://github.com/Telmate/terraform-provider-proxmox) — Terraform provider that provisions QEMU VMs and LXC containers on Proxmox.
- [OTF](https://github.com/leg100/otf) — open-source alternative to Terraform Enterprise with SSO, team management, and agents.
- [Semaphore UI](https://github.com/ansible-semaphore/semaphore) — web UI for running Ansible playbooks, getting failure notifications, and controlling access.
- [APITable](https://apitable.com/) — API-oriented low-code platform for building collaborative apps; an Airtable alternative.
- [Chisel Kubernetes Operator](https://github.com/FyraLabs/chisel-operator/) — Kubernetes operator that uses Chisel as a LoadBalancer provider for a cluster.
- [Docker-pgautoupgrade](https://github.com/pgautoupgrade/docker-pgautoupgrade) — PostgreSQL Docker container that detects the existing data directory version and upgrades it automatically.
- [IT-Tools](https://it-tools.tech/) — collection of online tools for developers.
- [Lazygit](https://github.com/jesseduffield/lazygit) — terminal UI for git commands, written in Go.
- [LazyDocker](https://github.com/jesseduffield/lazydocker) — terminal UI for Docker and docker-compose, written in Go.
- [Code-Server](https://github.com/coder/code-server) — Visual Studio Code running on a remote server, accessible through the browser.
- [Turbopilot](https://github.com/ravenscroftj/turbopilot) — open-source code completion engine that runs locally on the CPU.
- [Self-Hosted Sentry](https://develop.sentry.dev/self-hosted/) — official bootstrap for running your own Sentry with Docker.
- [Visual Studio Live Share](https://visualstudio.microsoft.com/services/live-share/) — extension for collaborative real-time editing and debugging, with shared terminals, port forwarding, and voice calls.
- [GistPad](https://marketplace.visualstudio.com/items?itemName=vsls-contrib.gistfs) — VS Code extension to edit GitHub Gists and repositories without cloning.
- [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) — VS Code extension that launches a local development server with live reload.
- [Act](https://github.com/nektos/act) — tool to run GitHub Actions locally.
- [Act runner](https://gitea.com/gitea/act_runner) — runner for Gitea based on act.
- [GitLab](https://about.gitlab.com/) — open-source software development platform with version control, issue tracking, code review, and CI/CD, self-hostable on your own servers or cloud.
- [Bonobo Git Server](https://bonobogitserver.com/) — self-hosted git server on IIS for Windows with a graphical interface for user and repository management.
- [Fossil](https://www.fossil-scm.org/index.html/doc/trunk/www/index.wiki) — distributed version control system with a built-in wiki and bug tracker.
- [Gerrit](https://www.gerritcodereview.com/) — code review and project management tool for Git-based projects.
- [Gitblit](https://www.gitblit.com/) — pure Java stack for managing, viewing, and serving Git repositories.
- [gitbucket](https://gitbucket.github.io/gitbucket-news/) — GitHub clone powered by Scala.
- [Gitea](https://gitea.io) — community-managed fork of Gogs; a lightweight code hosting solution.
- [Gitlist](https://gitlist.org/) — web-based git repository browser for viewing files, commit history, and diffs.
- [Gitolite](https://gitolite.com/gitolite/index.html) — git hosting on a central server with fine-grained access control.
- [GitPrep](https://github.com/yuki-kimoto/gitprep) — portable GitHub clone.
- [Gogs](https://gogs.io/) — self-hosted Git service written in Go.
- [Kallithea](https://kallithea-scm.org/) — source code management system supporting Mercurial and Git with a web interface.
- [Klaus](https://github.com/jonashaag/klaus) — simple, easy-to-set-up Git web viewer.
- [Lavagna](https://lavagna.io) — open-source issue and project management tool for small teams, written in Java.
- [Leantime](https://leantime.io) — lean project management system for small teams and startups.
- [Taiga](https://taiga.io/) — open-source project management software supporting scrum and kanban frameworks.
- [Planka](https://planka.app/) — realtime kanban board for workgroups built with React and Redux.
- [Microgit](https://github.com/microgit-com/microgit) — git hosting service written in Crystal and Lucky.
- [OneDev](https://onedev.io/) — DevOps platform with git management, issue tracking, and CI/CD.
- [OpenProject](https://www.openproject.org) — web-based project management system.
- [Pagure](https://pagure.io/pagure) — git-centric forge with features for federated and decentralized development.
- [Phorge](https://we.phorge.it/) — community-driven platform for collaborating on and reviewing software development projects.
- [Redmine](https://www.redmine.org/) — flexible project management web application.
- [RhodeCode](https://rhodecode.com/) — platform that unifies repository management for Git, Subversion, and Mercurial.
- [SCM Manager](https://www.scm-manager.org/) — share and manage Git, Mercurial, and Subversion repositories over HTTP.
- [Titra](https://titra.io/) — time-tracking solution for freelancers and small teams.
- [Traq](https://traq.io/) — project management and issue tracking system written in PHP.
- [Tuleap](https://www.tuleap.org/) — suite to plan, track, code, and collaborate on software projects.
- [UVDesk](https://www.uvdesk.com/) — service-oriented, event-driven open-source helpdesk system.
- [ZenTao](https://www.zentao.pm/) — agile (scrum) project management system.
- [k3s-ansible](https://github.com/techno-tim/k3s-ansible) — automated install of a high-availability k3s Kubernetes cluster with kube-vip and MetalLB.
- [Soft Serve](https://github.com/charmbracelet/soft-serve) — self-hostable Git server for the command line.
- [Coolify](https://coolify.io/) — open-source, self-hostable Heroku/Netlify alternative.
- [Corosync Cluster Engine](https://corosync.github.io/corosync/) — group communication system for implementing high availability within applications.
- [Glow](https://github.com/charmbracelet/glow) — terminal-based markdown reader for browsing documentation on the command line.
- [Deep Lake](https://github.com/activeloopai/deeplake) — data lake for deep learning with a dataset format optimized for streaming and querying while training models at scale.
- [Node-Red](https://nodered.org/) — low-code programming for event-driven applications.
- [krunvm](https://github.com/containers/krunvm) — CLI utility for creating microVMs from OCI images using libkrun and buildah.
- [Zeal](https://zealdocs.org/) — offline documentation browser for software developers.

## Web Servers

Software that serves web content and handles HTTP traffic, plus reverse proxies and caches that optimize web performance.

- [Apache](https://httpd.apache.org/) — widely used web server.
- [OpenResty Manager](https://om.uusec.com/) — open-source manager for OpenResty, an Nginx-enhanced version.
- [Beakon](https://github.com/RealDudePerson/beakon) — self-hosted location sharing webserver designed to leak as little data as possible.
- [Caddy](https://caddyserver.com/) — HTTP/2 web server with fully managed TLS.
- [Cherokee](https://cherokee-project.com/) — lightweight web server and reverse proxy.
- [Lighttpd](https://www.lighttpd.net/) — web server optimized for speed-critical environments.
- [Nginx](https://nginx.org/) — reverse proxy, load balancer, HTTP cache, and web server.
- [uWSGI](https://github.com/unbit/uwsgi/) — full stack for building hosting services.
- [HAProxy](https://www.haproxy.org/) — software load balancer with SSL offloading, compression, and web routing.
- [Squid](https://www.squid-cache.org/) — caching proxy for the web supporting HTTP, HTTPS, and FTP.
- [Traefik](https://traefik.io/) — HTTP reverse proxy and load balancer for deploying microservices.
- [Varnish](https://www.varnish-cache.org/) — HTTP web application accelerator focused on caching and compression.

## Self-Hosted LLMs & AI

Large language models generate text using neural networks. The tools below run models and chat interfaces locally or on your own servers; consult each project's documentation for hardware requirements and setup steps.

- [LLM-Leaderboard](https://github.com/LudwigStumpp/llm-leaderboard) — community leaderboard comparing language models.
- [Open LLM Leaderboard by Hugging Face](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard) — leaderboard ranking open LLMs.
- [Holistic Evaluation of Language Models (HELM)](https://crfm.stanford.edu/helm/latest/?groups=1) — benchmark for evaluating language models.
- [llama.cpp](https://github.com/ggerganov/llama.cpp) — port of the LLaMA model in C/C++ for local inference.
- [ollama](https://ollama.ai/) — tool to run Llama 2 and other large language models locally.
- [LocalAI](https://localai.io/) — self-hosted, OpenAI-compatible API that runs ggml-compatible models on consumer hardware with no GPU required.
- [Serge](https://github.com/serge-chat/serge) — self-hosted, dockerized web interface for chatting with Alpaca through llama.cpp.
- [OpenLLM](https://github.com/bentoml/OpenLLM) — platform to fine-tune, serve, deploy, and monitor large language models in production.
- [Llama-gpt](https://github.com/getumbrel/llama-gpt) — self-hosted, offline, ChatGPT-like chatbot powered by Llama 2.
- [Llama2 webui](https://github.com/liltom-eth/llama2-webui) — runs Llama 2 locally with a Gradio UI on GPU or CPU.
- [Llama2.c](https://github.com/karpathy/llama2.c) — trains the Llama 2 architecture in PyTorch and runs inference with a single C file.
- [Alpaca.cpp](https://github.com/antimatter15/alpaca.cpp) — runs a ChatGPT-like model locally, combining the LLaMA model with a fine-tuned reproduction of Stanford Alpaca and a llama.cpp chat interface.
- [GPT4All](https://github.com/nomic-ai/gpt4all) — ecosystem of open-source chatbots trained on assistant data, based on LLaMa.
- [GPT4All UI](https://github.com/nomic-ai/gpt4all-ui) — Flask web application providing a chat UI for the GPT4All chatbot.
- [MiniGPT-4](https://minigpt-4.github.io/) — vision-language understanding with large language models.
- [LoLLMS WebUI](https://github.com/ParisNeo/lollms-webui) — web interface to access and use various LLM models for writing, coding, data, and image tasks.
- [LM Studio](https://lmstudio.ai/) — desktop app to discover, download, and run local LLMs.
- [Gradio Web UI (text-generation-webui)](https://github.com/oobabooga/text-generation-webui) — web UI for LLMs, supporting transformers, GPTQ, and llama.cpp models.
- [OpenPlayground](https://github.com/nat/openplayground) — playground for running ChatGPT-like models locally.
- [Vicuna](https://vicuna.lmsys.org/) — open-source chatbot trained by fine-tuning LLaMA.
- [Yeagar ai](https://github.com/yeagerai/yeagerai-agent) — Langchain agent creator to build, prototype, and deploy AI-powered agents.
- [KoboldCpp](https://github.com/LostRuins/koboldcpp) — AI text-generation software for GGML models, built on llama.cpp with a Kobold API endpoint and UI.
- [Minima](https://github.com/dmayboroda/minima) — configurable conversational RAG system that runs an LLM locally and on-premises using containers.
- [Chatbot UI](https://github.com/mckaywrigley/chatbot-ui) — chatbot kit for OpenAI chat models built with Next.js, TypeScript, and Tailwind CSS, with locally stored conversations.
- [Chatbot UI Lite](https://github.com/mckaywrigley/chatbot-ui-lite) — simple chatbot starter kit for OpenAI chat models using Next.js, TypeScript, and Tailwind CSS.
- [DoctorGPT](https://github.com/ingyamilmolinar/doctorgpt) — self-contained binary that monitors application logs for problems and diagnoses them.
- [HttpGPT](https://github.com/lucoiso/UEHttpGPT/releases) — Unreal Engine 5 plugin for integrating OpenAI GPT and DALL-E services through asynchronous REST requests.

## Automation

Tools that automate workflows, tasks, and media management, often as self-hosted alternatives to services like Zapier and IFTTT.

- [Accelerated Text](https://github.com/accelerated-text/accelerated-text) — generates natural language descriptions of data varying in wording and structure.
- [Activepieces](https://www.activepieces.com) — no-code business automation tool; an open-source Zapier or Tray alternative.
- [ActiveWorkflow](https://github.com/automaticmode/active_workflow) — process and workflow automation platform based on software agents.
- [Alltube](https://github.com/Rudloff/alltube) — web GUI for youtube-dl to download video and audio from many websites.
- [AmIUnique](https://amiunique.org/) — browser fingerprinting tool that shows how identifiable you are online.
- [Automatisch](https://automatisch.io) — business automation tool connecting services like Twitter and Slack; an open-source Zapier alternative.
- [Baserow](https://baserow.io/) — open-source online database tool and Airtable alternative.
- [betanin](https://github.com/sentriz/betanin) — music organization tool between your torrent client and music player, based on beets.io.
- [ChiefOnboarding](https://chiefonboarding.com) — employee onboarding platform with provisioning, sequences, and a Slack bot.
- [Datasette](https://datasette.io/) — open-source tool for exploring and publishing data with import, export, and database management.
- [Eonza](https://www.eonza.org) — tool to create scripts and automate tasks on servers, managed from any browser.
- [Exadel CompreFace](https://exadel.com/solutions/compreface/) — face recognition system with a REST API, deployable with Docker and SDKs for Python and JavaScript.
- [feed2toot](https://feed2toot.readthedocs.io/en/latest/) — parses an RSS feed and sends the latest entries to Mastodon.
- [feedmixer](https://github.com/cristoper/feedmixer) — WSGI micro web service that merges recent entries from a list of feeds into a new Atom, RSS, or JSON feed.
- [Headphones](https://github.com/rembo10/headphones) — automated music downloader for NZB and Torrent, written in Python.
- [Healthchecks](https://healthchecks.io/) — Django app that listens for pings and sends alerts when they are late.
- [HRConvert2](https://github.com/zelon88/HRConvert2) — drag-and-drop file conversion server with session-based authentication and logging.
- [Huginn](https://github.com/huginn/huginn) — build agents that monitor and act on your behalf.
- [Kibitzr](https://kibitzr.github.io) — lightweight personal web assistant with integrations.
- [Krayin](https://krayincrm.com/) — open-source Laravel CRM application.
- [Leon](https://getleon.ai) — open-source personal assistant that runs on your server.
- [Lidarr](https://lidarr.audio/) — music collection manager for Usenet and BitTorrent users.
- [Matchering](https://github.com/sergree/matchering) — containerized web app for automated music mastering.
- [Medusa](https://pymedusa.com/) — automatic video library manager for TV shows.
- [MeTube](https://github.com/alexta69/metube) — web GUI for youtube-dl with playlist support.
- [Nautobot](https://github.com/nautobot/nautobot) — network source of truth and automation platform built on Django.
- [nefarious](https://github.com/lardbit/nefarious) — web application that automates downloading movies and TV shows.
- [NocoDB](https://www.nocodb.com/) — no-code platform that turns any database into a spreadsheet; an Airtable alternative.
- [OliveTin](https://github.com/OliveTin/OliveTin) — web interface for running Linux shell commands.
- [Patrowl](https://github.com/Patrowl/PatrowlManager) — open-source security operations orchestration platform.
- [Podgrab](https://github.com/akhilrex/podgrab) — podcast manager that automatically downloads new episodes.
- [pyLoad](https://pyload.net/) — remotely manageable downloader for one-click-hosting sites.
- [Radarr](https://radarr.video/) — fork of Sonarr for automatically downloading movies via Usenet and BitTorrent.
- [SickRage](https://www.sickrage.ca) — automatic video library manager for TV shows with torrent/nzb searching and processing.
- [SiteInspector](https://www.getsiteinspector.com/) — web tool for catching spelling errors, grammatical errors, and broken links.
- [Sonarr](https://sonarr.tv/) — automatic TV show downloader and manager for Usenet and BitTorrent.
- [StackStorm](https://stackstorm.com) — event-driven automation with a rules engine, workflows, and integration packs.
- [µTask](https://github.com/ovh/utask) — automation engine that models and executes business processes declared in YAML.

## Configuration Management

Tools that define, deploy, and maintain the desired state of servers and infrastructure, often through declarative code.

- [Ansible](https://www.ansible.com/) — agentless automation tool written in Python, with enterprise support from Red Hat.
- [Ansible.Ai](https://ansible.ai/) — AI tool that generates syntactically correct Ansible playbooks.
- [CFEngine](https://cfengine.com/) — lightweight agent system where configuration state is specified via a declarative language.
- [mgmt](https://github.com/purpleidea/mgmt) — config management tool written in Go.
- [Pallet](https://palletops.com/) — infrastructure definition, configuration, and management via a Clojure DSL.
- [Puppet](https://puppetlabs.com/) — automated engine that performs administrative tasks based on a centralized specification for Linux, Unix, and Windows.
- [Chef](https://www.opscode.com/chef/) — automation platform that turns infrastructure into code across environments.
- [(R)?ex](https://www.rexify.org/) — automation framework supporting local and remote execution with imperative or declarative approaches.
- [Salt](https://www.saltstack.com/) — event-driven automation tool to deploy, configure, and manage IT systems in a consistent desired state.
- [Fleek](https://getfleek.dev/) — management system for your computer setup.

## Cloud Storage

Self-hosted file synchronization and storage platforms.

- [Swift](https://docs.openstack.org/developer/swift/) — distributed, eventually consistent object/blob store.
- [Syncthing](https://syncthing.net/) — open-source system for private, encrypted, authenticated distribution of data.
- [git-annex assistant](https://git-annex.branchable.com/assistant/) — synchronized folder across computers, devices, drives, NAS appliances, and cloud services.
- [NextCloud](https://nextcloud.com) — provides access to your files via the web.
- [ownCloud](https://owncloud.org) — provides access to your files via the web, desktop, or mobile.
- [Seafile](https://seafile.com) — open-source cloud storage solution.
- [SparkleShare](https://sparkleshare.org/) — cloud storage and file synchronization using Git as a storage backend.

## Cloud Platforms

Cloud hosting providers and the collaboration platforms commonly deployed on them, with their associated tooling.

- [Linode](https://www.linode.com/) — cloud hosting company providing virtual private servers and other cloud services.
- [Linode Cloud Manager](https://www.linode.com/products/cloud-manager/) — interface to deploy and manage virtual machines, networking, and user accounts.
- [Linode API](https://developers.linode.com/api/v4/) — programmatic access to configure and deploy Linode products and services.
- [Linode CLI](https://www.linode.com/docs/cli/) — command-line tool to deploy and manage Linux servers on Linode.
- [Linode Images](https://www.linode.com/products/images/) — service to capture, store, and deploy custom images across Linodes and data centers.
- [Linode Integrations](https://www.linode.com/products/integrations/) — integrations connecting infrastructure and dev tools to the Linode platform.
- [StackScripts](https://www.linode.com/products/stackscripts/) — scripts to automatically configure new Linode instances.
- [Linode Bare Metal](https://www.linode.com/products/bare-metal/) — single-tenant solution combining direct hardware access with virtual machine flexibility.
- [Nextcloud](https://nextcloud.com) — open-source, on-premises content collaboration platform for file sync, share, and communication.
- [Nextcloud Hub](https://nextcloud.com/hub/) — on-premises tool to share and collaborate on documents, email, calendar, and video chats.
- [Nextcloud AIO (All In One)](https://github.com/nextcloud/all-in-one) — all-in-one deployment that bundles most Nextcloud features into a single instance.
- [Nextcloud Desktop Client](https://nextcloud.com/install/#install-clients) — synchronizes files from a Nextcloud server with your computer.
- [Nextcloud Deck](https://apps.nextcloud.com/apps/deck) — kanban-style organization tool integrated with Nextcloud.
- [Nextcloud Files](https://nextcloud.com/files/) — file access, sharing, and collaboration for teams, customers, and partners.
- [Nextcloud Talk](https://nextcloud.com/talk/) — team communication platform that keeps data and metadata on your servers.
- [Nextcloud Home](https://nextcloud.com/athome/) — store documents, calendar, contacts, and photos on your own server.
- [Nextcloud Enterprise](https://nextcloud.com/enterprise/) — software optimized and tested for mission-critical environments.
- [Nextcloud Outlook Integration](https://nextcloud.com/outlook/) — uploads files and integrates calendars and contacts in Microsoft Outlook.
- [Collabora Online in Nextcloud](https://nextcloud.com/collaboraonline/) — LibreOffice-based online office suite with collaborative editing.
- [ONLYOFFICE integration in Nextcloud](https://nextcloud.com/onlyoffice/) — real-time collaboration on office documents with Microsoft Office format compatibility.
- [Nextcloud VM](https://download.nextcloudvm.com/) — scripts that guide a quality-controlled installation of a Nextcloud instance, including for Raspberry Pi 4.
- [LibreSign](https://libresign.github.io/) — digital signature app for Nextcloud.
- [DigitalOcean](https://www.digitalocean.com/) — cloud infrastructure provider offering services to deploy and scale applications across worldwide data centers.
- [DigitalOcean API](https://developers.digitalocean.com/documentation/v2/) — RESTful API to manage DigitalOcean infrastructure.
- [DigitalOcean Client libraries](https://developers.digitalocean.com/libraries/) — libraries to use the DigitalOcean API in various programming languages.
- [DigitalOcean CLI](https://github.com/digitalocean/doctl) — open-source command-line interface for managing DigitalOcean infrastructure.
- [Terraform provider](https://www.terraform.io/docs/providers/do/index.html) — manage DigitalOcean infrastructure as code with Terraform.
- [DigitalOcean Custom images](https://www.digitalocean.com/docs/images/custom-images/) — provision servers with a custom image or a Linux distribution.
- [Container Registry](https://www.digitalocean.com/products/container-registry/) — stores, manages, and protects private container images.

## Object Storage & Web Deployment

Container-based web deployment and S3-compatible object storage platforms.

- [Back4app Web Deployment](https://www.back4app.com/web-deployment-platform) — Container as a Service platform to build and deploy containerized applications connected to a GitHub repository.
- [MinIO](https://min.io/download) — high-performance object storage released under AGPL v3.0 and API-compatible with Amazon S3, usable as the main storage tier for Spark, TensorFlow, Presto, Hadoop HDFS, and H2O workloads.

## Virtualization

Hypervisors, virtual machine managers, and the virtualization technologies (including network functions virtualization) used to run and isolate workloads.

- [HVM (Hardware Virtual Machine)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/virtualization_types.html) — virtualization type that runs an OS directly on a virtual machine as if on bare-metal hardware.
- [PV (ParaVirtualization)](https://wiki.xenproject.org/wiki/Paravirtualization_(PV)) — lightweight virtualization technique from the Xen Project that does not require host CPU virtualization extensions.
- [Network functions virtualization (NFV)](https://www.vmware.com/topics/glossary/content/network-functions-virtualization-nfv) — replaces network appliance hardware with virtual machines running networking software on a hypervisor.
- [Software Defined Networking (SDN)](https://www.vmware.com/topics/glossary/content/software-defined-networking) — networking approach that uses software controllers or APIs to direct traffic and communicate with underlying hardware.
- [Virtualized Infrastructure Manager (VIM)](https://www.cisco.com/c/en/us/td/docs/net_mgmt/network_function_virtualization_Infrastructure/3_2_2/install_guide/Cisco_VIM_Install_Guide_3_2_2/Cisco_VIM_Install_Guide_3_2_2_chapter_00.html) — lifecycle management of the software and hardware in NFV infrastructure, with a live inventory of physical and virtual resources.
- [Management and Orchestration (MANO)](https://www.etsi.org/technologies/open-source-mano) — ETSI-hosted Open Source NFV Management and Orchestration software stack.
- [Magma](https://www.magmacore.org/) — open-source platform giving network operators a flexible, extendable mobile core network solution across 2G–5G and access networks.
- [OpenRAN](https://open-ran.org/) — intelligent Radio Access Network on general-purpose platforms with open interfaces for multi-vendor deployments.
- [Open vSwitch (OVS)](https://www.openvswitch.org/) — multilayer virtual switch designed for network automation while supporting standard management protocols.
- [Edge](https://www.ibm.com/cloud/what-is-edge-computing) — distributed computing framework that brings enterprise applications closer to data sources such as IoT devices.
- [Multi-access edge computing (MEC)](https://www.etsi.org/technologies/multi-access-edge-computing) — ETSI specification group creating a standardized environment for integrating applications across multi-vendor edge platforms.
- [Virtualized network functions (VNFs)](https://www.juniper.net/documentation/en_US/cso4.1/topics/concept/nsd-vnf-overview.html) — software applications providing networking functions within an NFV implementation.
- [Cloud-Native Network Functions (CNF)](https://www.cncf.io/announcements/2020/11/18/cloud-native-network-functions-conformance-launched-by-cncf/) — network functions designed to run inside containers with Kubernetes lifecycle management.
- [Physical Network Function (PNF)](https://www.mpirical.com/glossary/pnf-physical-network-function) — physical network node that has not undergone virtualization.
- [Network functions virtualization infrastructure (NFVI)](https://docs.vmware.com/en/VMware-vCloud-NFV/2.0/vmware-vcloud-nfv-reference-architecture-20/GUID-FBEA6C6B-54D8-4A37-87B1-D825F9E0DBC7.html) — physical compute, storage, and networking hardware that hosts VNFs.
- [Virtualization-based Security (VBS)](https://docs.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-vbs) — hardware virtualization feature that isolates a secure region of memory from the OS.
- [Hypervisor-Enforced Code Integrity (HVCI)](https://docs.microsoft.com/en-us/windows-hardware/drivers/bringup/device-guard-and-credential-guard) — uses hardware virtualization so a hypervisor protects kernel-mode processes against malicious code.
- [NVIDIA virtual GPU (vGPU)](https://www.nvidia.com/en-us/data-center/virtual-solutions/) — software enabling GPU performance for virtual workstations, data science, and AI workloads.
- [AMD MxGPU](https://www.amd.com/en/graphics/workstation-virtual-graphics) — hardware-based virtualized GPU solution built on SR-IOV for multiple users per physical GPU.
- [Proxmox Virtual Environment (VE)](https://www.proxmox.com/en/) — open-source platform for enterprise virtualization with a web interface for VMs, containers, storage, and clustering.
- [KVM (Kernel-based Virtual Machine)](https://www.linux-kvm.org/page/Main_Page) — full virtualization solution for Linux on x86 hardware with virtualization extensions.
- [QEMU](https://www.qemu.org) — processor emulator that emulates a full system, usable to run a different OS or debug system code.
- [Quickemu](https://github.com/wimpysworld/quickemu) — quickly creates and runs optimized Windows, macOS, and Linux desktop virtual machines.
- [Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/) — runs virtualized computer systems on a physical host managed by a hypervisor.
- [Cloud Hypervisor](https://github.com/cloud-hypervisor/cloud-hypervisor) — open-source Virtual Machine Monitor on top of KVM, implemented in Rust and focused on modern cloud workloads.
- [VirtManager](https://github.com/virt-manager/virt-manager) — graphical tool for managing virtual machines via libvirt, mainly QEMU/KVM.
- [oVirt](https://www.ovirt.org) — open-source distributed virtualization solution using the KVM hypervisor with a web-based front-end.
- [Firecracker](http://firecracker-microvm.io/) — virtualization technology for secure, multi-tenant container and function-based services running in lightweight microVMs.
- [Foreman](https://theforeman.org/) — open-source project to automate tasks, deploy applications, and manage server lifecycle on-premises or in the cloud.
- [Harvester](https://harvesterhci.io/) — open-source hyper-converged infrastructure software built on Kubernetes.
- [Anthos](https://cloud.google.com/anthos/docs/concepts/overview) — application management platform providing a consistent experience across cloud and on-premises environments.
- [OpenNebula](https://opennebula.io/) — open-source platform to build and manage enterprise clouds for virtualized services, containerized applications, and serverless computing.
- [HyperKit](https://github.com/moby/hyperkit) — toolkit for embedding hypervisor capabilities, optimized for lightweight VMs and container deployment on macOS.
- [Intel Graphics Virtualization Technology (Intel GVT)](https://github.com/intel/gvt-linux) — full GPU virtualization solution with mediated pass-through for multiple guest virtual machines.
- [Apple Hypervisor](https://developer.apple.com/documentation/hypervisor) — framework to build virtualization solutions on a lightweight hypervisor with C APIs in user space.
- [Apple Virtualization Framework](https://developer.apple.com/documentation/virtualization) — high-level APIs for creating and managing virtual machines on Apple silicon and Intel Macs.
- [Apple Paravirtualized Graphics Framework](https://developer.apple.com/documentation/paravirtualizedgraphics) — implements hardware-accelerated graphics for macOS running in a virtual machine.
- [Cilicon](https://github.com/traderepublic/Cilicon) — macOS app using Apple's Virtualization Framework to create and run ephemeral virtual machines for self-hosted CI.
- [Xen](https://github.com/xen-project/xen) — virtualization project for server virtualization, IaaS, desktop virtualization, security, and embedded applications.
- [Ganeti](https://github.com/ganeti/ganeti) — virtual machine cluster management tool built on Xen or KVM.
- [Packer](https://www.packer.io/) — tool for creating identical machine images for multiple platforms from a single source configuration.
- [Vagrant](https://www.vagrantup.com/) — tool for building and managing reproducible virtual machine environments in a single workflow.
