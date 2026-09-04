# UC-NFR-01-genomsnittlig-svarstid-under-spelgång-under-0.33-sekunder-på-1000-cypresstester


## Meta
**Use case:** Genomsittlig svarstid under spel gång på under 0.33 sekunder på 1000 cypresstester.

**Use case ID:** UC-NFR-01

**Primär aktor:** Admin

**Syfte:** Uppnå en genomsnittlig svarstid på under 0.33 sekunder under spelets gång. 

## Förvillkor
* Spelet kan startas och köras normalt.
* Testmiljön är tillgänglig och fungerar korrekt.
* Mätningen av systemets svarstid är aktiverad.

* ## Trigger
* Testsystemet startar en serie på 1000 stresstester under pågående spel.

## Huvudflöde
1. Testsystemet startar spelet.
2. Testsystemet initierar mätning av svarstid.
3. Testsystemet genomfös under pågående spel.
4. Systemets svarstid reistreras.
5. Steg 3 och 4 upprepas 1000 gånger.

## Alternativa flöden
* Om genomsnittliga svarstiden är 0.33 sekunder eller högre så markeras testet som underkänt.
* Systemet kraschar eller slutar svara.


 ## Eftervillkor
  * 1000 Stresstester har genomförts.
  * Den genomsnittliga svarstiden har beräknats.
  * Resultatet har dokumenterats.


## Testbar avslutning
* Den uppmätta genomsnittliga svarstiden under 1000 genomförda stresstester är mindre än 0.33 sekunder. 
