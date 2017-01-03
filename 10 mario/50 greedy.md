# Greedy

## tl;dr
Implementeer een programma dat het minimaal aantal muntjes uitrekent om wisselgeld te geven. 

```
Hoeveel wisselgeld moet er gegeven worden? 0.41
4
```

## Background

![](coinchange.png)

In een ver verleden toen er nog actief werd betaald door middel van contanten was een muntenhouder als hierboven onmisbaar. Het vervelende is dat er voor elk muntje een levertje moest worden ingedrukt, en dit kost tijd. Gelukkig zijn wij er al computer scientists om het aantal terug te geven muntjes te minimaliseren door middel van "greedy algoritmes".

Een greedy algoritme is een algoritme dat altijd de beste lokale keuze maakt op weg naar een antwoord. Alsof je fietst en dan op elk kruispunt de afslag kiest waarvan jij op dat moment denkt dat die zo snel mogelijk leidt tot je eindbestemming. Dit soort algoritmes leiden voor sommige problemen altijd tot een optimale oplossing, maar niet voor alle problemen.

Stel je voor dat een kassière een klant wisselgeld schuldig staat, en dat deze kassière vervolgens op de levertjes kan drukken om kwartjes (25c), dubbeltjes (10c), stuivers (5c), en centen (1c) te krijgen. Een oplossing voor dit probleem is één of meer drukken op de levertjes, en we willen zo min mogelijk levertjes indrukken. Neem een "gierige" kassière die elke keer als hij op een levertje moet drukken, op het levertje drukt met de hoogst mogelijk waarde welke nog gedrukt mag worden. Bijvoorbeeld als een klant nog 41 cent schuldig staat, dan drukt de kassière eerst op het levertje voor een kwartje. Er blijft dan nog (41 - 25 =) 16 cent over. Nu mag de kassière niet meer drukken op het levertje voor een kwartje, want dan zou hij te veel wisselgeld geven. Dus drukt hij voor een dubbeltje, en daarmee blijft er nog 6 cent over. Dit volgt dan met een druk voor een stuiver, en tot slot een cent. In totaal krijgt de klant dus één kwartje, één dubbeltje, één stuiver, en één cent, dit maakt 4 munten in totaal.

Het blijkt dat deze greedy aanpak altijd een optimale oplossing levert voor dit probleem, met deze munten. Natuurlijk aannnemend dat muntstukken nooit opraken. Hoeveel munten er precies nodig zijn? Dat mag jij ons vertellen!

## Specification

* Schrijf in een bestand genaamd `greedy.py` een programma dat eerst vraagt hoe veel wisselgeld er gegeven moet worden, en vervolgens het minimaal aantal munten uitspuwt.
* Ga er vanuit dat de gebruiker een getal als geheel getal (integer), of als komma getal (float) invult. Het getal achter de komma staat dan voor centen. Dus `3.21` betekent 3 dollar en 21 cent.
* Zorg dat als de gebruiker een float heeft ingevuld, je hiervan een integer maakt. Floating points hebben kleine precisie fouten, en dat wil je niet als je met geld werkt! Je kan door middel van de functie `int` een float converteren naar een integer. Probeer maar eens `int(7.3)` en `int(7.8)`.
* [Slaagt de gebruiker er niet in om correcte input te geven](https://en.wikipedia.org/wiki/Murphy's_law), laat het de gebruiker dan opnieuw proberen.

## Hints

* Vergeet het deel achter de komma niet als je converteert naar een integer!
* Hoe je dit probleem aanpakt is aan jou. Je zou bijvoorbeeld loops kunnen gebruiken of gebruik kunnen maken van de modulo operator `%`. Probeer maar eens `26 % 8`.

## Testing

```
checkpy.test("greedy")
```