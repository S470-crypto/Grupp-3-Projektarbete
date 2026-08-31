# Use case ID: UC-03 Anslut till parti via länk

## Meta:

**Use case:** Anslut till parti via länk

**Use case ID:** UC-03

**Primär aktör:** Motståndare

**Syfte:** Motståndare ska kunna ansluta till parti via delad länk

## Förvillkor:
- Spelare har bjudit in till ett nytt parti genom att starta nytt parti och skicka delad länk.
- Det finns en delad oanvänd länk till ett startat parti som fortfarande aktiv. 
- Tidsgränsen har inte passerats.

## Trigger:
- Den inbjudna motståndaren klickar på länken för att ansluta till partiet.

## Huvudflöde:
1. Motståndaren klickar på länken.
2. Systemet verifierar att länken är aktiv och att partiet väntar på spelare
3. Systemet ansluter motståndaren till partiet.
4. Systemet visar att båda spelarna är anslutna och visar vems tur det är att börja göra ett drag. 

## Alternativa flöden:
**A1:** Länken är ogiltig
1. Tidsgränsen på 5 minuter har passerat utan att motståndaren har anslutit till partiet, länken är inaktiv/ogiltig.
2. Systemet avbryter tillståndet "väntar på spelare" enligt UC-05.

## Eftervillkor:
- Båda spelarna (spelare och motståndare) är anslutna till partiet och kan fortsätta spelet.

## Testbar avslutning:
Det finns en oanvänd giltig länk som spelaren kan klicka på för att ansluta till ett nytt parti. Tillstånd ändras från väntar på spelare till redo för drag, systemet visar att båda spelare är redo för spel.  
