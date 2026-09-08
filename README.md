# Grupp-3-Projektarbete
Gruppmedlemmar: Sami, Mikaela, Honelyn, Andreas

## Om projektet
Detta är ett skolprojekt i kursen krav och användningsfall. 
- Uppgiften gick ut på att genomföra en kravinsamling för ett webbaserat spel (Gomoku - 5 i rad) och skapa användningsfall (use cases) för de krav som identifierades.
- I detta projekt har fokus legat på kravanalysen snarare än själva implementationen av systemet (kod för spelet ingår inte i detta projekt). 
Genom intervju/samtal med en fiktiv kund som saknade kunskap om systemutveckling har vi baserat på kundens beskrivningar fångat upp och formulerat testbara krav samt identifierat aktörer.
- Diagram har skapats och använts för att identifiera tillstånd och aktiviteter, användarresa (user journey) och use case-modeller.

## Kort om systemet

Ett webbaserat Gomoku-spel som ska gå att spela i webbläsaren på datorn eller mobilen utan installation eller kontoregistrering. Spelaren ska kunna spela själv mot datorn (AI) eller spela mot en vän genom att bjuda in till spel via en delad länk till partiet.

## Designval

### Inga spelarkonton

Systemet ska använda länk-ID:n istället för kontoinloggning. Kundens önskemål var att undvika kontoregistrering. Valet bidrar även till att minimera mängden personuppgifter som ska lagras.

### Dataminimering och lagring

Systemet ska följa principen om minimal datalagring. Endast data som krävs för att ett parti ska fungera sparas. Partidata raderas automatiskt efter 24 timmars inaktivitet. Ingen spelarprofil eller spelhistorik lagras.

### Cookie-samtycke och integritet

För att uppfylla kraven i GDPR ska uppgifter om cookie-samtycke sparas separat från speldata och lagras pseudonymiserat.

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
