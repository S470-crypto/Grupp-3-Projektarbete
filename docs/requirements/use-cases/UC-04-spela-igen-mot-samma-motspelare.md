# Use Case-ID: UC-04 Spela igen mot samma motspelare

**Meta:**
- Aktör: Spelare (både initierare och inbjuden vän/motspelare)

**Förutsättningar:**
- Ett parti mellan spelarna har avslutats och resulterat i vinst, förlust eller oavgjort. 
- Båda spelarna är fortfarande anslutna.  

**Trigger:**
- En av spelarna väljer att spela igen från resultatvyn. 

**Huvudflöde:**
1. Systemet visar resultatet från avslutat parti och erbjuder möjligheten att spela igen eller avsluta.
2. Spelaren väljer att spela igen. 
3. Systemet skapar ett nytt parti mellan samma spelare. 
4. Ingen ny länkdelning eller annan process för att kunna ansluta krävs.
5. Systemet visar automatiskt vilken spelare som ska börja och väntar på att ett drag ska ske.

**Alternativa flöden:**
- Motståndaren har lämnat sidan vilket innebär att spelaren inte kan starta nytt parti mot den motståndaren. 

**Eftervillkor:**
- Ett nytt parti har skapats mellan de två spelarna. 

**Testbart slutvillkor:**
- Ett parti som nyligen avslutats mellan två spelare där en av spelarna väljer att spela igen mot samma spelare. Då startar ett nytt parti mellan samma spelare utan att en ny länk behöver delas till det nya partiet. 
