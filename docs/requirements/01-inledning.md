# 1. Inledning

## 1.1 Om spelet
Gomoku är ett spel som spelas i webbläsaren på datorn eller telefonen. Spelaren kan spela i realtid mot Datorn (AI) eller mot en vän via en delad länk. Ingen installation krävs för att spela spelet. 

## 1.2 Syfte
Det ska vara enkelt för spelaren att komma igång och starta ett spel/parti mot en motståndare (dator eller vän) och att genomföra det tills dess att något av tre slutresultat nåtts: vinst, förlust eller oavgjort.

## 1.3 Problem som ska lösas
Kunden vill kunna spela Gomoku själv mot datorn eller mot en vän genom att skicka en länk. Spelet ska gå att spela på datorn eller i telefonen. Ingen nedladdning, inget konto eller inloggning ska krävas för att kunna spela spelet.  

## 1.4 Aktörer

| Aktör | Typ | Beskrivning |
|-------|------|-------------|
| Spelare | Primär aktör (Mänsklig) | Personen som använder systemet för att spela. Hen kan starta parti/spelet, bjuda in till spel, spela mot motståndare (vän) eller Dator (AI). |
| Dator (AI) | Sekundär systemaktör | Agerar som motståndare och spelar mot spelaren i systemet när hen väljer att spela mot dator (AI), beräknar och gör automatiska drag baserat på spelets regler. |
| Motståndare | Primär aktör (Mänsklig) | Personen som till exempel en vän som spelar mot spelaren. |
| Administratör (Systemadmin) | Primär/sekundär aktör (Mänsklig) | Administratör som hanterar behörigheter för användare, drift, tekniska fel och övervakar systemet. |
| Dataansvarig | Primär/sekundär aktör (Mänsklig)| Säkerställer att GDPR följs, ansvarar för radering och eventuella personuppgiftsincidenter. |
| Systemet | Sekundär systemaktör | Validerar drag och raderar inaktiva spelpartier |


