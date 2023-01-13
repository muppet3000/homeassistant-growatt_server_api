# Growatt Server API (growatt_server_api)
This custom component (installable via HACS) is an upstream version of [growatt_server](https://www.home-assistant.io/integrations/growatt_server/) integration that is part of the [Home Assistant Core](https://github.com/home-assistant/core/tree/dev/homeassistant/components/growatt_server) repository.

The integration has been through a period of instability due to various issues with the authentication mechanism for Growatt (Growatt keep blocking the python library), using the HACS system will allow for more dynamic responses to the changes made by Growatt.

The changes made in this repository will be rolled up monthly and then submitted as a Pull-Request to the main Home Assistant Core repository for release as an 'official' Integration ([this one](https://www.home-assistant.io/integrations/growatt_server/)).

If anyone wants to say 'thanks' for the integration, feel free to click something below..... 

[![bmab_badge](https://img.shields.io/badge/Buy_Me-A_Beer-FFDD00.svg?style=for-the-badge&logo=buymeacoffee)](https://www.buymeacoffee.com/muppet3000)
[![paypal_badge](https://img.shields.io/badge/PayPal-Beer_Fund-blue.svg?style=for-the-badge&logo=paypal)](https://www.paypal.com/paypalme/muppet3000)

# Implementation
On initial release this plugin is an identical copy of the original integration that was part of the Home Assistant release. Going forward, this will be the upstream release of the Integration and the first place that bugs are fixed & new features are added.

This integration will continue to update the same sensors that are available in the Core integration with no interruption to service i.e. you don't have to go re-writing automations or re-mapping values

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
