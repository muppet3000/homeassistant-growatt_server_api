# FAQ
This page is intended to cover FAQs associated with the Growatt Integration for Home Assistant, not Home Assistant iteself

#### Table of Contents
- [How do I increase the update interval to be more than every 5 minutes](#how-do-i-increase-the-update-interval-to-be-more-than-every-5-minutes)
- [How do I configure my ShineLink/Wifi Dongle to update more often](#how-do-i-configure-my-shinelinkwifi-dongle-to-update-more-often)
- [How do I share my credentials with you for testing/adding new features for my system type](#how-do-i-share-my-credentials-with-you-for-testingadding-new-features-for-my-system-type)

## How do I increase the update interval to be more than every 5 minutes
Firstly you need to ensure your ShineLink/Wifi Dongle is configured to push updates to the server more regularly, see [here](#how-do-i-configure-my-shinelinkwifi-dongle-to-update-more-often)

Once you have configured your system to push updates to the server more frequently follow these steps:
1. Navigate to the 'automations' in area in your Home Assistant instance
<kbd>![image](https://user-images.githubusercontent.com/10612068/212285861-6028a930-c09d-436f-a695-64a300fd7064.png)</kbd>
1. Click on `Create Automation`:
<kbd>![image](https://user-images.githubusercontent.com/10612068/212546882-c54321e6-af4d-473f-b64a-5acff19d5560.png)</kbd>
1. Click `Start with an empty automation`:
<kbd>![image](https://user-images.githubusercontent.com/10612068/212547087-36131043-012e-4103-8e2e-693c545a6aef.png)</kbd>
1. In `Triggers` select `Add Tigger`
1. Select `Time pattern`
1. Enter the frequency in minutes that you wish the Integration to pull updates. Ensure you put a `/` before the number e.g `/1` for 1 minute.
**NOTE - The integration has a throttle of 1 minute, therefore any more frequent than that is pointless**
<kbd>![image](https://user-images.githubusercontent.com/10612068/212547381-d53da02a-da56-4daf-a812-463503200233.png)</kbd>
1. No values are required in `Conditions`
1. In Actions select `Add Action`
1. Select `Call Service`:  
<kbd>![image](https://user-images.githubusercontent.com/10612068/212547619-d72ea220-121a-40a1-98df-130e74355075.png)</kbd>
1. In the box that appears type `update` and then select `Home Assistant Core Integration: Update entity`:
<kbd>![image](https://user-images.githubusercontent.com/10612068/212547909-27629a04-00fd-4972-b0e3-bc4ef86e1751.png)</kbd>
1. In the `Targets` section of the resulting box select `Choose Device`:
<kbd>![image](https://user-images.githubusercontent.com/10612068/212548125-0c5234c2-37be-423f-992f-4533ee91111b.png)</kbd>
1. Then select your Growatt devices, there will be 2, one for `Totals` and one for your Inverter, make sure you add them both:
<kbd>![image](https://user-images.githubusercontent.com/10612068/212548187-a7257f60-ed21-404f-a051-dc0227c2789d.png)</kbd>
You'll end up with something like this:
<kbd>![image](https://user-images.githubusercontent.com/10612068/212548329-c32a7949-602f-481e-bfd6-e3589d81428d.png)</kbd>
1. **DO NOT SKIP THIS STEP** You must expand the two devices into their full entity list by clicking the `<>` image on each of them:
<kbd>![image](https://user-images.githubusercontent.com/10612068/212548877-32e2946c-436f-49b8-9428-9d114c1ea63d.png)</kbd>
1. Once you've expanded all entities you'll see something like this (yes, it's messy, but it works):
<kbd>![image](https://user-images.githubusercontent.com/10612068/212548913-541990b8-f4d0-459e-8d8a-6b5d1873dd68.png)</kbd>
1. The whole automation should look something like this (when everything is minimised):
<kbd>![image](https://user-images.githubusercontent.com/10612068/212548983-16e06ac4-3398-40e0-83f2-6ae6d0ce6bb1.png)</kbd>
1. Click `Save` and give the automation a useful name and it will then trigger every X minutes based on your selection


## How do I configure my ShineLink/Wifi Dongle to update more often
You need to know the IP address of your ShineLink/Wifi Dongle, this will vary depending on your home network setup and isn't something I can help you with. 

Typically looking on your router's configuration or DHCP server you will find something that looks like it. 

Once you know its IP address enter it into your browser and you'll find something like this:
<kbd>![image](https://user-images.githubusercontent.com/10612068/212528884-f7d7c44e-6a98-47f7-931c-fc035c3a4f5d.png)</kbd>

Enter the credentials (admin/admin by default), and you'll be shown the Datalogger information page, from here click on `Network Setting`:
<kbd>![image](https://user-images.githubusercontent.com/10612068/212528973-f2a5f248-2211-4154-b5aa-f272b5967985.png)</kbd>

On the Network Settings page change the `Data Transfer interval` to one of your choosing (lowest is 1 minute), then click `Save`
<kbd>![image](https://user-images.githubusercontent.com/10612068/212528966-c131c5aa-b478-4753-9648-4d0cbc381169.png)</kbd>

After this your ShineLink/Wifi Dongle will start pushing data more frequently to the Growatt Servers

## How do I share my credentials with you for testing/adding new features for my system type
Firstly - You have to acknowledge that you are willing to provide access to a complete stranger, that requires trust, if you're uncomfortable with this, stop reading now.
If you're still reading, follow the steps below:
1. Log in to the [growatt website](https://server.growatt.com)
1. Click 'Setting':
<kbd>![image](https://user-images.githubusercontent.com/10612068/212376925-18a13715-0503-40b1-99fe-4cca209fd6cb.png)</kbd>
1. Click 'Browse Account', then 'Add'
<kbd>![image](https://user-images.githubusercontent.com/10612068/212377188-206541b5-b4fa-4cec-935d-d985845d0c22.png)</kbd>
1. Fill out the Form with the required information
    1. **User Name** - Must be unique - Multiple people have already sent ones based on my username which is difficult to get alternatives for, instead pick something completely random
    1. **Email** - Please use my email address: c.m.straffon@gmail.com (I will get an email when the account is created then)
    1. **Password** - A Password of your choice
    1. **Again** - The password again
<kbd>![image](https://user-images.githubusercontent.com/10612068/212377862-c38a0e5e-c8d4-426a-a968-2703362bc680.png)</kbd>
1. Click 'Yes'

At any point if you become uncomfortable with me having access you can simply delete the user and my access is revoked
