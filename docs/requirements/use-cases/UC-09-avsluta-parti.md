# **Use Case:** UC-09-Avsluta parti


## **Meta:** 
**Use Case ID:** UC-09


**Namn:** Avsluta parti


**Primär aktör:** Systemet


**Syfte:** Systemet identifierar automatiskt när ett parti är slut och avgör vinnare, systemet utgår itfrån vinst eller oavgjort (full bräda)


## **Förvillkor:**
* Ett aktvit Gomoku parti pågår.
* En spelare har just placerat en giltig bricka på brädet.




## **Trigger:**
En spelare placerar en bricka.



## **Huvudflöde:**
1. Spelaren placerar en bricka på brädet.
2. Systemet kontrollerar brädet för att se om 5 i riad har uppnåtts (horisontellt, diagonalt eller ertikalt)
3. Systemet identifierar att en spelare har fått 5 i rad.
4. Systemet låser spelbrädet för yttligare drag.
5. Systemet markerar den vinnande linjen på brädet.
6. Systemet visar en slutskärm som visar vem som har vunnit.



## **Alternativaflöden:**

* Systemet konstaterar att ingen spelare har fått 5 i rad och att alla rutor är fyllda. Systemet markerar partiet som oavgjort, låser brädet och visar en slutskärm med resultatet.



## **Eftervillkor:**
* Partiets status är satt till avslutat vid vinst eller oavgjort.
* Vid vinst är vinnaren identifierad och resultatet visas för spelarna.
* 



## **Testbar avslutning:**

* Partiet är avslutat, brädet är låst och vinnare presenteras om inte avslutningen skedde via oavgjort resultat (fullt spelbräde.)



