---
layout: default
title: Button Sensor
parent: Sensors
nav_order: 3
has_toc: true
---

# Button Sensor


![](../assets/images/button-sensor.jpg)

The button sensor contains four buttons.
Whenever a button is pressed, the motherboard sends a message to the could specifying which button was pressed.

This sensor does not need to be configured.

Let op! In het huidige systeem is geen terugkoppeling voorzien. Het is mogelijk data van sensoren op te vragen en te analyseren, maar signalen uitsturen kan momenteel (nog) niet! De communicatie is dus eenzijdig: de sensormodules kunnen gegevens uitsturen, maar kunnen - op dit moment - nog geen gegevens ontvangen. (Dus bv. een deur openen of een lichtje doen branden als een drukknop ingedrukt wordt, is voorlopig niet mogelijk).

## Applications
- Stem-applicaties
	* Bv. groepjes in de klas stemmen over juiste antwoord op vragen van leraar (quasi real-time)
	* Bv. tevredenheid over het eten in het schoolrestaurant monitoren (niet real-time)
- Alarm
	* Bv. in gezondheidszorg: verpleegster oproepen met indicatie hoe dringend
	* Bv. valdetectie bij ouderen