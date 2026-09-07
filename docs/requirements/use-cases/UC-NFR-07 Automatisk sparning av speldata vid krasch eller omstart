
#Use case: UC-NFR-07 Automatisk sparning av speldata vid krasch eller omstart 


##Meta 
Use case: Automatisk sparning av speldata vid krasch eller omstart

Use case ID: UC-NFR-06

Primär aktör: System

Sekundär aktör: Spelare (mottagare av återställd data)

Syfte: Säkerställa att pågående speldata bevaras kontinuerligt så att ett parti kan återställas om webbläsaren kraschar eller sidan laddas om oavsiktligt (NFR-01.1).

##Förvillkor: 
Ett parti pågår (status: pågående eller pausad)
Autosave-funktionen är aktiv och tillgänglig
Trigger: 
Ett drag görs, partiet pausas, eller partiets tillstånd förändras på annat sätt under ett pågående parti.

##Huvudflöde: 
Ett drag görs eller partiets tillstånd förändras på annat sätt (t.ex. paus)
Systemet sparar automatiskt det aktuella spelbrädets tillstånd, tur-status och partiets metadata (session-/länk-ID)
Spelaren fortsätter spela som vanligt utan att märka av sparandet
Om webbläsaren kraschar eller sidan laddas om oavsiktligt, upptäcker systemet vid nästa sidladdning att en session med sparad, oavslutad data finns
Systemet återställer partiet till senast sparade tillstånd automatiskt
Spelaren kan fortsätta partiet exakt där det avbröts


##Alternativa flöden: 
A1: Ingen sparad data hittas (t.ex. vid ett nytt besök)

Systemet visar startsidan som vanligt, ingen återställning sker.
A2: Sparandet misslyckas tekniskt (t.ex. lagringsfel)

Systemet fortsätter spelet i minnet men flaggar internt att autosave misslyckats.
Om en krasch sker innan nästa lyckade sparning går den senaste, osparade förändringen förlorad.
A3: Sparad data är korrupt eller ofullständig vid återställningsförsök

Systemet kan inte återställa partiet tillförlitligt.
Spelaren informeras (se UC-12, Visa felmeddelande) och erbjuds att starta ett nytt parti.


##Eftervillkor: 
Partiets senaste tillstånd är alltid sparat inom en kort, definierad tidsram efter varje förändring
Vid oavsiktligt avbrott kan partiet återställas till senast sparade tillstånd

##Testbar avslutning: 
T1: Efter varje giltigt drag är det nya brädtillståndet sparat inom en definierad tidsgräns.
T2: Vid simulerad krasch (t.ex. stängd flik) och återöppning återställs partiet till exakt det tillstånd det hade precis innan kraschen.
T3: Om ingen sparad data finns visas startsidan normalt utan felaktig återställning.
T4: Om sparandet misslyckas tekniskt loggas detta internt utan att synligt krascha spelarens upplevelse.
