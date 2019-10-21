# Audio/Video

I have most of all my AV equipment connected to Home Assistant; PS4, gaming-pc, AVRs, TVs and streaming devices.

## Control

The PS4 control uses this [integration](https://www.home-assistant.io/integrations/ps4/) to control turning **both on** and off.

The gaming-pc (Windows) is turned on via [wake-on-lan integration](https://www.home-assistant.io/integrations/wake_on_lan/) and turned off via [RPC shutdown integration](https://www.home-assistant.io/addons/rpc_shutdown/).

The AVR is controlled both via the network (using the [Denon integration](https://www.home-assistant.io/integrations/denonavr/)) **AND** Harmony Hub via IR. The reason for using the Harmony Hub is to be able to **reliabily turn on** the AVR. I have had mixed success with using wake-on-lan.

The TV is also controlled with IR via the Harmony Hub. While LG TVs can be controlled via the [LG integration](https://www.home-assistant.io/integrations/webostv/) or [Samsung integration](https://www.home-assistant.io/integrations/samsungtv/), it is not able to turn on the TV; only turn it off. Wake-on-LAN also gave mixed results; with the TV appearing to go into a deep sleep.

> I ONLY USE THE HARMONY HUB AS AN IR TRANSMITTER. I actually do not plan on even using the remote; only the hub. I have all the things automated via home assistant for home theater activities.

## Automation

I use automated **predefined audio levels**. **TV mode** for normal watching while **theater mode** is ideal for a home theater experience. However, if you want to control the volume more granularly than predefined levels, a physical remote is ideal. We use the AppleTV 4K remote for this purpose currently. See below for more details.

## Streaming Devices

> I decided to use a Chromecast Ultra and AppleTV 4K; completely dropping the Roku 4K Ultra.

Chromecast makes it super easy for guests. They just cast from their phone, it turns on the TV and turns it off when they are done casting. No remotes or things to explain on how to use the TV.

For our use, I use the AppleTV 4K; primarily because apparently Roku currently have issues playing Dolby Digital Plus sound which causes it to sometimes just stop outputting sound altogether. Although they are much easier to automate, we opted to not use them. Also, it means when you want to tweak the volume (versus setting to pre-defined levels), the AppleTV 4K remote can not only do it but looks the nicest.
