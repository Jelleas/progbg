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
* Implementeer `grafiek`