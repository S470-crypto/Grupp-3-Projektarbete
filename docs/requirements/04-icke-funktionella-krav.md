## **NFR-01: Datalagring**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-01.1 |Speldata sparas vid krasch/omstart - Sparas lokalt i webbläsare genom cookie-samling| 
|    NFR-01.2 |Sparad speldata vid krasch/avstängd process ska automatiskt raderas 24 timmar efter senaste aktivitet| 
|    NFR-01.3 |Systemet ska enbart lagra den data som krävs för att spelet kan kunna köras korrekt (berättigat intresse) för att systemet ska fungera säkert och stabilt, ska framgå i integritetspolicyn| 
|    NFR-01.4 | | 
|    NFR-01.5 | |  



## **NFR-02: Användbarhet**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-02.1 |Systemet ska tydligt visa vems tur det är, vilket resultat matchen fick och hur användaren startar ett nytt parti. | 
|    NFR-02.2 |Ingen registrering krävs, anonymt och friktionsfritt att komma igång.| 
|    NFR-02.3 |Systemet visar enkla icke tekniska felmeddelanden.| 
|    NFR-02.4 |Webbsidan ska fungera på mobil och dator (support av 16:9 och 9:16 aspect ratio). | 
|    NFR-02.5 |         | 



## **NFR-03: Prestanda**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-03.1 |Spelet ska vara responsivt utan lag.  | 
|    NFR-03.2 |Svarstid under spel gång förväntas vara mindre än 0.33 sekunder per 1000 supress tester. |
|    NFR-03.3 || 
|    NFR-03.4 | | 
|    NFR-03.5 |         | 


## **NFR-04: Skalbarhet**
| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-04.1 |Arkitekturen ska kunna skalas horisontellt vid trafikökning. | 
|    NFR-04.2 |Systemet ska kunna hantera plötsliga belastningstoppar.| 
|    NFR-04.3 |Inbjudningslänkar ska vara slumpmässigt genererade och tillräckligt komplexa för att inte kunna gissas (brute force)| 
|    NFR-04.4 | | 
|    NFR-04.5 |         | 


## **NFR-05: Drift** 

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-05.1 |Systemet ska automatiskt återansluta en spelare vid kortare avbrott utan att partiet abryts. | 
|    NFR-05.2 || 
|    NFR-05.3 || 
|    NFR-05.4 | | 
|    NFR-05.5 |         | 


## **NFR-06: Säkerhet**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-06.1 | Åtkomstkontroll på inbjudningslänkar, obehöriga tredjeparter ska inte kunna gå med i ett parti. Länken inaktiveras efter 5 minuter. | 
|    NFR-06.2 |All kommunikation mellan klient och server ska ske krypterar via exempelvis HTTPS eller WSS. | 
|    NFR-06.3 |Åtkomst till loggfiler är begränsad till de med rollbaserad behörighet i system och administrationsportalen.| 
|    NFR-06.4 | | 
|    NFR-06.5 |         | 


## **NFR-07: Testbarhet**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-07.1 | Kritiska scenarier som paus, återanslutning och timeout ska kunna testas automatiserat. | 
|    NFR-07.2 |Loggning ska finnas för att i efterhand kunna spåra och felsöka avvikande spelförlopp.| 
|    NFR-07.3 || 
|    NFR-07.4 | | 
|    NFR-07.5 |         | 

## **NFR-08: Livscykelhantering**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-08.1 |Partier som inte återupptagits inom 5 minuter efter krasch/avstängning ska rensas automatiskt.  | 
|    NFR-08.2 |Systemet ska kunna uppdateras utan att pågående partier går förlorade.| 
|    NFR-08.3 || 
|    NFR-08.4 | | 
|    NFR-08.5 |         | 


## **NFR-09: Regulatoriska krav(GDPR)**

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    NFR-09.1 |Systemet ska kunna radera all sparad speldata kopplad till en specifik session/länk-ID på begäran av spelare.  | 
|    NFR-09.2 |Systemet ska ha en dokumenterad rutin för att bedöma och rapportera personuppgiftsincidenter till tillsynsmyndigheten inom 72 timmar och spelare ska informeras via banner.| 
|    NFR-09.3 |Endast personer med rollbaserad behörighet har åtkomst till systemets loggar (administratör och dataansvarig), deras handlingar i systemet är spårbara och loggas. | 
|    NFR-09.4 | Spelaren kan begära att få information om personlig data som behandlas, lagringstid och med vilket ändamål.| 
|    NFR-09.5 | Samtycke till cookies ska inhämtas innan cookies sätts, det ska vara enkelt att ge samtycke och att återkalla det.| 
|    NFR-09.6 | Systemet använder lämpliga säkerhetsåtgärder för lagrad data (åtkomstkontroll, kryptering, pseudonymisering och backup)| 

 

