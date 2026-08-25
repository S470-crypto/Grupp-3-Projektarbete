**Use case: UC-02-Spela drag**

**Meta:**

**Use Case ID:** uc-02

**Namn:** Spela drag

**Primär aktör:** Spelare

**Syfte:** Spelaren vill placera en spelpjäs på brädan


**Förvillkor:**

* Ett parti har startat
* Det är den aktuella spelarens tur
* Partiet är inte pausat eller avslutat




**Huvudflöde:**

1. Systemet visar spelbräet och markerar tydligt att det är spelarens tur.
2. Spelaren väljer en ledig ruta på brädet.
3. Systemet validerar att draget är giltigt.
4. Systemet placerar spelarens pjäs på den valda rutan.
5. Spelet uppdaterar spelbrädet i realtid.
6. Systemet kollar om draget resulterar i vinst , eller oavgjort.
7. Om inget av dessa uppfylls så växlar systemet turen till moståndaren.



**Undantagsflöde:**

* Spelaren väljer en upptagen ruta.
* Spelaren väljer en ruta när det inte är ens tur.
* Anslutningen är instabil och systemet försöker synka dragen igen.




**Testbar avslutning:**

Spelaren lyckas göra ett drag och pjäsen placeras på brädet. 
