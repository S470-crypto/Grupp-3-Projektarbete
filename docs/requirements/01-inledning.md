# 1. Inledning

## 1.1 Om spelet
Gomoku är ett brädspel som kan spelas i webbläsaren på datorn eller mobilen där två spelare turas om att lägga ut brickor för att först få 5 st brickor i rad (vågrätt, lodrätt eller diagonalt). Spelaren kan spela i realtid mot Datorn (AI) eller mot en vän via en delad länk. Ingen installation krävs för att spela spelet. 

## 1.2 Syfte
Det ska vara enkelt för spelaren att komma igång och starta ett spel/parti mot en motståndare (dator eller vän) och att genomföra det tills dess att något av tre slutresultat nåtts: vinst, förlust eller oavgjort. Spelet ska gå att spela på datorn eller i mobilen.  

## 1.3. Systemavgränsning
Spelet täcker spel mot datorn (AI) eller mot en vän (genom att skicka en länk med länk-ID). Ingen nedladdning, inget konto eller inloggning ska krävas för att kunna spela spelet. 
Systemet inkluderar inte användarkonton för spelarna eller topplistor. 

## 1.4 Aktörer

| Aktör | Typ | Beskrivning |
|-------|------|-------------|
| Spelare | Primär aktör (Mänsklig) | Personen som använder systemet för att spela. Hen kan starta parti/spelet, bjuda in till spel, spela mot motståndare (vän) eller Dator (AI). |
| Dator (AI) | Sekundär systemaktör | Agerar som motståndare och spelar mot spelaren i systemet när hen väljer att spela mot dator (AI), beräknar och gör automatiska drag baserat på spelets regler. |
| Motståndare | Primär aktör (Mänsklig) | Personen som till exempel en vän som spelar mot spelaren. |
| Administratör (Systemadmin) | Primär/sekundär aktör (Mänsklig) | Administratör som hanterar behörigheter för användare, drift, tekniska fel och övervakar systemet. |
| Dataansvarig | Primär/sekundär aktör (Mänsklig)| Säkerställer att GDPR följs, ansvarar för radering och eventuella personuppgiftsincidenter. |
| Systemet | Sekundär systemaktör | Validerar drag och raderar inaktiva spelpartier |


