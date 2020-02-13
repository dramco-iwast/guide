---
layout: default
title: F.A.Q.
has_children: false
has_toc: true
---

# F.A.Q.


## Moederbord

##	Hoe groot is het geheugen (voor de sensordata) van het moederbord? Is het mogelijk om via interrupts (bv met de stemknoppen) gedurende bv. een halfuur veel input door te sturen als je daarna 24 uur stil ligt, of zal de data dan toch gedropt worden?
TODO


##	Kan je data rechtstreeks uitlezen van moederbord naar computer? Bv. om na te gaan hoe vaak je interrupts genereert met een bepaalde instelling voor de thresholds?
Dit is momenteel niet mogelijk met de huidige firmware op het moederbord. We bekijken of het gewenst is om deze feature toe te voegen.

## Batterij

### Kan je het batterijniveau vanop afstand uitlezen? Of een signaal sturen als het batterijniveau onder een bepaalde threshold zakt?
Dit is niet mogelijk met de huidige hardwareversie van het moederbord. Dit sluit niet uit dat deze feature niet in een volgende versie kan voorzien worden.


## Geluidsensor

### Waarom is een DFT nodig bij het bepalen van het geluidsniveau? Wordt hier al een perceptuele weging (bv A-weging) toegepast?
TODO

###	Welk tijdsinterval wordt gebruikt om het geluidsniveau te bepalen?
400 samples aan 20 Hz = 20 seconden

###	Hoe kan het dat je 0dB kan opmeten? Fysisch verwacht je toch steeds minstens 10-20 dB op te meten?
TODO
