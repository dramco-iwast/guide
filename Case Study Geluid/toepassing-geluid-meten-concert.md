---
layout: default
title: Hoe geluid meten?
parent: Case study geluid
nav_order: 5
---

# Toepassing: geluid meten op een concert

## Theoretische basis

### Geluidsnormen
Geluid afkomstig van muziekactiviteiten kan opgedeeld worden in drie categorieën die bepaald worden aan de hand van het equivalent continu geluidsniveau (L<sub>Aeq</sub>). 
Dit is het constante geluidsdrukniveau dat gedurende een tijdsduur T dezelfde energie levert als de werkelijk gemeten geluidsdrukniveaus gedurende die tijdsduur T. 
Dit kan bijvoorbeeld zeggen dat het geluid over een periode van 15 minuten gemeten wordt en het gemiddelde lager moet zijn dan 95 dB. 
De 3 categorieën met bijhorende voorwaarden zijn hieronder weergegeven.

- **Categorie 1**: geluidsniveau <85 dB(A)L<sub>Aeq, 15min</sub>
- **Categorie 2**: geluidsniveau > 85 dB(A)L<sub>Aeq, 15min</sub> en <= 95 dB(A)L<sub>Aeq, 15min</sub>
- **Categorie 3**: geluidsniveau > 95 dB(A)L<sub>Aeq, 15min</sub> en <= 100 dB(A)L<sub>Aeq, 60min</sub>

In theorie kan voor elke muziekactiviteit gekozen worden welke categorie van toepassing is. 
In de praktijk zijn de organisatoren echter vaak ook beperkt tot een maximale categorie omwille van omgevingsfactoren zoals bijvoorbeeld de buren. 

### Open lucht vs in een kamer
Een puntbron, een begrip uit de theorie van trillingen en golven, is een in een punt geconcentreerd gedachte trillingsbron, bijvoorbeeld van geluid, licht, of van watergolven, waarvandaan de energie zich in alle richtingen gelijkelijk uitbreidt.

In this article, we will examine the effect of multipath propagation to a transmitted signal. Furthermore, we will illustrate the effect with the help of audio examples (scroll down for the examples).

First, let's try to understand the transmission of a signal from a source S to a destination D, which are d meters apart:

 

If we assume, the signal travels with velocity c, it will take τ=dc seconds until it arrives at the destination. Mathematically, we have

y(t)=x(t−dc),
where x(t) is the transmitted signal and y(t) is the received signal. Now, we know that the signal from the source is not only transmitted into the direction of D, but in all directions. Let's assume somewhere around the source, there is a big wall that can reflect the signal:

 

So, at the destination we receive two copies of the signal: One over the path of d meters and one over the path of d1 + d2 meters. Let us assume that the reflection of the signal at the wall removes 50% of the amplitude from the signal. Then, the received signal at the destination can be mathematically written as

y(t)=x(t−dc)+0.5⋅x(t−d1+d2c).
This characteristic is named multipath propagation, since the signal can arrive at the destination via multiple different paths.

Geluid afkomstig van een geluidsinstallatie (de *geluidsbron*) zal in open lucht .

Hoe rekening houden met verzwakking owv afstand en andere factoren

Eventueel: hoeveel microfoons nodig / op hoeveel plaatsen geluid meten om vast te stellen dat geluidsniveau nergens overschreden wordt? Evtl simuleren?

## Praktische uitvoering

Formuleer nauwkeurig je onderzoeksvraag: wat wil je precies meten en wat wil je hieruit besluiten?
Bv: wordt het toegestane geluidsniveau overschreden tijdens het vrijpodium georganiseerd op de speelplaats van onze school?
Hiervoor moet je weten wat het toegestane geluidsniveau is!

###Configuratie van de IWAST-microfoon

- Ga na of je geluid wilt opmeten via interrupt-gebaseerde communicatie of via polling. (LINKS TOEVOEGEN)
- Ga na welke parameters je wilt gebruiken:
-- Voor polling: om de hoeveel tijd wil je het geluidsniveau opvragen?
-- Voor interrupt-gebaseerde communicatie: welke drempelwaarde wil je gebruiken? 
Mogelijks moet je hier een correctie invoeren voor de verzwakking die optreedt omwille van de afstand tussen de *geluidsbron* en de *sensor*.
In een multipad omgeving moet je mogelijks nog extra corrigeren, maar dit moet je onderzoeken voor de concrete ruimte waarin je het geluidsniveau wilt testen.
- Open de configuratie-tool en volg de stappen [hier](../Configuration/configuration-tool.html).
- Installeer het moederbord en de geluidssensor op een geschikte plek (dicht genoeg bij de geluidsbron). 
Maak indien nodig de set-up waterdicht.

###Geluidsinformatie opmeten met IWAST

Ga naar het [webplatform](../Platform/platform.html) en download de data.

###IWAST data analyseren om geluidsoverlast vast te stellen

Analyseer de data met een computerprogramma naar keuze.
Documentatie voor analyse in Excel en Python vind je [hier](../Data Manipulation/data-manipulation.md).
