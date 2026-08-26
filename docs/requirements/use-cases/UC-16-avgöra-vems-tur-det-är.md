**UC-16 Avgöra vems tur det är**

**Meta**
ID: UC-16

Namn: Avgöra vems tur det är

Aktör: System

Syfte: Systemet ska kunna avgöra vilken spelares tur det är

**Förvillkor**
* En match har startats
* Spelare spelar mot antingen dator(AI) eller en vän och färger är tilldelade

**Huvudflöde**
1. Matchen startar och systemet sätter en spelare som ska gå först.
2. En spelare gör ett giltigt drag.
3. Systemet registrerar draget i speltillståndet.
4. Systemet växlar aktiv spelare till nästa spelare.
5. Systemet visar det nya tur-tillståndet för samtliga spelare.

**Alternativt flöde**
**A1 - Matchen avslutas efter draget**
* Vid steg 3-4: draget resulterar i vinst eller oavgjort
* Systemet ändrar matchstatus till avslutad iställed för att växla spelare

**Testbar avslutning**
* Efter matchstart är aktiv spelare den som ska gå först
* Efter ett giltigt drag från spelare A ska aktiv spelare växlas till spelare B
* Turtillståndet är konsekvent med antalet spelade drag (Ex. Spelare A gör udda drag och spelare B gör jämna drag)


