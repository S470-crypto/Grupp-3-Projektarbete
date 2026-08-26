## USE CASE: UC-14 Spara spelet


**Meta**

**Use case:** Spara spelet

**Use case ID:** UC-14

**Primär aktör:** System

**Syfte:** Spara pågående spelets så att spelaaren kan försätta senare och se historisk.


## Förutsättning:

Ett spel har startats och det finns spelinformation som kan sparas.

## Trigger:

Spelaren väljer **Spara spel** eller avslutar ett spel som ska sparas.


## Huvudflöde:

1. Spelaren väljer **Spara spel**. 
2. Systemet sparar spelets information. 
3. Systemet sparar spelplanen och resultatet om matchen är avslutad. 
4. Systemet visar att spelet har sparats. 
5. Spelaren kan senare öppna det sparade spelet. 
6. Om spelet inte är avslutat kan spelaren fortsätta spela. 
7. Om spelet är avslutat kan spelaren se resultatet.


## Postcondition

* Spelet är sparat och kan öppnas igen senare för att fortsätta eller se resultatet.

## Testbar avslutning

* Spelaren kan öppna ett sparat spel och se samma spelinformation som när spelet sparades.

