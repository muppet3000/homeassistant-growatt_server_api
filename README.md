# Growatt Server HomeAssistant Custom Component (growatt_server_hacs)
This custom component (installable via HACS) replaces the original growatt_server integration that used to be part of the core Home Assistant repository.

The integration was removed from the core repository after various issues with the authentication mechanism for Growatt (Growatt keep blocking the python library), using the HACS system will allow for my dynamic responses to the changes made by Growatt.

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
    
