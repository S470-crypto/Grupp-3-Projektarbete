## **UC-03 – Välja svårighetsgrad**

## **Meta:**

**Namn: Välja svårighetsgrad**


**Use Case ID: UC-03**


**Primär aktör: Spelare**

**Syfte:**
Spelaren vill kunna välja hur utmanande AI-motståndaren ska vara innan ett parti startas.

## **Förvillkor:**
* Spelaren befinner sig på startsidan eller menyn för att starta ett nytt parti.
* Spelaren har valt AI som motståndare.
* Inget parti har startats ännu.
* Trigger
* Spelaren väljer alternativet för svårighetsgrad.

## **Huvudflöde:**
* Systemet visar tillgängliga svårighetsgrader.
* Spelaren väljer en svårighetsgrad, exempelvis Lätt, Medel eller Svår.
* Systemet registrerar spelarens val.
* Systemet visar vilken svårighetsgrad som har valts.
* Spelaren startar ett nytt parti.
* Systemet använder den valda svårighetsgraden för AI:ns spelstrategi.

## **Alternativaflöden:**

* Spelaren ändrar val: Spelaren väljer en annan svårighetsgrad innan partiet startas. Systemet uppdaterar valet.

  
  ## **Eftervillkor:**
* En svårighetsgrad är vald och registrerad.
* Den valda svårighetsgraden används av AI:n när partiet startas.

  
## **Testbar avslutning:**
Spelaren har valt en svårighetsgrad och när partiet startas använder AI:n den valda svårighetsgraden.
