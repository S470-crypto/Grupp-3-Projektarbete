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
| UC-01 | Starta nytt parti mot dator (AI) | S | AI | FR-01.1, FR-01.4, NFR-02.1, NFR-02.2, NFR-02.4 |
| UC-02 | Starta parti bjud in vän | S, M | — | FR-01.2, NFR-02.1, NFR-02.2, NFR-02.4, NFR-04.3 |
| UC-03 | Anslut till parti via länk | M | S | FR-01.2, FR-01.9, NFR-02.2, NFR-02.4 |
| UC-04 | Spela igen mot samma motståndare | S, M | — | FR-01.3, NFR-02.1 |
| UC-05 | Avbryt väntan vid timeout | S | — | FR-01.11, NFR-06.1 |
| UC-06 | Spela drag | S | M, AI | FR-01.6, FR-01.8, NFR-02.1 |
| UC-07 | Pausa och återuppta parti | S | — | FR-01.13, NFR-05.1 |
| UC-08 | Välja svårighetsgrad | S | — | FR-01.15 |
| UC-09 | Avsluta parti | SYS | S, M | FR-01.5, NFR-02.1 |
| UC-11 | Förhindra tredje spelare från att ansluta | S | SYS | FR-01.12, NFR-06.1 |
| UC-12 | Visa felmeddelande | SYS | S, M, A | FR-01.14, NFR-02.3 |
| UC-16 | Avgöra vems tur det är | SYS | S, M | FR-01.7, FR-01.8, NFR-02.1 |
| UC-20 | Avsluta/lämna pågående parti | S | M | FR-01.16, NFR-05.1 |
 
### 7.2.1 Spelloop (kärnspel)
 
```mermaid
flowchart LR
    S["👤 Spelare"]
    M["👤 Motståndare"]
    AI["🤖 Dator (AI)"]
 
    subgraph sys["Gomoku-systemet"]
        UC06("UC-06\nSpela drag")
        UC16("UC-16\nAvgöra vems\ntur det är")
        UC09("UC-09\nAvsluta parti")
        UC12("UC-12\nVisa\nfelmeddelande")
        UC07("UC-07\nPausa och\nåteruppta parti")
        UC20("UC-20\nAvsluta/lämna\npågående parti")
 
        UC06 -.->|include| UC16
        UC06 -.->|extend| UC12
        UC16 -.->|include| UC09
    end
 
    S --> UC06
    S --> UC07
    S --> UC20
    M --> UC06
    M --> UC20
    AI --> UC06
```
 
### 7.2.2 Starta parti
 
```mermaid
flowchart LR
    S["👤 Spelare"]
    M["👤 Motståndare"]
    AI["🤖 Dator (AI)"]
 
    subgraph sys["Gomoku-systemet"]
        UC01("UC-01\nStarta nytt parti\nmot dator (AI)")
        UC08("UC-08\nVälja\nsvårighetsgrad")
        UC02("UC-02\nStarta parti\nbjud in vän")
        UC03("UC-03\nAnslut till parti\nvia länk")
        UC05("UC-05\nAvbryt väntan\nvid timeout")
        UC11("UC-11\nFörhindra tredje\nspelare från att ansluta")
        UC04("UC-04\nSpela igen mot\nsamma motståndare")
 
        UC01 -.->|include| UC08
        UC02 -.->|extend| UC05
        UC03 -.->|extend| UC11
    end
 
    S --> UC01
    S --> UC02
    S --> UC05
    S --> UC04
    M --> UC03
    M --> UC04
    AI --> UC01
```
 
### 7.2.3 Cookie-hantering
 
| UC-ID | Use Case-namn | Primär aktör | Sekundär aktör | Kopplat krav |
|-------|--------------|--------------|-----------------|-----------|
| UC-17 | Godkänn samtycke till cookies | S | — | FR-02.2, FR-02.3, NFR-01.3, NFR-01.4, NFR-09.5, NFR-09.6 |
| UC-18 | Neka samtycke till cookies | S | — | FR-02.2, FR-02.3, NFR-09.5 |
| UC-19 | Rensa cookies | S | — | FR-02.3, NFR-09.5 |
 
```mermaid
flowchart LR
    S["👤 Spelare"]
 
    subgraph sys["Gomoku-systemet"]
        UC17("UC-17\nGodkänn samtycke\ntill cookies")
        UC18("UC-18\nNeka samtycke\ntill cookies")
        UC19("UC-19\nRensa cookies")
 
        UC19 -.->|extend| UC17
        UC19 -.->|extend| UC18
    end
 
    S --> UC17
    S --> UC18
    S --> UC19
```
 
---
 
## 7.3 Administration & Autentisering
 
