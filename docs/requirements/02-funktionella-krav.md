# 2. Funktionella krav

## 2.1. Spelet, initiering och spelande

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    FR-01.1 |     En spelare ska kunna starta och gå med i ett parti utan att skapa konto eller logga in.    | 
|    FR-01.2 |     Det ska gå att bjuda in vän till spel via delad länk.    | 
|    FR-01.3 |     Efter avslutat spel ska det gå att starta ett nytt spel mellan samma spelare.     | 
|    FR-01.4 |     Spelare ska kunna spela själv mot dator (AI).    | 
|    FR-01.5 |     Systemet ska visa resultatet efter ett avslutat parti som vinst, förlust eller oavgjort.    | 
|    FR-01.6 |     Spelare ska i ett pågående parti kunna placera en bricka på en tom spelruta.  | 
|    FR-01.7 |     Systemet ska visa vems tur det är att göra ett drag. | 
|    FR-01.8 |     Systemet ska känna av att en bricka placerats på en giltig spelruta och sedan alternera turen mellan spelarna. | 
|    FR-01.9 |     Systemet ska tillåta att en motståndare ansluter till ett startat parti via delad länk. | 
|    FR-01.10 |    Systemet ska identifiera när spelare har fem brickor i rad på spelbrädan. | 
|    FR-01.11 |    Systemet ska avbryta väntan på anslutning när det har gått mer än 5 minuter om ingen ansluter till partiet.  | 
|    FR-01.12 |    Systemet ska endast tillåta att två spelare ansluter till ett parti, om en tredje spelare försöker ansluta ska det misslyckas.| 
|    FR-01.13 |    Om spelare gett samtycke till nödvändiga cookies ska ett pågående parti ska kunna pausas och återupptas. | 
|    FR-01.14 |    Systemet ska visa tydliga icke tekniska meddelanden vid fel som uppstått i systemet. | 
|    FR-01.15 |    Systemet ska låta spelaren välja svårighetsgrad (Lätt, Medium, Svår) vid spel mot Dator (AI). |
|    FR-01.16 |    Spelare ska kunna välja att avsluta ett pågående parti. 
|    FR-01.17 |    Systemet ska identifiera när spelbrädet är fullt och visa resultatet som oavgjort.|


## 2.2. Integritet, datarättighet och behörigheter

| ID      | Beskrivning | 
| ----------- | ----------- | 
|    FR-02.1 |     Det ska gå att logga in och ut på sidan med en rollbaserad behörighet som administratör och dataansvarig i en del (system- och administratörsportalen) som är skild från spelarnas kontofria spelvy. | 
|    FR-02.2 |     Systemet ska fråga om cookie samtycke via banner med tydlig information vid första kontakt med webbsidan, innan cookies sätts. |
|    FR-02.3 |     Spelare ska kunna samtycka till eller neka till cookies och samtycket ska gå att återkalla.   | 
|    FR-02.4 |     Spelare ska kunna begära att få ut information om lagrad personlig data genom att skicka förfrågan via hemsidan (till dataansvarig).  | 
|    FR-02.5 |     Vid eventuell personuppgiftsincident ska dataansvarig bedöma och rapportera tillsynsmyndigheten inom 72 timmar och spelare informeras via spelsidan (eftersom kontaktuppgifter saknas). | 
|    FR-02.6 |     Administratören ska kunna skapa nya konton med rollbaserad behörighet och inaktivera samt radera inaktuella konton. | 
|    FR-02.7 |     Spelare ska kunna begära att personuppgifter raderade genom att skicka förfrågan via hemsidan (till dataansvarig).  | 
|    FR-02.8 |     Systemet skapar en loggpost vid åtgärder som utförs av administratör eller dataansvarig i systemet. | 
|    FR-02.9|     Partidata ska raderas automatiskt efter 24 timmars inaktivitet vid pausat spel. |



