# **Use case: UC-06-Spela drag**

## **Meta:**


**Namn:** Spela drag


**Use Case ID:** UC-06



**Primär aktör:** Spelare

 **Syfte:** Spelaren vill göra ett drag genom att placera en bricka på spelbrädet


## **Förvillkor:**

* Ett parti har startat
* Det är den aktuella spelarens tur
* Partiet är inte pausat eller avslutat

## **Trigger**
Det är spelarens tur att placera en bricka på spelbrädet.


## **Huvudflöde:**

1. Systemet visar spelbrädet och markerar tydligt att det är spelarens tur.
2. Spelaren väljer en ledig spelruta på brädet.
3. Systemet validerar att draget är giltigt.
4. Systemet placerar spelarens bricka på den valda spelrutan.
5. Spelet uppdaterar spelbrädet i realtid.
6. Systemet kollar om draget resulterar i vinst eller oavgjort.
7. Om inget av dessa uppfylls så växlar systemet turen till moståndaren.



## **Alternativaflöden:**

* Spelaren väljer en upptagen spelruta.
* Spelaren väljer en spelruta när det inte är ens tur.
* Anslutningen är instabil och systemet försöker synka dragen igen.

## **Eftervillkor:**

* Spelarens bricka är placerad på vald spelruta.
* Om draget inte leder till vinst eller oavgjort så blir det motståndarens tur.



## **Testbar avslutning:**

Spelaren lyckas göra ett drag och brickan placeras på spelbrädet. 




