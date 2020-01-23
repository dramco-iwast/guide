---
layout: default
title: Configuration
has_children: true
nav_order: 3
has_toc: true
---

# Configuration


## Reading Sensor Data
There are two approaches to read sensor data.
During the configuration, you can opt to use polling and/or interrupt-based communication.
The former is used when you want to periodically retrieve data from the sensor bord.
The latter can be used when you are only interessted in if a certain value is above or below a threshold.

### Interrupt-based Communication
In case of interrupt-based communication, the sensor wakes up the motherboard when it has data.
Whereafter the motherboard reads the data from the sensor.
In this way the motherboard can go to sleep, knowing it will be interrupted by the sensor when needed.

### Polling-based Communication
In contrast to interrupt-based communication, the motherboard will actively poll the sensor to request the data.
As a result the motherboard needs to periodically wake up when it wants to read-out the sensor.