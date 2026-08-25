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

* Spelaren klickar på knappen för att pausa spelet.
* Systemet fryser sessionen och förhindrar yttligare drag.
* Systemet sparar det aktuella spelbrädets status och vems tur det är.
* Spelare klickar på knappen för att återuppta spelet.
* Systemet återställer spelbrädet till det senaste sparade läget.
* Systemet visar spelbrädet och markerar vems tur det är.
* Partiet är nu redo att fortsätta spelas.


**Undantagsflöde:** 
* Internetanslutningen avbryts medans spelaren är pausad.
* Spelaren stänger ner fliken under pausen.
* Motståndaren lämnar spelet under pausade tillståndet.


**Testbar avslutning:**

* Det pausade Gomoku partiet har återupptagits med exakt samma brädestatus och turordning som när den pausades. 




