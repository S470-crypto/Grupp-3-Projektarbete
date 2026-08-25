# Use Case: UC-11 - Hindra andra för att ansluta


**Meta**


**Use Case:** Hindra andra från ansluta


**Use case ID:** UC-08

**Aktör:** System

**Syfte:** Hindrar personer som inte är behöriga från att gå med i matchen.


**Förutsättning:**
* Ett privat parti har skapats
* En unknown spelare försöker ansluta länken


**Trigger:** Unknown spelare trycka på länken för att ansluta


**Huvudflöde:**
1. En unknown spelare försöker ansluta till en länk.
2. Systemet kontrollerar länken och matchen status
3. Systemet kontrollerar om anslutningen är giltig (xxantal timmar)
4. Om anslutningen är giltig, tillåter systemet personen att anslutna
5. Om anslutningen inte är giltig nekar systemet den personen som vill anslutna
6. Systemet visar meddelande om att personen inte kan anslutna.


**Postconditions:**
* Endast en behörig spelara har tillåtits att ansluta till matchen.
* Obehörig personer kan inte ansluta.


**Testbar avslutning:**
En person som inte har tillgång till spelet eller matchen kan inte ansluta.