| UC-ID | Use Case-namn | Primär aktör | Sekundär aktör | Kopplat krav |
|-------|--------------|--------------|-----------------|-----------|
| UC-10 | Skapa konto som admin | A | — | FR-02.6, NFR-09.3 |
| UC-13 | Logga in som behörig | A, DA | — | FR-02.1, NFR-09.3 |
| UC-14 | Logga ut som behörig | A, DA | — | FR-02.1, NFR-09.3 |
| UC-15 | Inaktivera konto som admin | A | — | FR-02.6, FR-02.8, NFR-06.3, NFR-07.2, NFR-09.3 |
 
### 7.3.1 Kontohantering
 
```mermaid
flowchart LR
    A["🛠️ Administratör"]
    DA["⚖️ Dataansvarig"]
 
    subgraph sys["System- och administrationsportalen"]
        UC10("UC-10\nSkapa konto\nsom admin")
        UC13("UC-13\nLogga in\nsom behörig")
        UC14("UC-14\nLogga ut\nsom behörig")
        UC15("UC-15\nInaktivera konto\nsom admin")
 
        UC10 -.->|include| UC13
    end
 
    A --> UC10
    A --> UC13
    A --> UC14
    A --> UC15
    DA --> UC13
    DA --> UC14
```
 
---
 
## 7.4 Icke-funktionella / GDPR Use Cases
 
| UC-ID | Use Case-namn | Primär aktör | Sekundär aktör | Kopplat krav |
|-------|--------------|--------------|-----------------|------------|
| UC-NFR-01 | Genomsnittlig svarstid under spelgång under 0,33 sekunder på 1000 cypresstester | A | SYS | NFR-03.1, NFR-03.2, NFR-04.1, NFR-04.2 |
| UC-NFR-02 | Begära radering av speldata | S | DA | FR-02.7, NFR-09.1 |
| UC-NFR-03 | Hantera begäran om integritetsinformation | S | DA | FR-02.4, NFR-09.4 |
| UC-NFR-04 | Hantering av information vid dataintrång | S | DA | FR-02.5, NFR-09.2 |
| UC-NFR-05 | Granska systemloggar | — | — | *(saknas – se anmärkning nedan)* |
| UC-NFR-06 | Automatisk rensning av partidata | SYS | — | FR-02.9, NFR-01.2, NFR-08.1 |
| UC-NFR-07 | Automatiskt sparande av speldata vid krasch eller omstart | SYS | S | FR-01.13, NFR-01.1, NFR-05.1 |
| UC-NFR-08 | Uppdatera systemet utan att pågående partier går förlorade | A | S, SYS | FR-01.13, NFR-08.2 |
| UC-NFR-09 | Säkerställa krypterad kommunikation mellan klient och server | SYS | S, M | FR-01.1, NFR-01.4, NFR-06.2, NFR-09.6 |
 
### 7.4.1 Dataskydd & Insyn
 
```mermaid
flowchart LR
    S["👤 Spelare"]
    DA["⚖️ Dataansvarig"]
 
    subgraph sys["Gomoku-systemet"]
        NFR02("UC-NFR-02\nBegära radering\nav speldata")
        NFR03("UC-NFR-03\nBegära\nintegritetsinformation")
        NFR04("UC-NFR-04\nHantering vid\ndataintrång")
        NFR05("UC-NFR-05\nGranska\nsystemloggar")
 
        NFR04 -.->|include| NFR05
    end
 
    S --> NFR02
    S --> NFR03
    S --> NFR04
    DA --> NFR04
    DA --> NFR05
```
 
### 7.4.2 Speldata & Drift
 
```mermaid
flowchart LR
    SYS["🖥️ Systemet"]
    S["👤 Spelare"]
    A["🛠️ Administratör"]
 
    subgraph sys2["Gomoku-systemet"]
        NFR07("UC-NFR-07\nAutomatiskt sparande\nvid krasch/omstart")
        NFR06("UC-NFR-06\nAutomatisk rensning\nav partidata")
        NFR09("UC-NFR-09\nKrypterad\nkommunikation")
        NFR08("UC-NFR-08\nUppdatera systemet\nutan dataförlust")
        NFR01("UC-NFR-01\nSvarstid under\n0,33 sekunder")
 
        NFR06 -.->|extend| NFR07
    end
 
    SYS --> NFR07
    SYS --> NFR06
    SYS --> NFR09
    A --> NFR08
    A --> NFR01
    S --> NFR07
```
 
---
 
## 7.5 Use Case Priority Matrix
 
| Prioritet | Use Cases |
|----------|----------|
| Kritiskt | UC-01, UC-02, UC-03, UC-06, UC-09, UC-16, UC-12, UC-NFR-01, UC-NFR-07, UC-NFR-09 |
| Bör ha | UC-04, UC-05, UC-07, UC-08, UC-11, UC-20, UC-17, UC-18, UC-19, UC-NFR-02, UC-NFR-03, UC-NFR-06 |
| Kan ha | UC-10, UC-13, UC-14, UC-15, UC-NFR-04, UC-NFR-05, UC-NFR-08 |

(*Alla diagram har tagits fram med hjälp av Claude AI*)

