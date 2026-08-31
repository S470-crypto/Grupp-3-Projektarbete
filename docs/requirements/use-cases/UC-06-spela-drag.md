# **Use case: UC-06-Spela drag**

## **Meta:**


**Namn:** Spela drag


**Use Case ID:** UC-06



**Primär aktör:** Spelare

## **Syfte:** Spelaren vill placera en spelpjäs på brädan


## **Förvillkor:**

* Ett parti har startat
* Det är den aktuella spelarens tur
* Partiet är inte pausat eller avslutat

## **Trigger**
Det är spelarens tur att placera en bricka på brädet.


## **Huvudflöde:**

1. Systemet visar spelbräet och markerar tydligt att det är spelarens tur.
2. Spelaren väljer en ledig ruta på brädet.
3. Systemet validerar att draget är giltigt.
4. Systemet placerar spelarens pjäs på den valda rutan.
5. Spelet uppdaterar spelbrädet i realtid.
6. Systemet kollar om draget resulterar i vinst , eller oavgjort.
7. Om inget av dessa uppfylls så växlar systemet turen till moståndaren.



## **Alternativaflöden:**

* Spelaren väljer en upptagen ruta.
* Spelaren väljer en ruta när det inte är ens tur.
* Anslutningen är instabil och systemet försöker synka dragen igen.

## **Eftervillkor:**

* Spelarens bricka är placerad på vald spelruta.
* Om draget inte leder till vinst eller oavgjort så blir det motståndarens tur.



## **Testbar avslutning:**

Spelaren lyckas göra ett drag och pjäsen placeras på brädet. 




