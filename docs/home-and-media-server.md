# Home & Media Server

[← Handbook home](../README.md)

For many people, this is why they started: a server that holds the family photo
library, streams movies to the TV, and runs the smart-home automations — all
privately, without a monthly bill or a company mining the contents. This page
covers the three most popular home workloads and how to think about each.

## Media servers

A **media server** organizes your movies, shows, and music, fetches artwork and
metadata, and streams to phones, TVs, and browsers — your own private streaming
service over files you own. The mainstream choices:

- **Jellyfin** — fully free and open source, with no paid tier and no account
  requirement. The default recommendation when you want everything unlocked and
  nothing phoning home.
- **Plex** — polished and easy, with the widest device support, but it is a
  commercial product that gates some features behind a subscription and involves
  a cloud account.
- **Emby** — sits between the two, with a free core and paid extras.

All three follow the same pattern: point the server at folders of media named in
a consistent scheme, and it builds a browsable, streamable library. The heaviest
cost is **transcoding** — converting video on the fly when a device cannot play
the original format. Transcoding is CPU-intensive, so if you stream to varied
devices, hardware that supports GPU-accelerated transcoding (such as Intel Quick
Sync) matters more than raw core count.

Around the media server sits an ecosystem that automates acquiring and
organizing content; whether you use it, and for what, is your call to make
within the law where you live. Those tools are listed in the catalog.

## Photos

Self-hosted photo management replaces cloud photo services while keeping your
library — often the most irreplaceable data you own — on your own disks.

- **Immich** — the standout of recent years: a fast mobile app with automatic
  phone backup, face and object recognition, and a familiar timeline. It is the
  closest open-source experience to mainstream cloud photo apps.
- **PhotoPrism** — mature, with strong AI-powered tagging and search, oriented
  toward browsing and organizing a large collection.

Because photos are precious and singular, this is the workload where the
**[backup discipline](storage-and-backups.md)** is non-negotiable: a photo
library with no off-site copy is one disaster away from gone. Set up backups
before you delete the originals from your phone or the cloud.

## Home automation

**Home automation** connects lights, sensors, plugs, locks, and cameras so they
can be controlled and automated together. Self-hosting it keeps that control —
and the data about when you are home — on your own hardware instead of a vendor
cloud that can change terms or disappear.

- **Home Assistant** is the center of gravity here: an open-source platform that
  integrates thousands of devices across otherwise incompatible ecosystems,
  runs automations entirely locally, and keeps working even when your internet
  is down. It is the default recommendation, available as a dedicated OS image
  for a Raspberry Pi or small PC, or as a container.
- **ESPHome** lets you build and flash custom firmware for inexpensive
  ESP-based sensors and controllers that integrate directly with Home
  Assistant.
- **Zigbee2MQTT** and similar bridges let you use Zigbee/Z-Wave devices locally,
  free of any manufacturer's cloud or hub.

The principle that makes home automation worth self-hosting is **local
control**: automations that run on your own hardware respond instantly and keep
working during an internet outage — which is exactly when you do not want your
lights and locks to stop responding.

## Putting it together

These workloads share a host comfortably. A common shape:

1. A small-to-midrange machine (or NAS) with enough storage for media and
   photos — see **[Hardware & Operating Systems](hardware-and-os.md)**.
2. Services run as containers behind a reverse proxy (see
   **[Networking](networking.md)**).
3. Access from outside over a VPN, not by exposing the media server (see
   **[Remote Access](remote-access.md)**).
4. Photos and configuration backed up off-site; media backed up if
   re-acquiring it would be costly (see
   **[Storage & Backups](storage-and-backups.md)**).

Home Assistant is often given its own dedicated device, because you want home
control to stay up even while you are tinkering with everything else.

## Find software

Media servers, photo managers, home automation, voice assistants, video
surveillance, and related tools are in the
**[Media & Home catalog](catalog/media-and-home.md)**.
