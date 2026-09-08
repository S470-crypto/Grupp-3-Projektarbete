[Tillbaka till README](../../../README.md)
# UC-NFR-08 Uppdatera systemet utan att pågående partier går förlorade 


## Meta 

**Use case:** Uppdatera systemet utan att pågående partier går förlorade

**Use case ID:** UC-NFR-08

**Primär aktör:** Administratör

**Sekundär aktör**: Spelare (påverkas indirekt), System

**Syfte:** Säkerställa att driftuppdateringar (t.ex. ny kodversion) kan genomföras utan att spelare förlorar sina pågående partier.

## Förvillkor: 
* En ny systemversion är redo att distribueras
* Pågående partier finns i systemet vid uppdateringstillfället
* Systemet stödjer en uppdateringsstrategi som bevarar tillstånd i servern.

## Trigger: 
Administratören initierar en driftsättning av en ny systemversion.

## Huvudflöde: 
1. Administratören initierar uppdateringen
2. Systemet säkerställer att alla pågående partiers tillstånd är sparat i en beständig lagring, separat från applikationsinstansen som ska uppdateras
3. Den nya versionen driftsätts, t.ex. genom att nya instanser startas parallellt med de gamla
4. Trafik och pågående sessioner flyttas gradvis över till den nya versionen
5. Spelare med pågående partier fortsätter sina partier på den nya versionen med bevarat tillstånd
6. De gamla instanserna avvecklas när inga sessioner längre använder dem


## Alternativa flöden: 

**A1: Ett pågående partis tillstånd kan inte överföras korrekt till den nya versionen (t.ex. p.g.a. en inkompatibel dataformatändring)**

- Systemet informerar berörd spelare om att partiet inte kunde återupptas, som ett undantag snarare än normalfallet.


**A2: Uppdateringen måste avbrytas mitt i processen**

- Systemet återgår till den tidigare versionen (rollback) utan att pågående partier påverkas, eftersom tillståndet aldrig var beroende av en specifik applikationsinstans.

## Eftervillkor: 
Den nya systemversionen är i drift.
Samtliga partier som pågick innan uppdateringen är fortsatt spelbara med bevarat tillstånd (spelbräde, tur, historik).

## Testbar avslutning: 

- Ett parti som pågår vid uppdateringstillfället kan fortsätta spelas utan avbrott eller dataförlust efter att uppdateringen slutförts.

- Spelbrädets tillstånd, tur-status och historik är identiska före och efter uppdateringen för ett pågående parti.

- Vid en avbruten uppdatering (rollback) påverkas inga pågående partier.

- Spelaren märker ingen eller minimal avbrottstid under uppdateringen (en acceptabel nedtid bör fastställas tillsammans med kunden).
