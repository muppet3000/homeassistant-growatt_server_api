[![validate_badge](https://github.com/muppet3000/homeassistant-growatt_server_api/actions/workflows/validate.yml/badge.svg)](https://github.com/muppet3000/homeassistant-growatt_server_api/actions)
[![hacs_badge](https://img.shields.io/badge/HACS-Default-41BDF5.svg?logo=homeassistantcommunitystore)](https://github.com/hacs/integration)
[![bmab_badge](https://img.shields.io/badge/Buy_Me-A_Beer-FFDD00.svg?logo=buymeacoffee)](https://www.buymeacoffee.com/muppet3000)
[![paypal_badge](https://img.shields.io/badge/PayPal-Beer_Fund-blue.svg?&logo=paypal)](https://www.paypal.com/paypalme/muppet3000)

# Growatt Server API Home Assistant Custom Component (growatt_server_api)
This custom component (installable via HACS) is an upstream version of [growatt_server](https://www.home-assistant.io/integrations/growatt_server/) integration that is part of the [Home Assistant Core](https://github.com/home-assistant/core/tree/dev/homeassistant/components/growatt_server) repository.

The integration has been through a period of instability due to various issues with the authentication mechanism for Growatt (Growatt keep blocking the python library), using the HACS system will allow for more dynamic responses to the changes made by Growatt.

The changes made in this repository will be rolled up monthly and then submitted as a Pull-Request to the main Home Assistant Core repository for release as an 'official' Integration.

# Implementation
On initial release this plugin is an identical copy of the original integration that was part of the Home Assistant release. Going forward, this will be the upstream release of the Integration and the first place that bugs are fixed & new features are added.

# Installation
This integration can be installed via HACS for Home Assistant
1. [Install HACS](https://hacs.xyz/docs/setup/prerequisites) (Follow all the way through to the 'Configuration' page)
1. In HACS install this integration (this will be simplified once this repository has been added to the default HACS repos via [this](https://github.com/hacs/default/pull/1660) PR):
    1. Click 'HACS' on the left menu
    1. Click 'Integrations'
       <!-- DELETE THIS SECTION ONCE AVAILABLE IN THE DEFAULT REPOS -->
    1. Click the three dots in the top-right corner
    1. Click 'Custom repositories'
    1. In the 'Repository' field enter: `https://github.com/muppet3000/homeassistant-growatt_server_api`
    1. In the 'Category' field select 'Integration'
    1. Click 'Add'
    1. Once the repository is added click on `Growatt Server API`
    1. On the next page select 'Download' in the bottom-right corner
    1. Choose the latest released version and click 'DOWNLOAD'
    1. Click the 'HACS' button in the menu and restart Home Assistant when prompted
    <!-- THIS WILL WORK WHEN IT'S IN THE DEFAULT REPOS
    1. Click 'Explore & Download Repositories'
    1. Search for 'Growatt Server HACS' & click it
    1. Click 'Download' and follow on-screen instructions
    -->
1. Once the plugin is installed via HACS configure it just like a normal Home Assistant Integration i.e. from Settings -> Devices & Settings -> Add Integration -> Search for Growatt Server API

or (if you don't want to use HACS)

1. Download the latest release to your custom_components folder inside the Home Assistant configuration directory and unpack it

# More Info
Please read the info.md file [here](https://github.com/muppet3000/homeassistant-growatt_server_api/blob/main/info.md) for more information, including the roadmap for the integration.
