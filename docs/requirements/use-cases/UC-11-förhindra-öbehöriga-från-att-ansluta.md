# Use Case: UC-11 - Förhindra tredje spelare från att ansluta


**Meta**


**Use Case:** Förhindra tredje från att ansluta

**Use case ID:** UC-11

**Primär Aktör:** Spelare

**Syfte:** Förhindrar fler personer än två spelare ansluter till samma parti.



## Förutsättning:

* Ett privat parti har skapats.
* En tredje spelare försöker ansluta länken.
* En eller två spelare kan vara ansluta via länken.


## Trigger:

En tredje spelare försöker trycka på länken för att ansluta.


## Huvudflöde:

1. En spelare försöker ansluta till en partiet.
2. Systemet kontrollerar hur många spelare redan är anslutna.
3. Om två spelare redan är anslutna, nekas anslutningen.
6. Systemet visar ett meddelande t.ex. **"Endast två spelare kan delta."**


## Eftervillkor:

* Partiet innehåller högst två spelare.
* En tredje spelare kan inte ansluta.


## Testbar avslutning:

När två spelare redan anslutna ska en tredje spelares anslutningsförsök misslyckas.
