# Hub

## Parts List

- Intel NUC
- [Z-Wave USB stick](https://www.amazon.com/gp/product/B00X0AWA6E/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- Bluetooth dongle

## Setup

I installed [hass.io](https://www.home-assistant.io/hassio/) (built on top of [Home Assistant](https://www.home-assistant.io/)) on the NUC. Unfortunately, the [download from hassio](https://www.home-assistant.io/hassio/installation/) is not an installer, but an image. I followed [this guide](https://community.home-assistant.io/t/my-steps-to-success-for-hass-io-on-intel-nuc/43915/127) to successfully image the NUC.

## Other Hass.io Addons

1. [Portainer](https://github.com/hassio-addons/addon-portainer) to easily manage containers that are NOT installed through hassio’s community add-ons
2. [Glances](https://community.home-assistant.io/t/community-hass-io-add-on-glances/97102) to monitor NUC’s resources (in case I end up with it being over-allocated on resources)
3. [MQTT Server and Web Client](https://community.home-assistant.io/t/community-hass-io-add-on-mqtt-server-web-client/70376) for services requiring MQTT, a lightweight message queue
4. [Visual Studio Code in Home Assistant](https://github.com/hassio-addons/addon-vscode) to make editing the configuration files on the device enjoyable (also offer IntelliSense for your defined devices)
5. [Samba Share](https://www.home-assistant.io/addons/samba/) (to more easily upload voice assistants)
6. [Snips.ai](https://www.home-assistant.io/addons/snips/) for voice AI completely on the device (not Alexa, cloud, or eavesdropping)
