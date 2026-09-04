# 10. Spårbarhetsmatris



## 10.1 Funktionella krav och relaterade use cases

|FR-ID  | Krav (kortfattat)                  | UC-ID          |
|-------|-------------------------------|----------------|
|FR-01.1|  Starta parti utan konto  |UC-01, UC-02    |
|FR-01.2|  Bjud in till parti via delad länk |   UC-02, UC-03    |
|FR-01.3|  Spela igen mot samma motståndare |   UC-04          |
|FR-01.4|  Spelare starta parti mot dator (AI) |       UC-01          |
|FR-01.5|  Resultat visas efter avslutat parti  |     UC-09   |
|FR-01.6|  Spelare placera bricka |        UC-06 |
|FR-01.7|  Systemet visar turordning |    UC-16    |
|FR-01.8|  Spelare kan spela drag    |  UC-06, UC-16         |
|FR-01.9|  Anslut till parti via delad länk     |      UC-03     |
|FR-01.10|  Systemet känner av 5 i rad |   UC-09 |
|FR-01.11| Avbryt väntan på spelare |       UC-05 |
|FR-01.12|   Bara två spelare kan vara anslutna till ett parti. |    UC-11           |
|FR-01.13| Pausa och återuppta parti |    UC-07    |
|FR-01.14|  Visa felmeddelande |       UC-12, NFR-02.3  |
|FR-01.15|   Välja svårighetsgrad |     UC-08   |
|FR-01.16|   Avsluta pågående parti   |  UC-20      |
|FR-01.17|   Systemet känner av oavgjort  |    UC-09      |
|    FR-02.1 | Logga in och ut med rollbaserad behörighet.|  UC-13, UC-14 | 
|    FR-02.2 |  Cookie samtycke via banner. |  UC-17 |
|    FR-02.3 |  Cookie går att samtycka till, neka eller återkalla.   |  UC-17, UC-18, UC-19  |
|    FR-02.4 |  Begäran integritetsinformation.  | UC-NFR-03 |
|    FR-02.5 |  Hantering vid personuppgiftsincident. | UC-NFR-04|
|    FR-02.6 |  Administratör hantering av konton. | UC-10 |
|    FR-02.7 |  Begäran radering av integritetsinformation.  | UC-NFR-02|
|    FR-02.8 |  Åtgärder loggas i systemet. | UC-10, UC-15|
|    FR-02.9|  Partidata raderas automatiskt. ||




## 10.2 Icke funktionella krav och relaterade use cases


| NFR-ID      | Beskrivning |    UC-ID  |
| ----------- | ----------- | --------|
|    NFR-01.1 |Speldata sparas vid krasch/omstart|     |
|    NFR-01.2 |Speldata raderas 24 timmar efter senaste aktivitet|    |
|    NFR-01.3 |Systemet ska lagra den data som krävs |   |
|    NFR-01.4 | Cookies lagras pseudonymiserat i 6 månader|   |
|    NFR-01.5 |Den data som systemet lagrar ska framgå i integritetspolicyn |    |
|    NFR-02.1 |Systemet visar turordning, resultat och hur spelare startar parti |   |
|    NFR-02.2 |Ingen kontoregistrering krävs |    |
|    NFR-02.3 |Systemet visar enkla icke tekniska felmeddelanden.|  |
|    NFR-02.4 |Webbsidan ska fungera på mobil och dator |   |
|    NFR-03.1 |Spelet ska vara responsivt utan lag.  |  UC-NFR-01 |
|    NFR-03.2 |Svarstid under spel gång förväntas vara mindre än 0.33 sekunder per 1000 supress tester. | UC-NFR-01 |
|    NFR-04.1 |Arkitekturen ska kunna skalas horisontellt vid trafikökning. |    |
|    NFR-04.2 |Systemet ska kunna hantera plötsliga belastningstoppar.|   |
|    NFR-04.3 |Inbjudningslänkar ska vara slumpmässigt genererade|   |
|    NFR-05.1 |Systemet ska automatiskt återansluta en spelare vid avbrott |   |
|    NFR-06.1 |Obehöriga tredjeparter ska inte kunna gå med i ett parti. |   |
|    NFR-06.2 |Kommunikation mellan klient och server ska ske krypterat |    |
|    NFR-06.3 |Åtkomst till loggfiler är begränsad|   UC-13, UC-NFR-04|
|    NFR-07.1 | Paus, återanslutning och timeout ska kunna testas automatiserat. |  |
|    NFR-07.2 |Loggfiler ska finnas |  UC-NFR-04  |
|    NFR-08.1 |Partier som inte återupptagits inom 24 timmar efter krasch/avstängning ska rensas automatiskt.  |   |
|    NFR-08.2 |Systemet ska kunna uppdateras utan att pågående partier går förlorade.|    |
|    NFR-09.1 |Systemet ska kunna radera all sparad speldata kopplad till en specifik session/länk-ID på begäran av spelare (inom en månad).  |  UC-NFR-02 |
|    NFR-09.2 |Systemet ska ha en dokumenterad rutin för personuppgiftsincidenter |  UC-NFR-04  |
|    NFR-09.3 | Åtkomstkontroll |  UC-10, UC-NFR-02, UC-NFR-03, UC-NFR-04 |
|    NFR-09.4 | Spelaren kan begära att få information om personlig data |  UC-NFR-03 |
|    NFR-09.5 | Samtycke till cookies godkänns eller nekas, återkallas| UC-17, UC-18, UC-19|
|    NFR-09.6 | Samtycke till cookies ska lagras|  UC-17  |

