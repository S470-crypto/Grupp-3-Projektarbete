# Grupp-3-Projektarbete
Gruppmedlemmar: Sami, Mikaela, Honelyn, Andreas

## Om projektet
Detta är ett skolprojekt i kursen krav och användningsfall. 
- Uppgiften gick ut på att vi skulle genomföra en kravinsamling för ett webbaserat spel (Gomoku - 5 i rad) och skapa användningsfall (use cases) för de krav som identifierades.
- I detta projekt fokus legat på kravanalysen snarare än själva implementationen av systemet (kod för spelet ingår inte i detta projekt). 
Genom intervju/samtal med en fiktiv kund som saknade kunskap om systemutveckling har vi fångat upp testbara krav och aktörer baserat på kundens beskrivningar.
- Diagram har använts för att identifiera tillstånd och aktiviteter, user journey och use case modell.

## Kort om systemet
- Ett webbaserat Gomoku-spel som kan spelas i webbläsaren på datorn eller mobilen utan installation eller kontoregistrering. Spelaren ska kunna spela själv mot en dator (AI)-motståndare eller spela mot en vän som motståndare genom att bjuda in till spel via en delad länk till partiet.

### Centrala designval

**Inga spelarkonton**
Systemet använder länk-ID:n istället för kontoinloggning för att:
- Minimera mängden personuppgifter.
- Förenkla GDPR-hantering.
- Undvika kontoregistrering och långsiktig datalagring.

**Dataminimering och lagring**
Systemet följer principen om minimal datalagring:
- Endast data som krävs för att ett parti ska fungera sparas.
- Partidata raderas automatiskt efter 24 timmars inaktivitet.
- Ingen användarprofil eller historik lagras.

**Cookie-samtycke och integritet**
Cookie-samtycke hanteras separat från speldata och lagras pseudonymiserat. Detta möjliggör dataminimering även utan spelarkonton och säkerställer att samtycke inte kan kopplas till en specifik spelare.

## Innehåll

|   Dokument    | Innehåll    |
|-------------|-------------|
|   [00-Ordlista](docs/requirements/00-ordlista.md) | Beskriver de centrala begrepp som används     |
|   [01-Inledning](docs/requirements/01-inledning.md) | Kortfattad beskrivning av systemet och syfte   |
|   [02-Funktionella krav](docs/requirements/02-funktionella-krav.md) | Vad systemet måste göra   |
|   [03-Kompletterande krav](docs/requirements/03-kompletterande-krav.md) | Antaganden och begränsningar  |
|   [04-Icke funktionella krav](docs/requirements/04-icke-funktionella-krav.md) | Hur systemet ska fungera och kvalitetsegenskaper|
|   [05-Begreppsmodell](docs/requirements/05-begreppsmodell.md)| Visuell karta över centrala begrepp och hur de hänger samman|
|   [06-User journey](docs/requirements/06-user-journey.md) | Diagram över användarresa |
|   [07-Use cases overview](docs/requirements/07-use-cases-overview.md) | Översikt över use cases och diagram|
|   [08-Diagram](docs/requirements/08-diagram.md) | Tillståndsdiagram och aktivitetsdiagram|
|   [09-Verksamhetsregler](docs/requirements/09-verksamhetsregler.md) | Beskriver spelets regler |
|   [10-Spårbarhetsmatris](docs/requirements/10-sparbarhetsmatris.md)| Tabeller visar översikt av krav kopplat till use cases|
|   [Use cases](docs/requirements/use-cases)| Genväg till use cases|
