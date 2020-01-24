---
layout: default
title: Wireless Communication
has_children: true
nav_order: 3
has_toc: true
---

# Wireless Communication
The motherboards host a LoRaWAN modem to provide a wireless connection.
LoRaWAN is a Low-Power Wide-Area Network technology allowing to wirelessly transmit small amaount of data over a large range.

Such a network consist of end-devices which communicate with gateways. These gateways relay the messages to the cloud:
![](https://www.thethingsnetwork.org/docs/network/overview.png)


In this project, we use the [The Things Network](https://www.thethingsnetwork.org/) (TTN) system.
Everyone can add gateways to this network in order to extend the network.
In case there is no coverage by the TTN, we will provide a LoRaWAN network.
You can view the active gateways on the [TTN map](https://www.thethingsnetwork.org/map).
Ensure there is a gateway present in at least a range of 1km of your devices.


## LoRaWAN Gateway
In case there is no coverage by the TTN, we will provide a LoRaWAN Gateway.

### Network Access
To be able to use the gateway, the firewall needs to allow TCP communication over port 1700 to and from `router.eu.thethings.network`.

- TCP port: `1700` (up/down)
- Destination: `router.eu.thethings.network`



