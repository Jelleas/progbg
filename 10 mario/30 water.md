# Water

## tl;dr

Implementeer een programma dat een gebruiker zijn waterverbruik reporteert, door het aantal minuten douchen te converteren naar flesjes drinkwater.

```
Hoeveel minuten douche je? 1
12

Hoeveel minuten douche je? 10
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