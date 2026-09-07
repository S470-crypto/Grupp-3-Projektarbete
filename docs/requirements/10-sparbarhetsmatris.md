[Tillbaka till README](../../README.md)
# 10. Spårbarhetsmatris



## 10.1 Funktionella krav och relaterade use cases

|FR-ID  | Krav (kortfattad beskrivning)                  | UC-ID          |
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
|FR-01.14|  Visa felmeddelande |       UC-12 |
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
|    FR-02.9|  Parti/speldata raderas automatiskt. | UC-NFR-06|




## 10.2 Icke funktionella krav och relaterade use cases


| NFR-ID      | Krav (kortfattad beskrivning)   |    UC-ID  |
| ----------- | ----------- | --------|
|    NFR-01.1 |Speldata sparas vid krasch/omstart|   UC-NFR-07  |
|    NFR-01.2 |Speldata raderas 24 timmar efter senaste aktivitet|  UC-NFR-06  |
|    NFR-01.3 |Systemet ska lagra den data som krävs | UC-07, UC-17, UC-NFR-07  |
|    NFR-01.4 | Cookies lagras pseudonymiserat i 6 månader|  UC-17 |
|    NFR-01.5 |Den data som systemet lagrar ska framgå i integritetspolicyn |  UC-10, UC-17, UC-18  |
|    NFR-02.1 |Systemet visar turordning, resultat och hur spelare startar parti | UC-01, UC-02, UC-04, UC-06, UC-09  |
|    NFR-02.2 |Ingen kontoregistrering krävs |  UC-01, UC-02, UC-03  |
|    NFR-02.3 |Systemet visar enkla icke tekniska felmeddelanden.| UC-12 |
|    NFR-02.4 |Webbsidan ska fungera på mobil och dator |  UC-01, UC-02, UC-03, UC-04 |
|    NFR-03.1 |Spelet ska vara responsivt utan lag.  |  UC-NFR-01 |
|    NFR-03.2 |Svarstid under spelets gång. | UC-NFR-01 |
|    NFR-04.1 |Arkitekturen ska kunna skalas horisontellt vid trafikökning. |  UC-NFR-01   |
|    NFR-04.2 |Systemet ska kunna hantera plötsliga belastningstoppar.|  UC-NFR-01  |
|    NFR-04.3 |Inbjudningslänkar ska vara slumpmässigt genererade|  UC-02 |
|    NFR-05.1 |Systemet ska automatiskt återansluta en spelare vid avbrott | UC-07, UC-20, UC-NFR-07  |
|    NFR-06.1 |Tredje person kan inte ansluta till länk (som är giltig 5 minuter) | UC-11, UC-05  |
|    NFR-06.2 |Kommunikation mellan klient och server ska ske krypterat |  UC-02, UC-15, UC-17, UC-NFR-09  |
|    NFR-06.3 |Åtkomst till loggfiler är begränsad|   UC-13, UC-NFR-04|
|    NFR-07.1 |Paus, återanslutning och timeout ska kunna testas automatiserat. | UC-07 |
|    NFR-07.2 |Loggfiler ska registreras | UC-15, UC-NFR-04, UC-NFR-07  |
|    NFR-08.1 |Partier som inte återupptagits inom 24 timmar efter krasch/avstängning ska rensas automatiskt.  |  UC-NFR-06 |
|    NFR-08.2 |Systemet ska kunna uppdateras utan att pågående partier går förlorade.|  UC-NFR-08  |
|    NFR-09.1 |Systemet ska kunna radera all sparad speldata på begäran av spelare (inom en månad).  |  UC-NFR-02 |
|    NFR-09.2 |Systemet ska ha en dokumenterad rutin för personuppgiftsincidenter |  UC-NFR-04  |
|    NFR-09.3 | Åtkomstkontroll |  UC-10, UC-NFR-02, UC-NFR-03, UC-NFR-04 |
|    NFR-09.4 | Spelaren kan begära att få information om personlig data |  UC-NFR-03 |
|    NFR-09.5 | Samtycke till cookies godkänns eller nekas, återkallas| UC-17, UC-18, UC-19|
|    NFR-09.6 | Samtycke till cookies ska lagras|  UC-17  |


