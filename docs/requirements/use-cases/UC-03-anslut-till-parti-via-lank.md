# Use case ID: UC-03 Anslut till parti via länk

**Meta:**
- Aktör: Spelare (inbjuden/vän)

**Förutsättningar:**
- Spelare (initierare) har bjudit in till ett nytt parti genom att starta nytt parti och skicka delad länk.
- Det finns en delad oanvänd länk till ett startat parti som fortfarande aktiv. 
- Tidsgränsen har inte passerats.

**Trigger:**
- Den inbjudna spelaren klickar på länken för att ansluta till partiet.

**Huvudflöde:**
1. Spelaren klickar på länken.
2. Systemet verifierar att länken är aktiv och att partiet väntar på spelare
3. Systemet ansluter spelaren till partiet.
4. Systemet visar att båda spelarna är anslutna och visar vems tur det är att börja göra ett drag. 

**Alternativa flöden:**
- 

**Postconditions:**
- Båda spelarna (inbjuden och initierare) är anslutna till partiet och kan fortsätta spelet genom att gå in i use case "Spela drag". 

**Testable end condition:**
