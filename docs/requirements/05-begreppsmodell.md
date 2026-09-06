```mermaid
classDiagram
    %% ===== AKTÖRER =====
    class Aktör {
        <<abstract>>
    }
    class Spelare {
        Huvudspelare som initierar/bjuder in till spel
    }
    class Motståndare {
        Motspelaren (vän) som blir inbjuden till spel
    }
    class DatorAI["Dator (AI)"] {
        Motståndare vid enspelarläge
    }
    class Admin {
        Administratör för systemet
    }
    class Dataansvarig
 
    Aktör <|-- Spelare
    Aktör <|-- Motståndare
    Aktör <|-- DatorAI
    Aktör <|-- Admin
    Aktör <|-- Dataansvarig
 
    %% ===== SPELBEGREPP =====
    class Parti {
        +länkID : LänkID
        Pågående spelsession
    }
    class LänkID {
        Unik ID i varje inbjudningslänk
    }
    class Spelvy {
        Spelarnas kontofria gränssnitt
    }
    class Spelbrädet {
        Där spelet pågår
    }
    class Spelruta {
        Ruta/position där bricka placeras
    }
    class Bricka {
        Det spelarna placerar på brädet
    }
    class Drag {
        Spelarens tur att placera bricka
    }
    class Spelresultat {
        <<enumeration>>
        Vinst
        Förlust
        Oavgjort
    }
 
    Spelare "1" --> "1" Spelvy : använder
    Motståndare "1" --> "1" Spelvy : använder
    Spelvy "1" --> "1" Parti : visar
 
    Spelare "1" --> "1" Parti : initierar
    Parti "1" *-- "1" LänkID : identifieras av
    Parti "1" --> "0..1" Motståndare : bjuder in
    Parti "1" --> "0..1" DatorAI : spelar mot (enspelarläge)
    Parti "1" *-- "1" Spelbrädet : äger
    Spelbrädet "1" *-- "*" Spelruta : består av
    Spelruta "1" o-- "0..1" Bricka : kan innehålla
    Spelare "1" --> "*" Drag : utför
    Motståndare "1" --> "*" Drag : utför
    Drag "1" --> "1" Spelruta : placerar bricka på
    Drag "1" --> "1" Bricka : placerar
    Parti "1" --> "1" Spelresultat : avgörs till
    Spelresultat --> "5" Bricka : fem i rad avgör Vinst/Förlust
 
    %% ===== SYSTEMBEGREPP =====
    class Systemet {
        Hanterar spelet och dess funktioner
    }
    class AuditLog["Audit.log"] {
        All systemaktivitet lagras här
    }
    class AdminPortal["System- och administrationsportalen"] {
        Portal för drift, säkerhet och behörighet
    }
    class Cookie {
        Sparar samtycke för loggning i audit.log
    }
 
    Systemet "1" --> "*" Parti : hanterar
    Systemet "1" --> "1" AuditLog : skriver till
    Admin "1" --> "1" AdminPortal : loggar in i
    Dataansvarig "1" --> "1" AdminPortal : loggar in i
    AdminPortal "1" --> "1" AuditLog : övervakar
    Spelare "1" --> "0..1" Cookie : ger samtycke via
 
    %% ===== GDPR / INTEGRITETSBEGREPP =====
    class GDPR {
        General Data Protection Regulation
    }
    class Samtycke {
        Cookie consent
    }
    class Pseudonymisering {
        Personuppgifter ersätts med kod/pseudonym
    }
    class Kryptering {
        Gör information oläslig för obehöriga
    }
    class Anonymisering {
        Personuppgifter tas bort permanent
    }
    class Personuppgiftsincident {
        Incident kopplad till personuppgifter
    }
 
    Cookie "1" --> "1" Samtycke : representerar
    GDPR "1" --> "*" Samtycke : kräver
    GDPR "1" --> "*" Pseudonymisering : kräver
    GDPR "1" --> "*" Kryptering : kräver
    GDPR "1" --> "*" Anonymisering : kräver
    GDPR "1" --> "*" Personuppgiftsincident : reglerar hantering av
    Dataansvarig "1" --> "1" GDPR : ansvarar för efterlevnad av
    Personuppgiftsincident "1" --> "1" AuditLog : loggas i
```


# Förklaring till modellen

Spelbegrepp: En Spelare initierar ett Parti och bjuder in en Motståndare (via en LänkID) eller spelar mot Dator (AI) i enspelarläge. Partiet äger ett Spelbrädet som består av flera Spelruta. Genom ett Drag placerar spelaren en Bricka på en spelruta. Partiet avgörs till ett Spelresultat: Vinst, Förlust eller Oavgjort.

Systembegrepp: Systemet hanterar alla pågående partier och skriver all aktivitet till Audit.log. Admin och Dataansvarig loggar in i System- och administrationsportalen för att hantera drift, säkerhet och behörigheter — separat från spelarnas kontofria Spelvy.

GDPR/integritetsbegrepp: GDPR styr hur personuppgifter hanteras genom krav på Samtycke (via Cookie), Pseudonymisering, Kryptering och Anonymisering, samt hur en eventuell Personuppgiftsincident ska loggas och hanteras.