## 10.3 Funktionella use cases relaterade till krav

|UC-ID  | Use case namn               | Kopplas till krav ID         |
|-------|-------------------------------|----------------|
|UC-01|  Starta parti mot dator (AI) |FR-01.1, FR-01.4, NFR-02.1, NFR-02.2,  NFR-02.4 |
|UC-02|  Starta parti bjud in vän |FR-01.2, NFR-02.1, NFR-02.2,  NFR-02.4, NFR-04.3 |
|UC-03|  Anslut till parti via länk |FR-01.2, FR-01.9, NFR-02.2,  NFR-02.4 |
|UC-04| Spela igen mot samma motståndare |FR-01.3, NFR-02.1 |
|UC-05| Avbryt väntan vid timeout|FR-01.11, NFR-06.1  |
|UC-06| Spela drag | FR-01.6, FR-01.8, NFR-02.1 |
|UC-07| Pausa och återuppta parti| FR-01.13, NFR-05.1|
|UC-08| Välja svårighetsgrad| FR-01.15 |
|UC-09| Avsluta parti (visa resultat)|  FR-01.5, NFR-02.1|
|UC-10| Skapa konto som admin| FR-02.6, NFR-09.3 |
|UC-11| Förhindra tredje spelare från att ansluta| FR-01.12, NFR-06.1 |
|UC-12| Visa felmeddelande| FR-01.14, NFR-02.3 |
|UC-13| Logga in som behörig| FR-02.1, NFR-09.3 |
|UC-14| Logga ut som behörig| FR-02.1, NFR-09.3 |
|UC-15| Inaktivera konto som admin| FR-02.6, FR-02.8, NFR-06.3, NFR-07.2, NFR-09.3 |
|UC-16| Avgöra vems tur det är| FR-01.8, NFR-02.1 |
|UC-17| Godkänn samtycke till cookies| FR-02.2, NFR-01.3, FR-02.3, NFR-01.4, NFR-09.5, NFR-09.6 |
|UC-18| Neka samtycke till cookies| FR-02.2, FR-02.3, NFR-09.5   |
|UC-19| Rensa cookies (återkalla)| FR-02.3, NFR-09.5 |
|UC-20| Avsluta/lämna pågående parti| FR-01.16, NFR-05.1 |


## 10.4 Icke funktionella use cases relaterade till krav

|UC-NFR-ID  | Use case namn               | Kopplas till krav ID         |
|-------|-------------------------------|----------------|
|UC-NFR-01| Genomsittlig svarstid under spel gång på under 0.33 sekunder på 1000 cypresstester | NFR-03.1, NFR-03.2, NFR-04.1, NFR-04.2|
|UC-NFR-02| Begära radering av speldata | FR-02.7, NFR-09.1 |
|UC-NFR-03| Hantera begäran om integritetsinformation |  FR-02.4, NFR-09.4 |
|UC-NFR-04| Hantering av information vid dataintrång |  FR-02.5, NFR-09.2  |
|UC-NFR-05| Granska systemloggar | |
|UC-NFR-06| Automatisk rensning av partidata| FR-02.9, NFR-01.2,  NFR-08.1  |
|UC-NFR-07| Automatiskt sparande av speldata vid krasch eller omstart | FR-01.13, NFR-01.1,  NFR-05.1  |
|UC-NFR-08| Uppdatera systemet utan att pågående partier går förlorade | FR-01.13, NFR-08.2 |
|UC-NFR-09| Säkerställa krypterad kommunikation mellan klient och server| FR-01.1, NFR-06.2, NFR-09.6 |
