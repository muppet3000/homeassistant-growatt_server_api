:warning: **This repository is still in development, please continue to use the Home Assistant Core Integration for now** :warning:
 
 

![validate_badge](https://github.com/muppet3000/growatt_server_hacs/actions/workflows/validate.yml/badge.svg)
[![hacs_badge](https://img.shields.io/badge/HACS-Default-41BDF5.svg?logo=homeassistantcommunitystore)](https://github.com/hacs/integration)
[![bmab_badge](https://img.shields.io/badge/Buy_Me-A_Beer-FFDD00.svg?logo=buymeacoffee)](https://www.buymeacoffee.com/muppet3000)

# Growatt Server Home Assistant Custom Component (growatt_server_hacs)
This custom component (installable via HACS) replaces the original [growatt_server](https://www.home-assistant.io/integrations/growatt_server/) integration that is currently part of the Core Home Assistant repository.

The integration will be removed from the core repository due to various issues with the authentication mechanism for Growatt (Growatt keep blocking the python library), using the HACS system will allow for more dynamic responses to the changes made by Growatt.

# Implementation
On initial release this plugin is an identical copy of the original integration that was part of the Home Assistant release. Going forward, this will be the only place that the Growatt integration for Home Assistant is updated. The original implementation will be removed from Home Assistant Core in due course. (This README will be updated when this happens).

# Installation
This integration can be installed via HACS for Home Assistant
1. [Install HACS](https://hacs.xyz/docs/setup/prerequisites) (Follow all the way through to the 'Configuration' page)
1. In HACS search for & install this integration:
    1. Click 'HACS' on the left menu
    1. Click 'Integrations'
    1. Click 'Explore & Download Repositories'
    1. Search for 'Growatt Server HACS' & click it
    1. Click 'Download' and follow on-screen instructions
1. Once the plugin is installed via HACS configure it just like a normal Home Assistant Integration i.e. from Settings -> Devices & Settings -> Add Integration -> Search for Growatt Server HACS

or (if you don't want to use HACS)

1. Download the latest release to your custom_components folder inside the Home Assistant configuration directory and unpack it

# More Info
Please read the info.md file [here](https://github.com/muppet3000/growatt_server_hacs/blob/main/info.md) for more information, including the roadmap for the integration.
