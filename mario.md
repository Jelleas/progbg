# Module 1: Mario

## tl;dr
* Installeer Python en checkpy
* Test jouw Python en checkpy installatie met `hello.py`
* Controleer je waterverbruik met `water.py`
* Bouw één van Mario's pyramides met `mario.py`
* Reken wisselgeld uit met `greedy.py`
* Submit!

## Getting Started (Python)

Python is zelf een programma, en moet dus waarschijnlijk nog geïnstalleerd worden op je computer. Wij gebruiken bij deze cursus standaard de *Canopy*-distributie; een pakket met Python en een heleboel handige functies om te hergebruiken. Canopy is gratis voor gebruik in het onderwijs.

Canopy kun je [hier](https://store.enthought.com/downloads/) downloaden. Als het goed is, wordt op de website automatisch de juiste versie voor jouw systeem geselecteerd. Druk op de knop "DOWNLOAD Canopy" om te starten.

- Op *Windows* bestaat de download uit een **.exe**-bestand. Dubbelklik om de installatie te starten. In principe kun je alle standaardopties accepteren, maar [hier](http://docs.enthought.com/canopy/quick-start/install_windows.html) staat nog wat meer uitleg.
  
- Op *Mac* is het een **.dmg**-bestand. Indien nodig, dubbelklik om het te openen. Sleep dan "Canopy" naar *Applications* en start het daarna op om de installatie af te ronden. In principe kun je alle standaardopties accepteren, maar [hier](http://docs.enthought.com/canopy/quick-start/install_macos.html) staat nog wat meer uitleg.

Kijk hier voor meer uitleg over Canopy:

![embed](https://player.vimeo.com/video/137728514)


## Getting Started (checkpy)

We gebruiken een programma om te checken of je opdrachten op de juiste manier werken. We vragen je om heel precies te zijn in het geven van de juiste uitvoer!

Om zelf het check-programma te downloaden, moeten we een opdracht invoeren in de "Canopy Command Prompt" of "Canopy Terminal". Deze vind je in de Editor, in het menu genaamd "Tools". Je krijgt een apart scherm waar je commando's kunt intikken. Voer het volgende in:

	pip install checkpy

Je kunt nu de command prompt of terminal weer sluiten. Vervolgens ga je in de Canopy Editor naar de Python Pane, waar je Python-commando's in kunt voeren. Eerst `importen` we checkpy:

	import checkpy

En dan downloaden we éénmalig de checks:

	checkpy.download("https://github.com/Jelleas/progBG2017Tests")

Het checken zelf doe je dan als volgt, bijvoorbeeld om het programma `priem100.py` te controleren:

	checkpy.test("hello")

Ben je klaar met de hele opdracht, check dan nog een keer de hele module:

	checkpy.testModule("module1")

Checkpy is erg streng. Toch is het echt de bedoeling dat je zorgt dat je programma de check door komt. Mocht je niet begrijpen waarom je antwoord wordt afgekeurd, spreek dan meteen een docent aan tijdens het practicum. We kijken dan met je mee.


## What to Do
* Implementeer `hello`
* Implementeer `water`
* Implementeer `mario`
* Implementeer `greedy`


# Hello

## tl;dr
Implementeer een programma dat een simpele begroeting uitprint als volgt:

```
Hello, world!
```

Voor context zie [wikipedia](https://nl.wikipedia.org/wiki/Hello_world_(programma))


## Specification
Tijd om ons eerste programma te schrijven. Maak via de Canopy editor een nieuwe file aan (ctrl+n of cmd+n) en sla deze in een plek naar keuze op als `hello.py` (ctrl+shift+s of cmd+shift+s). Een tip hierbij is om jouw bestanden op te slaan in Dropbox, zo kun je altijd je bestanden terughalen. Plaats in deze file het volgende stukje Python code:

```
print "Hello, world!"
```

Zie hoe sommige delen van de tekst anders kleuren in de editor. Dit is "syntax highlighting" wat door de editor wordt toegevoegd om stukken code voor jou als programmeur uit te lichten. 

Sla nu je bestand op (ctrl+s of cmd+s), en run deze door middel van de run knop bovenin de editor. Als het goed is zie je nu in de Python terminal de tekst `Hello, world!` staan.


## Testing
Test eerst je programma zelf. Staan er bijvoorbeeld geen extra hoofdletters of missende uitroeptekens in het resultaat?

Ben je tevreden? Test je programma dan met checkpy. Dit doe je door de volgende regels Python code uit te voeren in de Python terminal:

```
import checkpy
checkpy.test("hello")
```

Als je alleen maar happy smileys ziet dan slagen de tests, en kun je nu verder met de volgende opdracht. Slagen ze niet, dan is het tijd om te debuggen. Zie je de volgende error "No such file or directory:", probeer dan eens rechts te klikken de in Python terminal en het volgende aan te vinken:

![](sync.png)

Was dit niet het probleem? Kijk dan nog eens goed naar je code, staat er bijvoorbeeld geen extra spatie ergens? Kom je er niet uit, tik even een assistent aan!


# Water

## tl;dr

Implementeer een programma dat een gebruiker zijn waterverbruik reporteert, door het aantal minuten douchen te converteren naar flesjes drinkwater.

```
Hoe veel minuten douche je? 1
12

Hoe veel minuten douche je? 10
120
```

## Specification

* Schrijf in een nieuwe file genaamd `water.py` een programma dat de gebruiker vraagt voor de lengte van zijn of haar douche sessie in minuten. Print vervolgens het overeenkomende aantal flesjes water uit. Ga er vanuit dat één minuut douchen overeenkomt met 12 flesjes water (van 0.5L).
* Je mag aannemen dat de gebruiker altijd een positief getal invoert. Je hoeft dus geen fout afhandeling te implementeren mocht de gebruiker dat niet doen.

## Hints

* Maak gebruik van de `input` functie. Deze functie accepteert een argument en print deze uit, vervolgens wacht input tot de gebruiker van jouw programma iets invult en geeft het resultaat daarvan terug. Probeer maar eens `answer = input("Wat is 1 + 2? ")` in de Python terminal.

## Testing
Loop eerst je eigen programma na, werkt deze voor alle legale invoer? Vul bijvoorbeeld eens als aantal douche minuten 0, 10 en 137 in. Lijkt alles te werken, dan is het tijd om checkpy erbij te pakken. Testen gaat net zo als bij `hello`, alleen roep je nu de test voor `water` aan. Zo dus:

```
checkpy.test("water")
```

Mocht je als foutmelding krijgen dat de naam `checkpy` niet bekend is, doe dan eerst even `import checkpy`!


# Mario

## tl;dr
Implementeer een programma dat een halve piramide uitprint van een door de gebruiker gegeven hoogte.

```
Hoe hoog moet de pyramide zijn? 5
    ##
   ###
  ####
 #####
######

Hoe hoog moet de pyramide zijn? 3
  ##
 ###
####
```

## Background
Aan het einde van wereld 1-1 in Super Mario Brothers moet Mario een halve pyramide van blokken beklimmen voordat hij mag springen naar een vlaggenpost. Dit ziet er zo uit:

![](mario.png)

## Specification

* Schrijf in een bestand genaamd `mario.py` een programma dat de halve pyramide van Mario nabouwt door middel van hashes (`#`).
* Vraag eerst aan de gebruiker de hoogte van de halve piramide. Dit mag enkel een geheel positief getal zijn tussen 0 en 23. (0 en 23 wel, -1, 24 en 176 niet)
* Wanneer de gebruiker een foute hoogte invult vraag je de gebruiker opnieuw naar de hoogte. Net zo lang tot de gebruiker een goede hoogte invult.
* Als de hoogte bekend is, genereer dan door middel van `print` en één of meer loops de halve pyramide.
* Let goed op dat er geen spatie tussen de rand van je scherm en de onderste laag van je pyramide staat!

## Hints

* In Python kun je strings vermenigvuldigen door gehele getallen (integers). Probeer maar eens `"Hello" * 3`.
* Tel goed hoe veel spaties en hashes er op elke regel moeten staan.
* Denk goed na over welke loop structuur (`for` en `while`) je wilt gebruiken.
* Deel het probleem op in delen. Zorg bijvoorbeeld eerst dat de gebruiker een getal kan invoeren. Daarna kun je kijken of je kan voorkomen dat de gebruikers foutieve input geeft, en dan de pyramide zelf.
* Kijk ook of de gebruiker geen vreemde waardes invoert als invoer, zoals bijvoorbeeld strings of floats! Je kan kijken of het type van de ingevoerde waarde een integer is door middel van `isinstance`. Probeer bijvoorbeeld maar eens `isinstance(7, int)` en `isinstance("zeven", int)`.

## Testing
Loop weer eerst je eigen programma na. Wat gebeurt er als je 0 voor hoogte invult? Kan je programma alle foute input afhandelen? Ook als de gebruiker als hoogte helemaal geen getal invoert, zoals de string `vijf` bijvoorbeeld? Test dan je programma door middel van checkpy met:

```
checkpy.test("mario")
```


# Greedy

## tl;dr
Implementeer een programma dat het minimaal aantal muntjes uitrekent om wisselgeld te geven. 

```
Hoeveel wisselgeld moet er gegeven worden? 0.41
4
```

## Background

![](coinchange.png)

In een ver verleden toen er nog actief werd betaald door middel van contanten was een muntenhouder als hierboven onmisbaar. Het vervelende was dat er voor elk muntje een levertje moest worden ingedrukt, en dit kostte tijd. Gelukkig zijn wij er al computer scientists om het aantal terug te geven muntjes te minimaliseren door middel van "greedy algoritmes".

Een greedy algoritme is een algoritme dat altijd de beste lokale keuze maakt op weg naar een antwoord. Alsof je fietst en dan op elk kruispunt de afslag kiest waarvan jij op dat moment denkt dat die zo snel mogelijk zal leiden tot je eindbestemming. Dit soort algoritmes leiden voor sommige problemen altijd tot een optimale oplossing, maar niet voor alle problemen.

Stel je voor dat een kassière een klant wisselgeld schuldig staat, en dat deze kassière vervolgens op de levertjes kan drukken om kwartjes (25c), dubbeltjes (10c), stuivers (5c), en centen (1c) te krijgen. Een oplossing voor dit probleem is één of meer drukken op de levertjes, en we willen zo min mogelijk levertjes indrukken. Neem een "gierige" kassière die elke keer als hij op een levertje moet drukken, op het levertje drukt met de hoogst mogelijk waarde welke nog gedrukt mag worden. Bijvoorbeeld als een klant nog 41 cent schuldig staat, dan drukt de kassière eerst op het levertje voor een kwartje. Er blijft dan nog (41 - 25 =) 16 cent over. Nu mag de kassière niet meer drukken op het levertje voor een kwartje, want dan zou hij te veel wisselgeld geven. Dus drukt hij voor een dubbeltje, en daarmee blijft er nog 6 cent over. Dit volgt dan met een druk voor een stuiver, en tot slot een cent. In totaal krijgt de klant dus één kwartje, één dubbeltje, één stuiver, en één cent, dit maakt 4 munten in totaal.

Het blijkt dat deze greedy aanpak altijd een optimale oplossing levert voor dit probleem, met deze munten. Natuurlijk aannnemend dat muntstukken nooit opraken. Hoeveel munten er precies nodig zijn? Dat mag jij ons vertellen!

## Specification

* Schrijf in een bestand genaamd `greedy.py` een programma dat eerst vraagt hoe veel wisselgeld er gegeven moet worden, en vervolgens het minimaal aantal munten uitspuwt.
* Ga er vanuit dat de gebruiker een getal als geheel getal (integer), of als komma getal (float) invult. Het getal achter de komma staat dan voor centen. Dus `3.21` betekent 3 dollar en 21 cent.
* Zorg dat als de gebruiker een float heeft ingevuld, je hiervan een integer maakt. Floating points hebben kleine precisie fouten, en dat wil je niet als je met geld werkt! Je kan door middel van de functie `int` een float converteren naar een integer. Probeer maar eens `int(7.3)` en `int(7.8)`.
* [Slaagt de gebruiker er niet in om correcte input te geven](https://en.wikipedia.org/wiki/Murphy's_law), laat het de gebruiker dan opnieuw proberen.

## Hints

* Vergeet het deel achter de komma niet als je converteert naar een integer!
* Hoe je dit probleem aanpakt is aan jou. Je zou bijvoorbeeld loops kunnen gebruiken of gebruik kunnen maken van de module operator `%`. Probeer maar eens `26 % 8`.

## Testing

```
checkpy.test("greedy")
```