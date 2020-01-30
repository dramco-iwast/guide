---
layout: default
title: Sensors
has_children: true
nav_order: 2
has_toc: true
---

# Sensors

## Reading Sensor Data
There are two approaches to read sensor data.
During the configuration, you can opt to use polling and/or interrupt-based communication.
The former is used when you want to periodically retrieve data from the sensor bord.
The latter can be used when you only want to know whether the measurement of interest is above or below a preset threshold.

| Sensor type   | Number     | Interrupt- or polling-based communication? | 
| ------------- |:-------------:|:-------------:| 
| Sound level sensor     | 3-10 (varies over schools) | Interrupt and polling |
| Environmental sensor      | 0-3 (varies over schools)  |  Interrupt and polling |
| Button sensor | 10      | Interrupt |


