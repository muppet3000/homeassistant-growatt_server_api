:warning: **This repository is still in development, please continue to use the Home Assistant Core Integration for now** :warning:

# Growatt Server API (growatt_server_api)
This custom component (installable via HACS) replaces the original [growatt_server](https://www.home-assistant.io/integrations/growatt_server/) integration that is currently part of the Core Home Assistant repository.

The integration will be removed from the core repository due to various issues with the authentication mechanism for Growatt (Growatt keep blocking the python library), using the HACS system will allow for more dynamic responses to the changes made by Growatt.

If anyone wants to say 'thanks' for the integration, feel free to click..... [![bmab_badge](https://img.shields.io/badge/Buy_Me-A_Beer-FFDD00.svg?style=for-the-badge&logo=buymeacoffee)](https://www.buymeacoffee.com/muppet3000)

# Implementation
On initial release this plugin is an identical copy of the original integration that was part of the Home Assistant release. Going forward, this will be the only place that the Growatt integration for Home Assistant is updated. The original implementation will be removed from Home Assistant Core in due course. (This README will be updated when this happens).

# Features
This is a sensor to collect information from your Growatt inverters using [Growatt server](https://server.growatt.com/) by default. It is possible to specify an alternative endpoint server at configuration time e.g., [SMTEN](https://server.smten.com/).

This will log into your Growatt account and use the first “Plant”, after which it collects the inverters on this plant and creates sensors for these inverters as well as total sensors.

## Supported Systems
- TLX aka MIN/MIC/MOD/NEO
- Mix aka Hybrid
- Inverter
- Storage

## Not Yet Supported Systems
The implementation for these systems will follow soon
- MAX/MID/MAC
- AC Coupled aka SPA3000

# Roadmap & Prioritised Items
The roadmap for this integration can be found in the HA Forums [here](https://community.home-assistant.io/t/growatt-integration-roadmap/510221)

The current prioritised list of features to implement can be found in the HA Forums [here](https://community.home-assistant.io/t/growatt-integration-prioritised-list-of-features-for-implementation-fixing/483850)
