# Use Case ID: UC-10 Visa resultat

## Meta:
**Use case:** Visa resultat

**Use case ID:** UC-10

**Primär aktör:** Spelare och motståndare

**Sekundär aktör:** Dator/AI

## Förvillkor:
- Parti har precis spelats och avgjorts mellan spelare (spelare och motståndare) eller mot dator/AI och kommit fram till ett resultat (någon har fått 5 i rad eller så är brädet fullt och det blev oavgjort).

## Trigger:
- Kontroll görs i systemet om drag resulterat i vinst, förlust eller oavgjort. 

## Huvudflöde:
1. Systemet känner av att kontrollen resulterat i ett slutresultat och avbryter det aktiva spelflödet. 
2. Systemet visar resultatet (vinst för en spelare, förlust för den andra spelaren eller oavgjort för båda) för spelare som deltagit i partiet. 
3. Systemet visar möjlighet att spela igen eller avsluta. 

## Alternativt flöde:

**A1:** ??

## Eftervillkor:
- Partiet är markerat som avslutat
- Resultatet visas tydligt för deltagande spelare.
- Det går inte att göra flera drag i partiet. 

## Testbart avslutning:
När ett parti har avgjorts ska slutresultatet visas tydligt på webbsidan (vinst, förlust eller oavgjort) för de deltagande spelarna. När resultatet visas ska det även vara möjligt att välja att spela igen mot samma spelare eller att avsluta.
