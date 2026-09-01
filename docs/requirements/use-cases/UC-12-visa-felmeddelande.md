
# Use Case: UC-12 - Visa felmeddelande


## **Meta**


**Use case:** Visa felmeddelande

**Use case ID:** UC-12

**Primär aktör:** System

**Syfte:** Att informera spelaren när något går fel om spelet.


## Förutsättningar:

Ett fel har uppstått i spelet när något fel i spelet eller spelare gjort nånting fel.

## Trigger:

Systemet visar felmeddelande tex: **"Ogiltigt drag. Den valda rutan är redan upptagen. Välj en ledig ruta."**


## Huvudflöde:

1. Ett fel uppstår i systemet.
2. Systemet identifierar felet tex: **"Ogiltig drag."**.
3. Systemet visar tydligt felmeddelande information tex: **"Den valda rutan är redan upptagen."**
4. Systemet informerar spelaren om vad som kan göras tex: **"Välj en annan ruta."**
5. Spelaren försöka utföra vad systemet föreslå eller vad står på felmeddelande.
6. Systemet lösa problemet.
7. Spelaren försätta använda spelet.


## Eftervillkor:

* Ett fel meddelande med en tydligt information har visats för spelaren.


## Alternativaflöden:

**Felet kan inte lösas direkt**

* Ett fel uppstår i spelet.
* Systemet försöker hantera felet.
* Felet går inte att lösa automatiskt.
* Systemet visar ett tydligt felmeddelande **"Något gick fel. Försök igen."**
* Spelaren föröka igen eller hen lämna spelet.


## Testbar avslutning:

Ett tydligt felmeddelande visas när något går fel.
