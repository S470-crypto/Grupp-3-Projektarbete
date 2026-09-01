# Use Case-ID: UC-04 Spela igen mot samma motståndare

## Meta:

**Use case:** Spela igen mot samma motståndare

**Use case ID:** UC-04

**Primär aktör:** Spelare och motståndare

**Syfte:** Kunna spela igen direkt efter ett parti mot samma motståndare utan att behöva börja om och skicka ny inbjudan/länk

## Förvillkor:
- Ett parti mellan spelarna har avslutats och resulterat i vinst, förlust eller oavgjort. 
- Både spelarna är fortfarande anslutna.  

## Trigger:
- En av spelarna väljer att spela igen från resultatvyn. 

## Huvudflöde:
1. Systemet visar resultatet från avslutat parti och erbjuder möjligheten att spela igen eller avsluta.
2. Spelaren väljer att "spela igen". 
3. Systemet skapar ett nytt parti mellan samma spelare och motståndare. 
4. Ingen ny länkdelning eller annan process för att kunna ansluta krävs.
5. Systemet visar automatiskt vilken spelare som ska börja och väntar på att ett drag ska ske.

## Alternativa flöden:

**A1:** Motståndaren har lämnat spelet
1. Motståndaren har lämnat spelsidan och är inte längre tillgänglig för spel.
2. Felmeddelande visas för spelaren med information om att motståndaren inte är aktiv.
3. Det går inte att välja "spela igen" i samma spelsession, ny inbjudan behöver skickas med länk till nytt parti.

## Eftervillkor:
- Ett nytt parti har skapats mellan de två spelarna. 

## Testbar avslutning:
Ett parti som nyligen avslutats mellan två spelare där en av spelarna väljer att spela igen mot samma spelare. Då startar ett nytt parti mellan samma spelare utan att en ny länk behöver delas till det nya partiet. 
