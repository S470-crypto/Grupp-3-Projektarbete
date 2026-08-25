**Use Case: UC-07-Pause och återuppta parti


**Use Case ID:** UC-07

**Namn:** Pausa och återuppta parti

**Primär aktör:** Spelaren

**Syfte:** Spelarne vill tillfälligt kunna pausa ett pågående Gomoku parti för att sedan kunna återuppta den vid ett senare tillfälle efter x antal minuter som längst.

**Förvillkor:** 
* Spelaren har ett aktivt pågpende Gomoku parti.
* Webbsidan är öppen i en webbläsare.


**Trigger:** 
* Spelaren klickar på knappen som pausar spelet under en pågående match.



**Huvudflöde:**

1. Spelaren klickar på knappen för att pausa spelet.
2. Systemet fryser sessionen och förhindrar yttligare drag.
3. Systemet sparar det aktuella spelbrädets status och vems tur det är.
4. Spelare klickar på knappen för att återuppta spelet.
5. Systemet återställer spelbrädet till det senaste sparade läget.
6. Systemet visar spelbrädet och markerar vems tur det är.
7. Partiet är nu redo att fortsätta spelas.


**Undantagsflöde:** 
* Internetanslutningen avbryts medans spelaren är pausad.
* Spelaren stänger ner fliken under pausen.
* Motståndaren lämnar spelet under pausade tillståndet.


**Testbar avslutning:**

* Det pausade Gomoku partiet har återupptagits med exakt samma brädestatus och turordning som när den pausades. 




