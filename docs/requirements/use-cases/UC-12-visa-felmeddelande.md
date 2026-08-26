
# Use Case: UC-12 - Visa felmeddelande


**Meta**


**Use case:** Visa felmeddelande

**Use case ID:** UC-12

**Primär aktör:** System

**Syfte:** Att informera spelaren nar något går fel.


## Förutsättningar:

Ett fel har uppstått i spelet när något fel i spelet eller spelare gjort nånting fel.

## Trigger:

Systemet visar "Felmeddelande" is spelet.


## Huvudflöde:

1. Ett fel uppstår i systemet.
2. Systemet identifierar felet.
3. Systemet visar tydligt felmeddelande information
4. Systemet informerar spelaren om vad som kan göras
5. Spelaren försöka utföra vad systemet föreslå eller vad står på felmeddelande
6. Systemet lösa problemet
7. Spelaren försätta använda spelet


## Postcondition:

* Ett fel meddelande med en tydligt information har visats för spelaren.


## Testbar avslutning:

Ett tydligt felmeddelande visas när något går fel.
