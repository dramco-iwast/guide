---
layout: default
title: What is polling?
parent: Configuration
grand_parent: SP 4 Onderzoeksopzet
nav_order: 2
---

Some sensors can be polled.
This means that the motherboard periodically requests the current status of the sensor.
The periodicity can be configured with the configuration tool.
In order to reduce the power consumption of the IoT system, we suggest using an interrupt based approach opposed to using polling.
The fastest you can poll your sensor is every minute.

A polling interval of 0 indicates that polling is disabled, and therefore that only thresholding is used to determine when to transmit data.
