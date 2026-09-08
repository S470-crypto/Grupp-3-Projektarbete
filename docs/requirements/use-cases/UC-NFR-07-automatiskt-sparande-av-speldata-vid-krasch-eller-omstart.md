[Tillbaka till README](../../../README.md)
# UC-NFR-07 Spel-skall-kunna-återskapas-efter-krasch


## Meta 

**Use case:** Spel skall kunna återskapas efter krasch

**Use case ID:** UC-NFR-07

**Primär aktör:** System

**Sekundär aktör:** Spelare (mottagare av återställd data)

**Syfte:** Säkerställa att pågående speldata sparas kontinuerligt så att ett parti kan återställas om webbläsaren kraschar eller sidan laddas om.

## Förvillkor: 

- Ett parti pågår (status: pågående eller pausad) och spelare har gett samtycke till cookies.


## Trigger: 

- Ett drag görs, partiet pausas, eller partiets tillstånd förändras på annat sätt under ett pågående parti.

## Huvudflöde: 
1. Ett drag görs eller partiets tillstånd förändras på annat sätt (t.ex. paus)
2. Systemet sparar automatiskt det aktuella spelbrädets tillstånd, tur-status och partiets metadata (länk-ID) på servern. Länk-ID lagras i spelarens webbläsare via sessionscookie.
3. Spelaren fortsätter spela som vanligt utan att märka av sparandet
4. Om webbläsaren kraschar eller sidan laddas om oavsiktligt, upptäcker systemet vid nästa sidladdning att en session med sparad, oavslutad data finns
5. Systemet återställer partiet till senast sparade tillstånd automatiskt
6. Spelaren kan fortsätta partiet exakt där det avbröts


## Alternativa flöden: 
**A1: Ingen sparad data hittas (t.ex. vid nekat samtycke till cookies)**

- Systemet visar startsidan som vanligt, ingen återställning sker. 

**A2: Sparad data är korrupt eller ofullständig vid återställningsförsök**

 - Systemet kan inte återställa partiet tillförlitligt.
 - Spelaren informeras via ett felmeddelande och erbjuds att starta ett nytt parti.
 - Om systemet misslyckats med att spara speldata så registreras det i loggen (hanteras av admin).

**A3: Automatisk rensning har skett (efter 24 timmar)**

- Om spelaren försöker återuppta partiet efter mer än 24 timmar har rensning skett och speldata kopplad till länk-ID har raderats. 

## Eftervillkor: 

- Partiets senaste tillstånd är sparat efter varje förändring.
- Vid oavsiktligt avbrott kan partiet återställas till senast sparade tillstånd.

## Testbar avslutning: 

- Efter varje giltigt drag är spelbrädets nya tillstånd sparat.
   
- Vid simulerad krasch (t.ex. stängd flik) och återöppning återställs partiet till exakt det tillstånd det hade precis innan kraschen.
  
- Om ingen sparad data finns visas startsidan normalt utan felaktig återställning.
  
- Om sparande misslyckats så registreras det i loggen (hanteras av admin).
