# Use Case: UC-02 Starta parti bjud in vän

**Meta:**
- Aktör: Spelare (initierare) och spelare (inbjuden/vän) som motståndare
- Relaterade use cases: Spela drag

**Förutsättningar:**
- Att spelaren är inne på spelets hemsida. 

**Trigger:**
- Spelaren väljer att spela mot annan spelare/vän och skicka inbjudan via delad länk

**Huvudflöde:**
1. Spelaren väljer att starta ett nytt parti och "Spela mot vän" på startsidan.
2. Systemet startar ett nytt parti med spelare (initierare) och spelare (inbjuden/vän) som motståndare. 
3. Systemet skapar en delad länk med länk-ID till partiet som kan delas till motståndaren utanför systemet via valfri kanal t.ex. via mail eller chatt. 
4. Systemet väntar på att spelare ska ansluta.
5. Motståndaren ansluter till partiet via länken. 
6. Systemet visar att båda spelare är redo och visar en tom spelplan samt anger vems tur det är att göra ett drag.
7. Systemet väntar på att spelare ska göra ett drag, use case Spela drag tar vid. 

**Alternativa flöden:**
A1 - Ingen ansluter inom tidsgränsen
- Tidsgräns på X min, sedan blir länken inaktiv.
- Use case "Avbryt i väntan på timeout"

**Postconditions:**
- Parti skapats med unikt länk-ID.
- Systemet i väntande läge på Spela drag.

**Testable end condition:**
- Ett nytt parti av Gomoku har skapats mellan två spelare och väntar på nästa drag.
