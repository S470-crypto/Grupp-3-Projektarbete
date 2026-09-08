[Tillbaka till README](../../README.md)
# 7. Use Cases Overview

## 7.1 Aktörer

|  Aktör | Beskrivning |
|--------------|-------|
| Spelare (S)| Använder systemet för att starta och spela spel mot en vän eller datorn. |
| Motståndare (M)| Den andra spelaren (mänsklig) som deltar i samma parti via inbjudningslänk. |
| Dator (AI) | Spelar automatisk mot spelaren och gör drag enlig spelets regler. |
| Administratör (A)| Hanterar användare, behörigheter och tekniska problem. |
| Dataansvarig (DA)| Ansvarar för GDPR, dataradering och personuppgiftsincidenter. |
| Systemet (SYS)| Kontrollerar drag och hanterar sparade och inaktiva spel. |


---
 
## 7.2 Funktionella Use Cases
 
| UC-ID | Use Case-namn | Primär aktör | Sekundär aktör | Kopplat krav |
|-------|--------------|--------------|-----------------|-----------|
| UC-01 | Starta nytt parti mot dator (AI) | S | AI | Krav 3 |
| UC-02 | Starta parti, bjud in vän | S | M | Krav 4 |
| UC-03 | Anslut till parti via länk | M | S | Krav 4, Krav 5 |
| UC-04 | Spela igen mot samma motståndare | S | M | Krav 8 |
| UC-05 | Avbryt väntan vid timeout | S | — | Krav 4 |
| UC-06 | Spela drag | S | M, AI | Krav 6 |
| UC-07 | Pausa och återuppta parti | S | — | Krav 1 |
| UC-08 | Välja svårighetsgrad | S | — | Krav 3 |
| UC-09 | Avsluta parti (vinst/oavgjort) | SYS | S, M | Krav 9 |
| UC-16 | Avgöra vems tur det är | SYS | S, M | Krav 6 |
| UC-11 | Förhindra obehöriga från att ansluta | S | SYS | Krav 4 |
| UC-12 | Visa felmeddelande | SYS | S, M, A | Krav 6, Krav 9 |
| UC-20 | Avsluta/lämna pågående parti | S | M | Krav 1 |



