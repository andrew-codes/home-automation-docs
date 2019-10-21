# My Home Automation Notes

## Goals

1. Require as few phone apps to control the home as possible (ideally just a single app)
2. Device control, automation rules, etc. are as centralized as possible; versus stringing multiple services together in tandem to accomplish an automation/control a device
3. Isolate services and their setup from another; favor containerization
4. Multi-room audio; primarily streaming from Spotify
5. Voice control with privacy (no Amazon, Google, or Apple services listening)

## All the Things / Device List

### Hub

- Intel NUC (running [hass.io](https://www.home-assistant.io/hassio/))

### Presence Detection

- iPhones

### AV Equipment

- Gaming-PC (Windows)
- PS4 Pro/PS4
- TV (LG)
- TV (Samsung)
- AVR (Denon)
- AppleTV
- Harmony hubs (used primarily for its IR emitter)
- ~~Nintendo Switch~~

### Networking

- [Ubiquiti cloud key](https://www.ui.com/unifi/unifi-cloud-key/) ([ASUS](https://www.home-assistant.io/integrations/asuswrt/) and [DD-WRT](https://www.home-assistant.io/integrations/ddwrt/) routers also supported)

### Other

- Lights
- Ceiling fans
- Locks
- Thermostats
- Roomba

## Setup Overview

1. [Install network](install-network.md)
2. [Setup the hub](setup-hub.md)
3. [Setup network](setup-network.md)
4. [Presence detection](presence-detection.md)
5. [Lights & ceiling fans](lights-and-ceiling-fans.md)
6. [Locks](locks.md)
7. Thermostat
8. AV / home theater
9. Multi-room audi
10. Voice Control
11. [Roomba](roomba.md)
