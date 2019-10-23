# Network Setup

## Network-wide Ad Blocking

[AdGuard](https://www.home-assistant.io/components/adguard/) or pihole work. [Install](https://www.home-assistant.io/hassio/installing_third_party_addons/) on of them as Hass.io integrations.

## DNS Server

I use AdGuard (can also use pihole) as a DNS server, so that I can resolve local resources by domain a local domain name; e.g. `something.lan` or `something.your-local-domain`.

> By default, port 53 (used by the DNS server) is already in use in Ubuntu.

### Free port 53

**WARNING**: This currently prevents the ubuntu host from being able to access the Internet. :disappointed:

```shell
sudo systemctl disable systemd-resolved
sudo systemctl stop systemd-resolved
sudo systemctl restart NetworkManager
```

> **Don't forget to set the DHCP server (cloud key) to use this local DNS server before others**

## Reverse Proxy

This section will enable mapping IP and ports to domains; e.g. instead of using `http://ip:8123` for home assistant, you could use `http://ha`, `http://ha.lan`, etc.

### Install NGINX Proxy Manager

From the hass.io community: [NGINX Proxy manager](https://github.com/hassio-addons/addon-nginx-proxy-manager)

> The default username:password can be found in the logs after installing and starting the service.

Open the web UI, log in, then you can add proxy hosts. This will allow you to map a domain to an IP and port.

> **Warning**: don't forget to setup DNS to resolve your proxies to the proper IP address in AdGuard/piHole.

## Dynamic DNS

## SSL and Secure HTTPS Access

## OpenVPN

For remote access to your network via a VPN, setup OpenVPN Access Server via this [docker image](https://hub.docker.com/r/linuxserver/openvpn-as/).

> Ensure ports 943, 9443, and 1194/udp are forwarded to your hub.

```shell
docker create \
  --name=openvpn-as \
  --cap-add=NET_ADMIN \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=US/Atlanta \
  -p 943:943 \
  -p 9443:9443 \
  -p 1194:1194/udp \
  -v /docker/openvpn-as/config:/config \
  --restart unless-stopped \
  linuxserver/openvpn-as
```

## Other Features

Guest network with a [Guest Portal](https://help.ubnt.com/hc/en-us/articles/115000166827-UniFi-Guest-Network-Guest-Portal-and-Hotspot-System).
