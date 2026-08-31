## **NFR-4: Datalagring**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 |Speldata sparas vid krasch/omstart - Sparas lokalt i webbläsare genom cookie-samling| 
|    NFR-01.2 |Sparad speldata vid krasch/avstängd process ska automatiskt raderas 24 timmar efter senaste aktivitet| 
|    NFR-01.3 |Systemet ska enbart lagra den data som krävs för att spelet kan kunna köras korrekt| 
|    NFR-01.4 | | 
|    NFR-01.5 |         | 



## **NFR-4.1: Användbarhet**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 | Det ska vara tydligt vems tur det är, vilket resultat matchen fick och hur användaren startar ett nytt parti. | 
|    NFR-01.2 |Ingen registrering krävs, anonymt och friktionsfritt att komma igång.| 
|    NFR-01.3 |Enkla icke tekniska felmeddelanden.| 
|    NFR-01.4 |Webbsidan ska fungera på mobil och dator (support av 16:9 och 9:16 aspect ratio). | 
|    NFR-01.5 |         | 



## **NFR-4.2: Prestanda**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 |Spelet ska vara responsivt utan lag.  | 
|    NFR-01.2 |Tolerans för prestanda och svarstid < 0.33s |
|    NFR-01.3 || 
|    NFR-01.4 | | 
|    NFR-01.5 |         | 


## **NFR4.3: Skalbarhet**
| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 |Arkitekturen ska kunna skalas horisontellt vid trafikökning. | 
|    NFR-01.2 |Systemet ska kunna hantera plötsliga belastningstoppar.| 
|    NFR-01.3 |Inbjudningslänkar ska vara slumpmässigt genererade och tillräckligt komplexa för att inte kunna gissas (brute force)| 
|    NFR-01.4 | | 
|    NFR-01.5 |         | 


## **NFR4.4: Drift** 

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 |Systemet ska automatiskt återansluta en spelare vid kortare avbrott utan att partiet abryts. | 
|    NFR-01.2 || 
|    NFR-01.3 || 
|    NFR-01.4 | | 
|    NFR-01.5 |         | 


## **NFR4.5: Säkerhet**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 | Åtkomstkontroll på inbjudningslänkar, obehöriga tredjeparter ska inte kunna gå med i ett parti. Länken inaktiveras efter 5 minuter. | 
|    NFR-01.2 |All kommunikation mellan klient och server ska ske krypterar via exempelvis HTTPS eller WSS. | 
|    NFR-01.3 || 
|    NFR-01.4 | | 
|    NFR-01.5 |         | 


## **NFR4.6: Testbarhet**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 | Kritiska scenarier som paus, återanslutning och timeout ska kunna testas automatiserat. | 
|    NFR-01.2 |Loggning ska finnas för att i efterhand kunna spåra och felsöka avvikande spelförlopp.| 
|    NFR-01.3 || 
|    NFR-01.4 | | 
|    NFR-01.5 |         | 

## **NFR4.7: Livscykelhantering**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 |Partier som inte återupptagits inom 5 minuter efter krasch/avstängning ska rensas automatiskt.  | 
|    NFR-01.2 |Systemet ska kunna uppdateras utan att pågående partier går förlorade.| 
|    NFR-01.3 || 
|    NFR-01.4 | | 
|    NFR-01.5 |         | 


## **NFR4.8: Regulatoriska krav(GDPR)**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 |Systemet ska kunna radera all sparad speldata kopplad till en specifik session/länk på begäran  | 
|    NFR-01.2 |Systemet ska ha en rutin för att upptäcka och rapportera personuppgiftsincidenter| 
|    NFR-01.3 || 
|    NFR-01.4 | | 
|    NFR-01.5 |         | 


 

