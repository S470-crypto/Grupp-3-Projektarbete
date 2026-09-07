[Tillbaka till README](../../../README.md)
# UC-NFR-06 Automatisk rensning av partidata

## Meta:

**Use case:** Automatisk rensning av partidata

**Use case ID:** UC-NFR-06

**Primär aktör:** Systemet

**Syfte:** Säkerställa att parti-/speldata inte lagras längre än nödvändigt och att inaktiva spelpartier inte ligger kvar för länge i systemet.

## Förvillkor:

- Partidata/speldata finns lagrad på servern kopplad till ett länk-ID

- Ingen aktivitet har registrerats i partiet på mer än 24 timmar

## Trigger:

- Systemet känner av att 24 timmar har passerat sedan den senaste aktiviteten registrerades i partiet

## Huvudflöde:

1. Systemet identifierar spelpartier där senaste aktiviteten genomfördes för mer än 24 timmar sedan.

2. Systemet markerar partierna som ska rensas/raderas med "rensning".

3. Systemet raderar allt lagrat tillstånd kopplat till länk-ID:t (spelbräde, brickor, turordning, status).

4. Länk-ID:t blir ogiltigt, om spelare klickar på länken visas felmeddelande som informerar om att spelet har avslutats pga inaktivitet.

5. Åtgärden registreras i driftloggen.

## Alternativa flöden:

**A1: En spelare återvänder innan tidsgränsen passerats**

1. Systemet registrerar aktivitet i partiet.

2. Systemets räknare kopplat till inaktivitet nollställs och nedräkning börjar om.

**A2: En driftuppdatering genomförs under inaktivitetsperioden**

1. Partiets tillstånd bevaras genom uppdateringen.

2. Systemets räknare kopplat till inaktivitet påverkas inte av uppdateringen. 24-timmarsgränsen räknas från spelarnas senaste aktivitet och påverkas inte av uppdateringen.

**A3: Det uppstår ett tekniskt fel vid rensningen**

1. Systemet har misslyckats med rensningen.

2. Systemet loggar felet.

3. Admin kontrollerar loggen och genomför rensning/radering manuellt (eftersom utebliven radering innebär att lagringsminimeringen inte efterlevs).

**Eftervillkor:**

- Ingen partidata kopplad till länk-ID:t finns kvar på servern

- Åtgärden (att rensning/radering genomförts) har loggats för att kunna styrka efterlevnad

**Testbar avslutning:**

Givet att det finns ett parti utan registrerad aktivitet där 24 timmar har passerat sedan senaste aktivitet då finns ingen partidata kvar kopplad till länk-ID:t och ett försök att öppna länken leder inte till något pågående spelparti.
