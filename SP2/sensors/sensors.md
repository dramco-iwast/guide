---
layout: default
title: Sensoren
parent: SP 2 Randvoorwaarden IoT systeem
has_children: true
nav_order: 2
has_toc: true
---

# Sensoren

## Beschikbare sensoren
- Vermogen/lichtsensor (power/light sensor)
- Omgevingssensor (environmental sensor)
- Geluidsniveausensor (sound level sensor)
- Drukknopsensor (button sensor)

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
| Power | 10 | Interrupt and polling |

In the table below you can find the minimum and maximum values `TL` and `TH` can take, for each physical quantity and each sensor.

| Sensor type   | Physical quantity     | minimum | maximum |
| ------------- |:-------------:|:-------------:|:-------------:| 
| Sound level sensor     | Sound level (dB) | 75 | 120 |
| Environmental sensor      | Temperature (&deg;C)  | -40  | 100 |
| Environmental sensor      | Air pressure (hPa)  | 0  |	65000 |
| Environmental sensor      |  Humidity (%) | 0  | 100	|
| Environmental sensor      | Air quality (no unit)  | 0  |	600 |
| Button sensor | - (no thresholding)  |  - (no thresholding) | - (no thresholding) |
| Light sensor      | Illuminance (lux) | 0  |	65535 |
| Power      | Battery voltage (V) | 0  |	4.20 |


Pay attention! Due to the manner in which sound levels are calculated, the measured sound level is always at least 70 dB. 
Therefore it does not make sense to try to measure 'quiet' sounds.
It is also not allowed to set thresholds lower than 75 dB, as this will lead to constant data transmission, which consume a lot of power and will drain the battery.

