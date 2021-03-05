---
layout: default
title: IWAST systeem
parent: Internet der Dingen
grand_parent: SP 2 Randvoorwaarden IoT systeem
nav_order: 4
has_toc: true
---
# Het IWAST Systeem
Het “IoT with a soft touch”-systeem bestaat uit
1. Een gateway/toegangspoort. Naar de gateway worden de sensorgegevens draadloos doorgestuurd.
2. Moederborden, die een batterij en de elektronica die nodig is voor de draadloze communicatie bevatten, waarop telkens sensoren kunnen aangesloten worden
3. Sensoren, ook wel dochterborden genoemd. Het overzicht van de sensoren, hun aantallen en mogelijke toepassingen staat [hier](./SP2/sensors/sensors.html).

De moederborden maken een draadloze connectie met de gateway. 
De gegevens van de sensoren, aangesloten op elk moederbord, worden naar de gateway doorgestuurd. 
De gateway is verbonden met de server, waar de sensorgegevens opgeslaan worden. 
De data is toegankelijk via een website, zowel via de computer, als via de smartphone. Meer informatie kan je [hier](./Platform) terugvinden.

![](../../assets/images/setup.svg)

Let op! In het huidige systeem is geen terugkoppeling voorzien. Het is mogelijk data van sensoren op te vragen en te analyseren, maar signalen uitsturen kan momenteel (nog) niet! De communicatie is dus eenzijdig: de sensormodules kunnen gegevens uitsturen, maar kunnen - op dit moment - nog geen gegevens ontvangen. (Dus bv. een deur openen of een lichtje doen branden als een drukknop ingedrukt wordt, is voorlopig niet mogelijk).

# Draadloze communicatietechniek
Zoals hierboven aangehaald heeft de draadloze communicatietechniek een invloed op het energieverbruik van de moederborden. Zoals in elk ontwerpprobleem moet ook bij de keuze van de draadloze communicatietechnologie een evenwicht gezocht worden tussen verschillende vereisten. “There is no such thing as free lunch”: je kan niet alles krijgen in het leven wat je zou willen. Binnen dit project werd gekozen voor de communicatietechnologie LoRa (Long Range). 
We lijsten hieronder de voor- en nadelen van LoRa-communicatie op:
- <i class="fas fa-plus"></i> energiezuinig: de draadloze communicatie kost niet veel energie, waardoor de sensormodules lang op eenzelfde batterij kunnen functioneren zonder dat de batterij moet vervangen worden. Bij optimale condities zou een batterijduur langer dan jaar geen uitzondering zijn.
+ <i class="fas fa-plus"></i> groot draadloos bereik: de sensoren kunnen tot op grote afstand gegevens naar de gateway doorsturen. In sommige gevallen tot wel 40 km ver! In praktische omstandigheden kan je berichten sturen tot wel enkele kilometers ver.
- <i class="fas fa-minus"></i> Beperkte hoeveelheid data die kan doorgestuurd worden binnen een vast tijdsinterval. Daardoor is het niet mogelijk geluid of video continu door te sturen. Afhankelijk van het aantal en type sensoren kunnen sensormodules ongeveer om de 5 minuten de sensorwaarden doorsturen.

## Belangrijke informatie voor leerkrachten

- Er werden twee tools ontwikkeld:
	* Configuratie-tool: De configuratie-tool wordt eenmalig gebruikt om de sensoren te configureren nadat ze aan het moederbord aangesloten zijn.
		- Configuratie van de sensoren houdt in dat bepaalde parameters ingesteld worden
			* Bv. voor geluidsniveau-sensor: drempelwaarde voor geluidsoverlast
			* Bv. voor temperatuur-sensor: interval waarop meetwaarden moeten doorgestuurd worden.
		- De parameters per sensor worden op een intuïtieve manier weergegeven in de configuratie-tool. We voorzien een documentatie over de betekenis van de parameters indien nodig.
		- De configuratie-tool wordt lokaal op een computer geïnstalleerd.
		- Minimum versie besturingssysteem voor configuratie-tool: windows 7
		- De computer hoeft niet permanent internetconnectie te hebben, maar haalt wel updates op online. Bij eventuele updates is het niet noodzakelijk de configuratie-tool manueel te updaten of opnieuw te installeren.
		- We gaan na of admin-rechten nodig zijn om de configuratie-tool op de schoolcomputers te installeren. Indien dit admin-rechten nodig zijn, maar de IT-dienst dit niet toelaat, zullen de leerlingen/leerkracht zelf een laptop moeten voorzien.
	* Web-interface: de web-interface is toegankelijk via een internet browser en laat toe de sensorgegevens weer te geven in een tabel en indien gewenst ook in een grafiek.
		- De sensorgegevens of een selectie daarvan kunnen ook gedownload worden in csv-formaat voor verdere verwerking, bv. in Python als programmeeroefening of in excel.
	* In de rugzak wordt een gateway voorzien. Gebruik van de gateway is enkel nodig als de school niet binnen de dekking van The Things Network valt. The Things Network is een open source netwerk voor IoT toepassingen gebaseerd op LoRa. 
	* Als leerlingen een probleemstelling buiten de scope van het huidige project willen onderzoeken of behandelen, kunnen we op ad-hoc basis onderzoeken of het mogelijk en opportuun is hier verder zaken voor te ontwikkelen. Dan ontmoeten wij de leerlingen graag om hun motivatie te peilen en de kwaliteit van hun project in te schatten.







