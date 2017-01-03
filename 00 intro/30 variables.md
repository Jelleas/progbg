# Variables

Tot nu toe zijn we enkel bezig geweest met constantes. Om resultaten van berekeningen te kunnen gebruiken in andere berekeningen, hebben we iets nodig om deze op te slaan. Als oplossing laat Python je namen toekennen aan waardes. Deze naam-waarde combinaties noemen we *variables*. Door middel van de `=` operator kunnen we een naam toekennen aan een waarde, en deze vervolgens ergens anders gebruiken. Zie bijvoorbeeld hieronder:

```
income = 230
expense = 170
profit = income - expense
print profit
```

Het is hierbij belangrijk om te letten op de volgorde van de regels code. Python interpreteert jouw code van boven naar beneden. Zou je de laatste regel als eerste neerzetten, dan krijg je een `NameError`. Want de naam `profit` is nog niet bekend (*defined*), want die wordt pas bekend gemaakt op regel 3.

Continu nieuwe namen introduceren voor elke berekening is soms niet wat je wilt. In Python kan je ook oude, al gebruikte namen toekennen aan nieuwe waardes. Bijvoorbeeld:

```
income = 170
income = income - 10
income -= 30
print income
```

Hier is de `-=` operator puur een verkorting voor `a = a - ...`.