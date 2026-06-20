# Media, Home Server & Home Automation

This page catalogs self-hostable software for running a home server, streaming media, automating a smart home, and related areas such as photos, podcasts, maps, and gaming. Each entry links to the project and gives a short factual description.

[← Catalog index](./README.md) · [← Handbook home](../../README.md)

## Home Server

Software for running services and managing storage on a machine you control, such as a NAS or a Raspberry Pi.

- [Home Assistant](https://www.home-assistant.io/) — Open-source home automation platform focused on local control and privacy; runs on Raspberry Pi.
- [Homebridge](https://homebridge.io/) — Framework that integrates smart home devices lacking native HomeKit support, with over 2,000 plugins.
- [Homebridge UI](https://github.com/oznu/homebridge-config-ui-x) — Web interface to manage Homebridge plugins, configuration, and accessories.
- [ESPHome](https://esphome.io/) — System to control ESP8266/ESP32 devices via configuration files and integrate them with home automation systems.
- [Shelly Cloud](https://shelly.cloud/) — Smart home control and monitoring for Shelly devices, compatible with Alexa, Google Home, Android, and iOS.
- [Zigbee](https://csa-iot.org/all-solutions/zigbee/) — Wireless protocol used by many large smart home ecosystems including Amazon Echo Plus, Samsung SmartThings, and Philips Hue.
- [openHAB](https://github.com/openhab) — Cross-platform software to integrate various smart home technologies and devices.
- [Z-Wave](https://www.z-wave.com/) — Wireless communications protocol used by many smart home brands.
- [Homey](https://homey.app/) — Application to control, automate, and monitor a smart home from phone, tablet, or desktop.
- [Caddy](https://caddyserver.com/) — Web server that obtains and renews TLS certificates and serves over HTTPS automatically.
- [Bazarr](https://hub.docker.com/r/linuxserver/bazarr) — Companion application to Sonarr and Radarr that manages and downloads subtitles based on per-show or per-movie preferences.
- [Sonarr](https://github.com/Sonarr/Sonarr) — PVR for Usenet and BitTorrent that monitors RSS feeds for new episodes and grabs, sorts, and renames them.
- [Homarr](https://github.com/ajnart/homarr) — Customizable home page to interact with a home server's Docker containers such as Sonarr and Radarr.
- [Midarr](https://github.com/midarrlabs/midarr-server) — Open-source media server that integrates with Radarr and Sonarr.
- [Rustdesk](https://rustdesk.com/) — Open-source remote desktop software for Windows, macOS, Linux, and Android.
- [TinyPilot](https://tinypilotkvm.com/) — Tool that enables KVM over IP to control any computer remotely.
- [PM2](https://github.com/Unitech/pm2) — Production process manager for Node.js applications with a built-in load balancer.
- [authentik](https://github.com/goauthentik/authentik) — Open-source identity provider for adding authentication, signup, and recovery to applications.
- [ESPHome Remote](https://github.com/landonr/esphome-remote) — Wi-Fi smart home remote with display running on ESPHome, using Lilygo T-Display or M5Stack Fire.
- [Tdarr](https://tdarr.io/) — Distributed transcode automation application using FFmpeg/HandBrake with library analytics and video health checking.
- [AppFlowy](https://www.appflowy.io/) — Open-source alternative to Notion where you control your data and customizations.
- [deemix](https://deemix.app/) — Deezer downloader library built from Deezloader Remix.
- [Neko](https://github.com/m1k1o/neko/) — Self-hosted virtual browser that runs in Docker and uses WebRTC.
- [QNAP Switch System (QSS)](https://www.qnap.com/) — Configuration interface for QNAP's managed switch series, enabling link aggregation, VLAN, and RSTP.
- [ASUSTOR](https://www.asustor.com/) — Provider of network attached storage (NAS) for home and enterprise users.
- [Seafile](https://www.seafile.com/) — Open-source, cross-platform file-hosting system that organizes files into libraries synced to desktop and mobile devices.
- [SnapRAID](http://www.snapraid.it/) — Folder-based backup tool that behaves like RAID5/6 without being a disk raid, using manual backup execution.
- [FreeNAS](https://www.truenas.com/freenas/) — Open-source storage platform supporting ZFS and sharing across Windows, Apple, and UNIX-like systems.
- [Gladys Assistant](https://github.com/gladysassistant/gladys) — Privacy-first, open-source home assistant that runs on Raspberry Pi.
- [Audiobookshelf](https://github.com/advplyr/audiobookshelf) — Self-hosted audiobook and podcast server.
- [Mistborn](https://gitlab.com/cyber5k/mistborn) — Platform for standing up and managing self-hosted cloud services, including firewall, ad-blocking, and multi-factor WireGuard VPN.

## Media Server

Software for organizing and streaming your own movies, TV, music, and other media to your devices.

- [Overseerr](https://overseerr.dev/) — Open-source application for managing media library requests, integrating with Sonarr, Radarr, and Plex.
- [Jellyfin](https://jellyfin.org/) — Free media system for managing and streaming media; an alternative to Emby and Plex.
- [Swiftfin](https://github.com/jellyfin/Swiftfin) — Video client for the Jellyfin media server, written in Swift for Apple devices.
- [Intro Skipper](https://github.com/ConfusedPolarBear/intro-skipper) — Tool that analyzes episode audio to detect and skip intro sequences in Jellyfin.
- [Jellyseerr](https://github.com/Fallenbagel/jellyseerr) — Media request management application; a fork of Overseerr with support for Jellyfin and Emby.
- [Midarr](https://github.com/midarrlabs/midarr-server) — Open-source media server that integrates with Radarr and Sonarr.
- [Kirino Media Server](https://kirino.io/) — Lightweight, modular alternative to Plex and Jellyfin.
- [Emby](https://emby.media/) — Home media server with a REST-based API for client development.
- [OpenMediaVault](https://www.openmediavault.org/) — NAS solution based on Debian Linux with services like SSH, FTP, SMB/CIFS, UPnP media server, RSync, and BitTorrent.
- [MediaElch](https://github.com/Komet/MediaElch) — Media manager for Kodi that stores metadata for movies, TV shows, concerts, and music as NFO files.
- [tinyMediaManager](https://www.tinymediamanager.org/) — Media management tool written in Java/Swing that provides metadata for Kodi, MediaPortal, and Plex.
- [FileBot](https://www.filebot.net/) — Tool for renaming and organizing movies, TV shows, and anime, with metadata, artwork, and subtitle fetching.
- [Plex media server](https://www.plex.tv/) — Application to add, access, and share media across devices, with on-demand titles, live TV, and personal media.
- [Tautulli](https://tautulli.com/) — Application that runs alongside Plex to monitor activity and track statistics.
- [Plex DupeFinder](https://github.com/l3uddz/plex_dupefinder) — Python script that finds duplicate media in a Plex library and removes lower-rated versions based on user scoring.
- [Prometheus Exporter for Plex](https://github.com/jsclayton/prometheus-plex-exporter) — Exposes library playback, storage, and host metrics in Prometheus format.
- [Infuse](https://firecore.com/) — Video player for iOS, Apple TV, and Mac that plays many video file formats without transcoding.
- [InfuseSync](https://github.com/firecore/InfuseSync) — Plugin for Emby and Jellyfin that tracks media changes to decrease sync times with Infuse clients.
- [InvidTUI](https://darkhz.github.io/invidtui/) — Invidious client that fetches data from Invidious instances and plays YouTube audio and video in a terminal interface.
- [Polaris](https://github.com/agersant/polaris) — Music streaming application that streams your collection directly from your computer or server without third-party uploads.
- [AirSonic](https://hub.docker.com/r/airsonic/airsonic) — Web-based media streamer for accessing your music.
- [TubeSync](https://github.com/meeb/tubesync) — PVR for YouTube that synchronizes channels and playlists to local directories and updates your media server.
- [yt-fts](https://github.com/NotJoeMartinez/yt-fts) — Python script that scrapes a YouTube channel's subtitles into a searchable SQLite database and generates timestamped video URLs.
- [Tube Archivist](https://github.com/tubearchivist/tubearchivist) — Self-hosted YouTube media server.
- [PeerTube](https://joinpeertube.org/) — ActivityPub-federated video streaming platform using P2P in the web browser.
- [Ant Media Server](https://github.com/ant-media/Ant-Media-Server) — Streaming engine providing low-latency streaming using WebRTC.
- [Castopod](https://code.castopod.org/adaures/castopod) — Open-source podcast hosting platform for podcasters to engage with their audience.
- [Festival](https://festival.pm/) — Music player for local album collections.
- [HD HomeRun Scribe 4K](https://www.silicondust.com/product/hdhomerun-scribe-4k/) — Local live TV box with DVR, 4 tuners, and recording storage.
- [RuneAudio](https://www.runeaudio.com/) — Open-source software that turns embedded hardware into Hi-Fi music players.
- [Volumio](https://volumio.com/) — Music aggregator and player for various hardware setups.
- [Snapcast](https://github.com/badaix/snapcast) — Multiroom client-server audio player that time-synchronizes clients for synced playback.
- [SonoBus](https://sonobus.net) — Application for streaming high-quality, low-latency peer-to-peer audio between devices over a network.
- [MythTV](https://www.mythtv.org/) — Open-source digital video recorder (DVR) project under the GNU GPL.

## Smart Home Automation

Smart home automation lets you control appliances, lights, thermostats, and other devices remotely, often over a dedicated network segment. Most smart devices sit on their own VLAN with limited internet access; software like Home Assistant, Homebridge, and ESPHome simplifies controlling and automating them.

- [Matter](https://buildwithmatter.com/) — Open standard letting a device work with any Matter-certified smart home ecosystem using a single protocol.
- [Amazon Alexa](https://alexa.amazon.com/) — Virtual assistant software to manage Alexa-enabled devices, music, lists, reminders, and timers.
- [Google Assistant](https://assistant.google.com/) — Virtual assistant software for mobile and home automation devices.
- [Apple HomeKit](https://www.apple.com/shop/accessories/all/homekit) — Framework to discover and control home automation accessories from multiple vendors through a unified interface.
- [Samsung SmartThings](https://www.smartthings.com/) — Framework to connect, monitor, and control smart home devices from one app.
- [Philips Hue](https://www.philips-hue.com) — Smart lighting system with smart lights, the Hue Bridge, and smart controls.
- [Sonos](https://www.sonos.com) — Wireless home sound system for multi-room audio.
- [Home Assistant](https://www.home-assistant.io/) — Open-source home automation platform focused on local control and privacy; runs on Raspberry Pi. Add-ons run alongside it on the Home Assistant OS and Supervised installations.
- [DuckDNS](https://github.com/home-assistant/hassio-addons/blob/master/duckdns/DOCS.md) — Home Assistant add-on that updates your Duck DNS IP address and generates SSL via Let's Encrypt.
- [Almond](https://github.com/home-assistant/hassio-addons/blob/master/almond/DOCS.md) — Open, privacy-preserving virtual assistant add-on.
- [HomeMatic](https://github.com/home-assistant/hassio-addons/blob/master/homematic/DOCS.md) — HomeMatic central based on OCCU.
- [Let's Encrypt](https://github.com/home-assistant/hassio-addons/blob/master/letsencrypt/DOCS.md) — Add-on to get a free SSL certificate from Let's Encrypt.
- [MariaDB](https://github.com/home-assistant/hassio-addons/blob/master/mariadb/DOCS.md) — Open-source relational database add-on (fork of MySQL).
- [File editor](https://github.com/home-assistant/hassio-addons/blob/master/configurator/DOCS.md) — Browser-based configuration file editor add-on.
- [Mosquitto](https://github.com/home-assistant/hassio-addons/blob/master/mosquitto/DOCS.md) — MQTT broker add-on.
- [Terminal & SSH](https://github.com/home-assistant/hassio-addons/blob/master/ssh/DOCS.md) — Add-on for remote login via web terminal or SSH client.
- [Samba](https://github.com/home-assistant/hassio-addons/blob/master/samba/DOCS.md) — Add-on to access configuration files using Windows network shares.
- [NGINX SSL proxy](https://github.com/home-assistant/hassio-addons/blob/master/nginx_proxy/DOCS.md) — Reverse proxy add-on with SSL termination.
- [deCONZ](https://github.com/home-assistant/hassio-addons/blob/master/deconz/DOCS.md) — Add-on to control a ZigBee network using ConBee or RaspBee hardware.
- [TellStick](https://github.com/home-assistant/hassio-addons/blob/master/tellstick/DOCS.md) — Add-on to run a TellStick and TellStick Duo service.
- [Ada](https://github.com/home-assistant/hassio-addons/blob/master/ada/DOCS.md) — Voice assistant add-on powered by Almond.
- [Fully Kiosk Browser](https://www.home-assistant.io/integrations/fully_kiosk/) — Integration to control and monitor an Android kiosk browser device from Home Assistant.
- [Dasshio](https://github.com/danimtb/dasshio) — Add-on to use Amazon Dash Buttons.
- [InfluxDB](https://github.com/hassio-addons/addon-influxdb) — Datastore add-on for metrics, events, and real-time analytics.
- [Grafana](https://github.com/hassio-addons/addon-grafana) — Add-on for analytics and monitoring dashboards.
- [Tor](https://github.com/hassio-addons/addon-tor) — Add-on to access your instance via Tor.
- [Spotify Connect](https://github.com/hassio-addons/addon-spotify-connect) — Spotify Connect client add-on for playing music on a Home Assistant device.
- [SSH & Web Terminal](https://github.com/hassio-addons/addon-ssh) — SSH and web-based terminal add-on with preloaded tools.
- [UniFi Controller](https://github.com/hassio-addons/addon-unifi) — Add-on to manage a UniFi network from a web browser.
- [Node-RED](https://github.com/hassio-addons/addon-node-red) — Flow-based programming add-on for the Internet of Things.
- [Plex Media Server](https://github.com/hassio-addons/addon-plex) — Plex media server add-on.
- [IDE](https://github.com/hassio-addons/addon-ide) — Web-based IDE add-on based on Cloud9 IDE.
- [zigbee2mqtt](https://github.com/danielwelch/hassio-zigbee2mqtt) — Zigbee to MQTT bridge add-on.
- [Matrix](https://github.com/hassio-addons/addon-matrix) — Decentralized communication platform add-on.
- [AdGuard Home](https://github.com/hassio-addons/addon-adguard-home) — Network-wide ad and tracker blocking DNS server add-on with parental control.
- [Traccar](https://github.com/hassio-addons/addon-traccar) — GPS tracking platform add-on.
- [Home Panel](https://github.com/hassio-addons/addon-home-panel) — Touch-compatible web frontend add-on for controlling the home.
- [Hass.io Google Drive Backup](https://github.com/sabeechen/hassio-google-drive-backup) — Add-on for backing up snapshots to Google Drive.
- [Grocy](https://github.com/hassio-addons/addon-grocy) — Groceries and household management add-on.
- [EmonCMS](https://github.com/inverse/hassio-addon-emoncms) — Web app add-on for processing, logging, and visualizing energy and environmental data.
- [CrowdSec](https://github.com/crowdsecurity/home-assistant-addons) — Collaborative IPS/IDS add-on to protect against intrusion.
- [AppDaemon](https://github.com/hassio-addons/addon-appdaemon) — Python apps and HADashboard add-on.
- [TasmoAdmin](https://github.com/hassio-addons/addon-tasmoadmin) — Add-on to centrally manage Sonoff-Tasmota devices.
- [Aircast](https://github.com/hassio-addons/addon-aircast) — AirPlay capabilities add-on for Chromecast players.
- [AirSonos](https://github.com/hassio-addons/addon-airsonos) — AirPlay capabilities add-on for Sonos players.
- [Log Viewer](https://github.com/hassio-addons/addon-log-viewer) — Browser-based live log viewing add-on.
- [Tautulli](https://github.com/hassio-addons/addon-tautulli) — Add-on to monitor and get statistics from a Plex server.
- [motionEye](https://github.com/hassio-addons/addon-motioneye) — CCTV/NVR add-on for cameras.
- [JupyterLab](https://github.com/hassio-addons/addon-jupyterlab) — Add-on to create documents containing live code, equations, visualizations, and text.
- [Glances](https://github.com/hassio-addons/addon-glances) — Cross-platform system monitoring add-on written in Python.
- [Simple Thermostat](https://github.com/nervetattoo/simple-thermostat) — Flexible thermostat Lovelace card.
- [Card Modder](https://github.com/thomasloven/lovelace-card-mod) — Card to style Lovelace cards.
- [Bar Card](https://github.com/Gluwc/bar-card) — Customizable animated bar card.
- [forked-daapd Card](https://github.com/kalkih/forked-daapd-card) — Card to control a forked-daapd instance.
- [Dual Gauge Card](https://github.com/Rocka84/dual-gauge-card) — Card that shows two gauges in one.
- [Atomic Calendar Revive](https://github.com/totaldebug/atomic-calendar-revive) — Calendar card with advanced settings.
- [Simple Weather Card](https://github.com/kalkih/simple-weather-card) — Minimalistic weather card.
- [Auto-Entities Card](https://github.com/thomasloven/lovelace-auto-entities) — Card that dynamically adds entities.
- [Canvas Gauge Card](https://github.com/custom-cards/canvas-gauge-card) — Card using gauges from canvas-gauges.com.
- [Big Number Card](https://github.com/custom-cards/bignumber-card) — Card to display big numbers for sensors, including severity level as background.
- [Animated Weather Card](https://github.com/bramkragten/weather-card) — Weather card with subtle animations.
- [Thermostat Card](https://github.com/ciotlosm/lovelace-thermostat-dark-card) — Thermostat control card styled like a Nest Thermostat.
- [Raspberry Pi Status Card](https://github.com/ironsheep/lovelace-rpi-monitor-card) — Card to show the status of Raspberry Pis.
- [Mini Media Player](https://github.com/kalkih/mini-media-player) — Minimalistic media player card.
- [Mini Graph Card](https://github.com/kalkih/mini-graph-card) — Minimalistic sensor graph card.
- [Button card](https://github.com/kuuji/button-card) — Button card for entities.
- [Slider Entity Row](https://github.com/thomasloven/lovelace-slider-entity-row) — Card that adds a slider to adjust values such as light brightness.
- [Power Wheel Card](https://github.com/gurbyz/power-wheel-card) — Card to represent the power your home consumes or produces.
- [Home Card](https://github.com/postlund/home-card) — Card for a quick glance at the state of your home.
- [Banner Card](https://github.com/nervetattoo/banner-card) — Linkable banner card with interactive glances for dashboards.
- [Spotify Card](https://github.com/custom-cards/spotify-card) — Card to list devices and top playlists on Spotify.
- [Battery Entity](https://github.com/cbulock/lovelace-battery-entity) — Card to display battery levels for battery entities.
- [Multiple Entity Row](https://github.com/benct/lovelace-multiple-entity-row) — Card to show multiple entity states or attributes on entity rows.
- [Home Feed Card](https://github.com/gadgetchnnel/lovelace-home-feed-card) — Card to display notifications, calendar events, and entities as a feed.
- [Config Template Card](https://github.com/custom-cards/config-template-card) — Card that allows using templates in Lovelace.
- [RGB Light Card](https://github.com/bokub/rgb-light-card) — Card with buttons to control RGB lights.
- [Restriction Card](https://github.com/iantrich/restriction-card) — Card to provide restrictions on the Lovelace cards defined within.
- [Vacuum Map Card](https://github.com/PiotrMachowski/Home-Assistant-Lovelace-Xiaomi-Vacuum-Map-card) — Card to control Xiaomi and Neato vacuums.
- [Vacuum Card](https://github.com/denysdovhan/vacuum-card) — Card for controlling a vacuum cleaner robot.
- [Purifier Card](https://github.com/denysdovhan/purifier-card) — Card for controlling air purifiers.
- [Lutron Caseta Pro](https://github.com/upsert/lutron-caseta-pro) — Integration for the Lutron Caseta Smart Bridge PRO / RA2 Select.
- [SmartIR](https://github.com/smartHomeHub/SmartIR) — Integration for devices using Broadlink IR.
- [Alexa Media Player](https://github.com/keatontaylor/alexa_media_player) — Integration to control Amazon Alexa devices.
- [Circadian Lighting](https://github.com/claytonjn/hass-circadian_lighting) — Integration that synchronizes color-changing lights with the natural color temperature of the sky.
- [Volkswagen Carnet](https://github.com/robinostlund/homeassistant-volkswagencarnet) — Integration for Volkswagen Carnet (requires a valid Carnet subscription).
- [Untappd](https://github.com/custom-components/sensor.untapped) — Integration that connects with an Untappd account.
- [Elasticsearch](https://github.com/legrego/homeassistant-elasticsearch) — Integration that publishes events to Elasticsearch.
- [HASS Aarlo](https://github.com/twrecked/hass-aarlo) — Asynchronous Arlo integration that monitors events and states for base stations, cameras, and doorbells.
- [Xiaomi Cloud Map Extractor](https://github.com/PiotrMachowski/Home-Assistant-custom-components-Xiaomi-Cloud-Map-Extractor) — Integration presenting a live map view for Xiaomi vacuums without rooting.
- [Xiaomi Hygrothermo](https://github.com/dolezsa/Xiaomi_Hygrothermo) — Sensor platform for the Xiaomi Mijia BT temperature and humidity sensor.
- [WebRTC Camera](https://github.com/AlexxIT/WebRTC) — Integration to view RTSP streams from IP cameras through WebRTC or MSE with pan/zoom controls.
- [Sonoff LAN](https://github.com/AlexxIT/SonoffLAN) — Integration to control Sonoff devices with eWeLink firmware over LAN or cloud.
- [Spotcast](https://github.com/fondberg/spotcast) — Integration to start Spotify playback on an idle Chromecast and control Spotify Connect devices.
- [The Watchman](https://github.com/dummylabs/thewatchman) — Integration to track missing entities and services in config files.
- [Homebridge](https://homebridge.io/) — Framework that integrates smart home devices lacking native HomeKit support, with over 2,000 plugins.
- [Homebridge UI](https://github.com/oznu/homebridge-config-ui-x) — Interface to manage Homebridge plugins, configuration, and accessories.
- [Homebridge Raspberry Pi Image](https://github.com/homebridge/homebridge-raspbian-image) — Raspbian-based Raspberry Pi image with Homebridge and Homebridge Config UI X preinstalled.
- [Homebridge Config UI X](https://github.com/oznu/homebridge-config-ui-x) — Web-based management tool for all aspects of a Homebridge setup.
- [Homebridge webOS TV](https://github.com/merdok/homebridge-webos-tv) — Plugin to control an LG webOS TV from the Home app.
- [Homebridge Unifi Protect](https://github.com/hjdhjd/homebridge-unifi-protect) — Plugin that provides HomeKit support to the UniFi Protect device ecosystem.
- [Homebridge Camera FFmpeg](https://github.com/Sunoo/homebridge-camera-ffmpeg) — Homebridge plugin providing FFmpeg-based camera support.
- [Homebridge Mi Aqara](https://github.com/YinHangCode/homebridge-mi-aqara) — Homebridge plugin for XiaoMi Aqara.
- [Homebridge Camera UI](https://github.com/seydx/homebridge-camera-ui) — Tool to expose cameras from camera.ui to HomeKit via Homebridge.
- [HOOBS](https://hoobs.org/) — Tool that makes smart accessories compatible with Apple HomeKit, Google Home, or Amazon Alexa.
- [ESPHome](https://esphome.io/) — System to control ESP8266/ESP32 devices via configuration files and integrate them with home automation systems.
- [Shelly Cloud](https://shelly.cloud/) — Smart home control and monitoring for Shelly devices, compatible with Alexa, Google Home, Android, and iOS.
- [Homey](https://homey.app/) — Application to control, automate, and monitor a smart home from phone, tablet, or desktop.
- [Ecobee](https://www.ecobee.com) — Company that makes thermostats for residential and commercial use.
- [Lutron Caséta](https://www.lutron.com/en-US/Products/Pages/SingleRoomControls/CasetaWireless/Overview.aspx) — Smart lighting control system that works with older and newer home wiring.
- [Insteon switches](https://www.insteon.com/) — Hub and devices for controlling and configuring a home, bridging to Amazon Alexa and Google Assistant.
- [Jeedom](https://www.jeedom.com/) — Open-source home automation software compatible with protocols including ZigBee, Z-Wave, EnOcean, KNX, LoRaWAN, BACnet, and Modbus.
- [Beestat](https://github.com/beestat/app) — Tool that connects with a thermostat and provides charts and analytics on energy use.
- [MQTT](https://mqtt.org/) — Lightweight publish/subscribe messaging protocol for the Internet of Things.
- [pfSense](https://www.pfsense.org/) — Firewall/router software distribution based on FreeBSD.
- [Pi-hole](https://pi-hole.net/) — DNS sinkhole that blocks unwanted content network-wide without client-side software.
- [AdGuard Home](https://github.com/AdguardTeam/AdGuardHome) — DNS relay with ad/tracker blocking, IP redirections, and DNS-over-HTTPS.
- [OpenWRT](https://openwrt.org/) — Open-source embedded Linux operating system used on devices to route network traffic.
- [ZoneMinder](https://zoneminder.com/) — Open-source video surveillance software system.
- [Plex media server](https://www.plex.tv/) — Application to add, access, and share media across devices, with on-demand titles, live TV, and personal media.

## Voice Assistants

Software for building local, privacy-focused voice control, including speech-to-text, wake-word detection, and assistant frameworks.

- [$13 voice assistant remote for Home Assistant](https://www.home-assistant.io/voice_control/thirteen-usd-voice-remote/) — Guide to a low-cost voice assistant remote for Home Assistant.
- [Wyoming](https://github.com/rhasspy/wyoming) — Peer-to-peer protocol for voice assistants used in Rhasspy and Home Assistant.
- [Wyoming Faster Whisper](https://github.com/rhasspy/wyoming-faster-whisper) — Wyoming protocol server for the faster-whisper speech-to-text system.
- [Wyoming Porcupine1](https://github.com/rhasspy/wyoming-porcupine1) — Wyoming protocol server for the porcupine1 wake word detection system.
- [Wyoming Snowboy](https://github.com/rhasspy/wyoming-snowboy) — Wyoming protocol server for the snowboy wake word detection system.
- [faster-whisper](https://github.com/guillaumekln/faster-whisper/) — Reimplementation of the Whisper model using CTranslate2 for fast inference.
- [Porcupine](https://github.com/Picovoice/porcupine) — Lightweight wake word engine for building always-listening voice applications.
- [Rhasspy](https://github.com/rhasspy/rhasspy3/) — Open-source voice assistant toolkit for many human languages.
- [openWakeWord](https://github.com/dscripka/openWakeWord) — Open-source wakeword library with pre-trained models for common words and phrases.
- [Conversation](https://www.home-assistant.io/integrations/conversation) — Integration that lets you converse with Home Assistant by voice or transcribed text.
- [Piper](https://github.com/rhasspy/piper/) — Fast, local neural text-to-speech system optimized for the Raspberry Pi 4.
- [Mycroft](https://mycroft.ai/) — Open-source voice assistant that is private by default and customizable.
- [DeepSpeech](https://github.com/mozilla/DeepSpeech) — Open-source offline speech-to-text engine that runs from a Raspberry Pi 4 to GPU servers.
- [Leon](https://github.com/leon-ai/leon) — Open-source personal assistant.
- [Olivia](https://olivia-ai.org/) — Open-source chatbot built in Go using machine learning, as an alternative to DialogFlow.
- [Alan SDK](https://github.com/alan-ai/alan-sdk-web) — Voice assistant SDK to build a voice interface for websites and web apps.
- [OpenAssistant](https://open-assistant.io/) — Chat-based assistant that understands tasks, interacts with third-party systems, and retrieves information.

## Video Surveillance

Software for recording and analyzing camera feeds locally, including network video recorders (NVRs) and AI object detection.

- [Frigate](https://frigate.video/) — Open-source NVR built around real-time AI object detection with local processing.
- [hkcam](https://hochgatterer.me/hkcam/) — Open-source HomeKit IP camera implementation that uses ffmpeg to publish a camera stream to HomeKit.
- [OpenDataCam](https://opendata.cam/) — Open-source tool that quantifies and tracks moving objects with live video analysis, saving only meta-data.
- [Viseron](https://github.com/roflcoopter/viseron) — Self-hosted, local-only NVR and AI computer vision software.
- [zmninja](http://zmninja.zoneminder.com/) — Cross-platform app for home or commercial security surveillance using ZoneMinder.
- [Moonfire NVR](https://github.com/scottlamb/moonfire-nvr) — Security camera network video recorder.
- [Shinobi Pro](https://gitlab.com/Shinobi-Systems/Shinobi) — Open-source video management software with support for over 6000 IP and USB cameras.
- [WyzeHacks](https://github.com/HclX/WyzeHacks) — Set of scripts that add features to Wyze cameras such as telnet, NFS recording redirection, and scheduled reboots.

## Text-to-Speech (TTS)

Tools for speech recognition (speech-to-text) and speech synthesis (text-to-speech) that run locally.

- [whisper.cpp](https://github.com/ggerganov/whisper.cpp) — Inference of the Whisper automatic speech recognition (ASR) model.
- [WaaS](https://github.com/schibsted/WAAS) — Whisper as a Service, providing a GUI and API for Whisper.
- [Web Whisper](https://codeberg.org/pluja/web-whisper) — Whisper running in your web browser.
- [Vosk](https://github.com/alphacep/vosk-api) — Offline open-source speech recognition toolkit supporting 20+ languages and dialects.
- [Coqui TTS](http://coqui.ai/) — Deep learning toolkit for text-to-speech.
- [Mozilla TTS](https://github.com/mozilla/TTS) — Library for text-to-speech generation balancing training ease, speed, and quality.
- [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) — Conversational AI toolkit for ASR, TTS, large language models, and natural language processing.

## Video & Audio Processing

Tools and standards for decoding, encoding, transcoding, and streaming video and audio.

- [Intel® Quick Sync Video](https://www.intel.com/content/www/us/en/architecture-and-technology/quick-sync-video/quick-sync-video-general.html) — Uses Intel Graphics Technology to decode and encode media quickly.
- [Intel® QuickAssist Technology (Intel® QAT)](https://www.intel.com/content/www/us/en/architecture-and-technology/intel-quick-assist-technology-overview.html) — Technology to accelerate data encryption/decryption and compression across applications.
- [FFmpeg](https://ffmpeg.org) — Multimedia framework that can decode, encode, transcode, mux, demux, stream, filter, and play media on Windows, macOS, and Linux.
- [FFmpeg.guide](https://ffmpeg.guide/) — GUI tool to create FFmpeg filtergraphs without writing filter syntax.
- [HandBrake](https://handbrake.fr/) — Tool for transcoding video from many formats using widely supported codecs on Windows, macOS, and Linux.
- [Tdarr](https://github.com/HaveAGitGat/Tdarr) — Cross-platform conditional transcoding application for automating media library transcode/remux management.
- [SRS](https://github.com/ossrs/srs) — Realtime video server supporting RTMP, WebRTC, HLS, HTTP-FLV, SRT, and GB28181.
- [obsws-python](https://github.com/aatikturk/obsws-python) — Python SDK for OBS Studio WebSocket v5.0.
- [AAC (Advanced Audio Coding)](https://mpeg.chiariglione.org/) — Audio coding standard for lossy digital audio compression, endorsed by ISO and IEC.
- [H.264 (AVC)](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC) — Video compression standard with multiple profiles and levels supporting up to 8K.
- [H.265 (HEVC)](https://en.wikipedia.org/wiki/High_Efficiency_Video_Coding) — Successor to H.264 offering 25% to 50% better compression at the same quality.
- [HTTP Live Streaming (HLS)](https://developer.apple.com/streaming/) — Apple communications protocol that sends live and on-demand audio and video to Apple devices and PC.
- [Dynamic Adaptive Streaming over HTTP (DASH)](https://developer.mozilla.org/en-US/docs/Web/HTML/DASH_Adaptive_Streaming_for_HTML_5_Video) — Adaptive streaming protocol that switches bit rates based on network performance.
- [OpenMAX™](https://www.khronos.org/openmax/) — Cross-platform API for streaming media codec and application portability across operating systems and platforms.
- [GStreamer](https://gstreamer.freedesktop.org/) — Library for constructing graphs of media-handling components for playback, streaming, and editing.
- [Media Source Extensions (MSE)](https://www.w3.org/TR/media-source/) — W3C specification allowing JavaScript to send byte streams to media codecs in browsers.
- [WebRTC](https://webrtc.org/) — Open-source project adding real-time video, voice, and data communication to applications.

## Podcasting

Software for hosting, distributing, downloading, and playing podcasts.

- [Castopod](https://code.castopod.org/adaures/castopod) — Open-source podcast hosting platform for podcasters to engage with their audience.
- [Sovereign Feeds](https://sovereignfeeds.com/) — Tool to search for podcasts and add them to favorites.
- [IPFS Podcasting](https://ipfspodcasting.net/) — Decentralized podcast distribution over IPFS with storage and bandwidth from volunteer nodes.
- [Audiobookshelf](https://www.audiobookshelf.org/) — Self-hosted audiobook and podcast server.
- [Vod2Pod-RSS](https://github.com/madiele/vod2pod-rss) — Tool that converts a YouTube or Twitch channel into a podcast RSS, transcoding VODs to MP3 on the fly.
- [Podverse](https://podverse.fm/) — Open-source podcast app for iOS, Android, F-Droid, and Web.
- [Alby](https://getalby.com/) — Bitcoin Lightning app for your browser.
- [Alby wallet API](https://blog.getalby.com/introducing-the-alby-wallet-api/) — OAuth-based API that grants client applications delegated access to an Alby wallet.
- [Blubrry](https://blubrry.com/) — Podcast hosting and publishing service with support, migration, and statistics.
- [SATurn](https://saturn.fly.dev/) — Tool to connect a getalby.com account and see which content resonates with your audience.
- [AntennaPod](https://antennapod.org/) — Open-source podcast player that supports any RSS feed and respects privacy.
- [Podgrab](https://github.com/akhilrex/podgrab) — Self-hosted podcast manager, downloader, and archiver with an integrated player.
- [Podify](https://github.com/podify-org/podify) — Self-hosted service to download videos and audio supported by youtube-dl and serve them as subscribable feeds.
- [dir2cast](https://github.com/ben-xo/dir2cast/) — Tool that turns a directory of MP3s into a podcast automatically.
- [Snipd](https://www.snipd.com/) — AI-powered podcast player to search transcripts, get summaries, and share clips.
- [Wave Share](https://ggerganov.github.io/wave-share) — Serverless, peer-to-peer, local file sharing through sound.
- [KBD Audio](https://github.com/ggerganov/kbd-audio) — Collection of command-line and GUI tools for capturing and analyzing audio data.

## Audiobooks

Software for serving and managing audiobook libraries.

- [Audioserve](https://github.com/izderadicka/audioserve) — Personal server to serve audio files from directories, intended primarily for audiobooks.
- [Audiobookshelf](https://www.audiobookshelf.org/) — Self-hosted audiobook and podcast server.
- [Jellyfin Bookshelf Plugin](https://github.com/jellyfin/jellyfin-plugin-bookshelf) — Bookshelf plugin for Jellyfin.

## Health

Self-hosted software for medical records, health data aggregation, and personal tracking.

- [Connect](https://github.com/nextgenhealthcare/connect) — Healthcare integration engine.
- [Fasten](https://github.com/fastenhealth/fasten-onprem) — Open-source, self-hosted personal and family electronic medical record aggregator that integrates with many insurers, hospitals, and clinics.
- [ERPNext](https://erpnext.com/) — Free and open-source Enterprise Resource Planning (ERP) for managing businesses.
- [OpenEMR](https://open-emr.org/) — Open-source electronic health records and medical practice management application with scheduling and billing.
- [Ryot (Roll Your Own Tracker)](https://ryot.fly.dev/) — Self-hosted platform for tracking facets of your life such as media and fitness.

## Gardening

Software and DIY projects for irrigation control, plant tracking, and farm and garden management.

- [ESPHome: DIY Irrigation Controller With Internal Scheduler](https://community.home-assistant.io/t/esphome-diy-irrigation-controller-with-internal-scheduler/171844) — Community guide to building a DIY irrigation controller with ESPHome.
- [Smart WiFi Controlled Irrigation System Using Home Assistant and ESPHome](https://www.instructables.com/Smart-WiFi-Controlled-Irrigation-System-Using-Home/) — Guide to building a WiFi-controlled irrigation system with Home Assistant and ESPHome.
- [OpenSprinkler](https://opensprinkler.com/product/opensprinkler/) — Open-source, web-based smart sprinkler controller for lawn, plant, drip, and farm irrigation with built-in WiFi.
- [Droplet](https://github.com/PricelessToolkit/Droplet) — All-in-one irrigation and monitoring system for ESPHome and Home Assistant.
- [9 Valve Sprinkler Controller](https://github.com/hwstar/9-Valve-Sprinkler-Controller) — Nine-valve sprinkler controller for use with firmware such as ESPHome.
- [GardenBot](https://www.gardenbot.org/howTo/) — Open-source garden monitoring system with tutorials, software, and resources.
- [farmOS](https://farmos.org/) — Web-based application for farm management, planning, and record keeping.
- [OpenFarm](https://openfarm.cc/) — Open database and web application for farming and gardening knowledge.
- [Growstuff](http://growstuff.org/) — Open-source, open-data project for food gardeners that crowdsources and shares growing data via an API.
- [Harvest Helper](https://github.com/damwhit/harvest_helper) — Tool providing growing, harvesting, and recipe information with a JSON API.
- [HappyPlants](https://happyplants.garden/) — Mobile web application for collecting and organizing information about your plants.
- [Automated irrigation system](https://github.com/PatrickHallek/automated-irrigation-system) — Open-source application to water plants automatically with a scalable DIY setup.
- [Pigrow](https://github.com/Pragmatismo/Pigrow) — Garden automation suite to monitor, log, graph, and control a grow space using a Raspberry Pi, sensors, and relays.
- [Tania](https://usetania.org/) — Farm management software for hobbyist and smallholder farmers.

## Maps

Self-hosted and open-source mapping software, tile servers, and navigation tools, largely built on OpenStreetMap.

- [Magic Earth](https://www.magicearth.com/) — Turn-by-turn navigation with OpenStreetMap, crowd-sourced traffic, 3D and satellite maps, offline maps, and transit.
- [Organic Maps](https://organicmaps.app/) — Free offline maps app for Android and iOS using OpenStreetMap data, with no ads or tracking.
- [MapTiler Server](https://www.maptiler.com/server/self-host-satellite-maps/) — Self-hosted aerial and satellite imagery maps served from your own server.
- [GPSLogger](https://gpslogger.app/) — Android tool that logs GPS coordinates at intervals for geotagging photos or sharing routes.
- [KelperJs](http://keplerjs.io/) — Open-source full-stack geosocial network platform.
- [OpenStreetMap (OSM)](https://www.openstreetmap.org/) — Map of the world created by contributors and free to use under an open license.
- [uMap](https://github.com/umap-project/umap) — Tool to create maps with OpenStreetMap layers and embed them in your site.
- [Martin](https://martin.maplibre.org/) — Tile server written in Rust that generates vector tiles from PostGIS databases or serves PMTile and MBTile files.
- [MapLibre GL JS](https://github.com/maplibre/maplibre-gl-js) — Open-source library for publishing maps with GPU-accelerated vector tile rendering.
- [MapLibre Native](https://maplibre.org/) — Interactive vector tile maps for iOS, Android, and other platforms.
- [Maplibre-rs](https://github.com/maplibre/maplibre-rs) — Experimental maps for web, mobile, and desktop.

## Photos

Self-hosted photo and video management, galleries, backup, and editing tools.

- [PhotoPrism®](https://docs.photoprism.app/license/docs/) — AI-powered app for browsing, organizing, and sharing a photo collection at home, on a server, or in the cloud.
- [Immich](https://immich.app/) — Self-hosted photo and video backup solution from your mobile phone.
- [Piwigo](https://piwigo.org/) — Self-hosted, open-source photo gallery web application with templates, plugins, galleries, and viewing permissions.
- [Czkawka](https://github.com/qarmin/czkawka) — App to find duplicates, empty folders, and similar images.
- [Phockup](https://github.com/ivandokov/phockup) — Media sorting tool that organizes photos and videos into folders by year, month, and day.
- [PiGallery 2](https://github.com/bpatrik/pigallery2) — Directory-first photo gallery website optimized for low-resource servers such as the Raspberry Pi.
- [Photoview](https://photoview.github.io/) — Self-hosted photo gallery for photographers to navigate directories of high-resolution photos.
- [digiKam](https://www.digikam.org/) — Free and open-source professional photo management tool.
- [ShareX](https://getsharex.com/) — Open-source program to capture or record the screen and upload images, text, and files to many destinations.
- [PhotoSync](https://www.photosync-app.com/home.html) — Service to wirelessly transfer, back up, and share photos and videos to computers, NAS, phones, and cloud services.
- [Lychee](https://lycheeorg.github.io/) — Photo-management system you can run on your server to manage and share photos.
- [Gimme-iPhotos](https://github.com/Zebradil/Gimme-iPhotos) — Tool that uses pyicloud to synchronize photos and videos from iCloud to a local machine.
- [PyiCloud](https://github.com/picklepete/pyicloud) — Python module to interact with iCloud webservices, built on the requests HTTP library.
- [Pixelfed](https://pixelfed.org/) — Decentralized photo sharing using ActivityPub, interoperable with Mastodon and Pleroma.
- [Chevereto](https://hub.docker.com/r/linuxserver/chevereto) — Image hosting software to create an image hosting website on your own server.
- [Got Your Back (GYB)](https://github.com/GAM-team/got-your-back) — Command-line tool for backing up Gmail messages using the Gmail API over HTTPS.
- [Upscayl](https://upscayl.github.io/) — Open-source desktop application that upscales low-resolution images using AI models, with a Linux-first build.
- [Librephotos](https://github.com/LibrePhotos/librephotos) — Self-hosted open-source photo management service (backend repository).
- [Librephotos frontend](https://github.com/LibrePhotos/librephotos-frontend) — Frontend repository for the LibrePhotos photo management service.
- [Librephotos Mobile](https://github.com/LibrePhotos/librephotos-mobile) — Android and iOS mobile application for a self-hosted LibrePhotos server.
- [Librephotos Docker](https://github.com/LibrePhotos/librephotos-docker) — Dockerfiles for the automated build process of LibrePhotos.
- [OneFolder](https://github.com/OneFolderApp/OneFolder) — Desktop app to sort images locally like Google Photos, without running a server and compatible with NAS.

## Gaming

Software for game streaming, server management, game libraries, and console emulation.

- [Cartridge](https://github.com/unclebacon-live/cartridge) — Self-hosted game library made with Laravel and Vue.js that scans ROM files and matches them with IGDB information.
- [Moonlight Game Streaming](https://moonlight-stream.org/) — Program to stream PC games over the internet to almost any device.
- [Sunshine](https://github.com/LizardByte/Sunshine) — Self-hosted, low-latency game stream host for Moonlight with support for AMD, Intel, and NVIDIA GPUs.
- [Chiaki](https://git.sr.ht/~thestr4ng3r/chiaki) — Open-source client for PlayStation 4 and PlayStation 5 Remote Play across many platforms.
- [EmuDeck](https://www.emudeck.com/) — Tool that configures RetroArch, emulators, gamepads, and EmulationStation for retrogaming setups.
- [EmulationStation Desktop Edition (ES-DE)](https://www.es-de.org/) — Frontend for browsing and launching games from a multi-platform collection on Unix/Linux, macOS, and Windows.
- [RetroPie](https://retropie.org.uk/) — Frontend for emulators that turns a Raspberry Pi, ODroid, or PC into a retro-gaming machine.
- [RetroArch](https://www.retroarch.com/) — Frontend for emulators, game engines, and media players with unified configuration.
- [Pterodactyl](https://pterodactyl.io/) — Open-source game server management panel that runs game servers in isolated Docker containers.
- [LinuxGSM (Linux Game Server Managers)](https://linuxgsm.com/) — Command-line tool for deploying and managing Linux dedicated game servers.
- [Dolphin](https://dolphin-emu.org) — Emulator for the Nintendo GameCube and Wii with HD rendering and enhancements.
- [Citra](https://citra-emu.org/) — Open-source emulator for the Nintendo 3DS.
- [yuzu](https://yuzu-emu.org) — Experimental open-source emulator for the Nintendo Switch.
- [m64p](https://m64p.github.io/) — Nintendo 64 emulator using the mupen64plus-gui Qt5 frontend.
- [DeSmuME](https://desmume.org/) — Nintendo DS emulator.
- [Snes9x](https://www.snes9x.com/) — Portable, freeware Super Nintendo Entertainment System (SNES) emulator.
- [bsnes](https://github.com/bsnes-emu/bsnes) — SNES emulator focused on performance, features, and ease of use.
- [mGBA](https://mgba.io/) — Emulator for running Game Boy Advance games with a focus on speed and accuracy.
- [DOSBox](https://www.dosbox.com/) — Open-source DOS emulator focused on running DOS games.
- [DOSBox Staging](https://github.com/dosbox-staging/dosbox-staging) — x86 CPU emulator capable of running DOS programs requiring real or protected mode.
- [Flycast](https://github.com/flyinghead/flycast) — Multi-platform Sega Dreamcast, Naomi, and Atomiswave emulator derived from reicast.
- [PCSX2](https://pcsx2.net/) — PlayStation 2 emulator for playing PS2 games on a PC.
- [RPCS3](https://rpcs3.net/) — Experimental open-source Sony PlayStation 3 emulator and debugger written in C++.
- [MAME](https://www.mamedev.org/) — Arcade machine emulator.
- [xemu](https://xemu.app/) — Original Xbox emulator.
- [Xenia](https://github.com/xenia-project/xenia) — Xbox 360 emulator.
