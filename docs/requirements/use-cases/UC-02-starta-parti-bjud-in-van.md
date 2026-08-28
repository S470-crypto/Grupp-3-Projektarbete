# Use Case: UC-02 Starta parti bjud in vän

## Meta:
**Use case:** Starta parti bjud in vän

**Use case ID:** UC-02

**Primära aktörer:** Spelare och motståndare (inbjuden/vän)

## Förvillkor:
- Att spelaren är inne på spelets hemsida. 

## Trigger:
- Spelaren väljer att spela mot annan motståndare som är en annan spelare/vän och skicka inbjudan via delad länk

## Huvudflöde:
1. Spelaren väljer att starta ett nytt parti och "Spela mot vän" på startsidan.
2. Systemet startar ett nytt parti med spelare och motståndare. 
3. Systemet skapar en delad länk med länk-ID till partiet som kan delas till motståndaren utanför systemet via valfri kanal t.ex. via mail eller chatt. 
4. Systemet väntar på att motståndare ska ansluta.
5. Motståndaren ansluter till partiet via länken. 
6. Systemet visar att båda spelare är redo och visar en tom spelplan samt anger vems tur det är att göra ett drag.
7. Systemet väntar på att spelare ska göra ett drag, use case Spela drag tar vid. 

## Alternativa flöden:
**A1:**
- Ingen ansluter inom tidsgränsen
- Tidsgräns på 5 min, sedan blir länken inaktiv, se use case "Avbryt i väntan på timeout"

## Eftervillkor:
- Parti skapats med unikt länk-ID.
- Systemet i väntande läge på Spela drag.

## Testbar avslutning:
Ett nytt parti av Gomoku har skapats mellan två spelare och väntar på nästa drag.
