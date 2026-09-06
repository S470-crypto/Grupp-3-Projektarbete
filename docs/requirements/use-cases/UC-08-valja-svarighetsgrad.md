# **UC-08 – Välja svårighetsgrad**

## **Meta:**

**Use case:** Välja svårighetsgrad


**Use Case ID:** UC-08


**Primär aktör:** Spelare

**Syfte:**
Spelaren vill kunna välja hur utmanande AI-motståndaren ska vara innan ett parti startas.

## **Förvillkor:**
* Spelaren befinner sig på startsidan eller menyn för att starta ett nytt parti.
* Spelaren har valt AI som motståndare.
* Inget parti har startats ännu.

## Trigger:
* Spelaren väljer alternativet för svårighetsgrad.

## **Huvudflöde:**
1. Systemet visar tillgängliga svårighetsgrader.
2. Spelaren väljer en svårighetsgrad, exempelvis Lätt, Medel eller Svår.
3. Systemet registrerar spelarens val.
4. Systemet visar vilken svårighetsgrad som har valts.
5. Spelaren startar ett nytt parti.
6. Systemet använder den valda svårighetsgraden för AI:ns spelstrategi.

## **Alternativaflöden:**

* Spelaren ändrar val: Spelaren väljer en annan svårighetsgrad innan partiet startas. Systemet uppdaterar valet.

  
  ## **Eftervillkor:**
* En svårighetsgrad är vald och registrerad.
* Den valda svårighetsgraden används av AI:n när partiet startas.

  
## **Testbar avslutning:**
Spelaren har valt en svårighetsgrad och när partiet startas använder AI:n den valda svårighetsgraden.
