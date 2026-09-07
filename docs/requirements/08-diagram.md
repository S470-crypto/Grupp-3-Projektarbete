[Tillbaka till README](../../README.md)
# 8. Diagram

## 8.1 Tillståndsdiagram
| Diagram | Täcker Use case| 
| ----------- | ----------- | 
|    Cookie-samtycke |UC-17, UC-18, UC-19| 
|    Partiets tillstånd |UC-01, UC-02, UC-03, UC-04, UC-05, UC-07, UC-09, UC-11, UC-20| 
|    Administratörskonto |UC-10, UC-13, UC-14, UC-15| 

## **Tillståndsdiagram: Cookie-samtycke**
 
```mermaid
%% Täcker use cases: UC-17 (Godkänn samtycke till cookies), UC-18 (Neka samtycke till cookies), UC-19 (Rensa cookies)
stateDiagram-v2
    classDef neutral fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-width:1px
    classDef godkant fill:#dcfce7,stroke:#15803d,color:#14532d,stroke-width:1px
    classDef nekat fill:#fee2e2,stroke:#b91c1c,color:#7f1d1d,stroke-width:1px
 
    [*] --> EjHanterat
    EjHanterat --> Godkänt : Godkänner samtycke
    EjHanterat --> Nekat : Nekar samtycke
    Godkänt --> Nekat : Ändrar val till nekat
    Nekat --> Godkänt : Ändrar val till godkänt
    Godkänt --> EjHanterat : Rensar cookies
    Nekat --> EjHanterat : Rensar cookies
 
    class EjHanterat neutral
    class Godkänt godkant
    class Nekat nekat
 
    note right of EjHanterat
        Dialogen visas på nytt varje gång
        detta tillstånd nås (första besök,
        efter rensning, eller om spelaren
        stänger dialogen utan att välja)
    end note
 
    note right of Nekat
        Spelet är fullt spelbart i detta
        tillstånd - endast strikt nödvändiga
        cookies (t.ex. autosave) är aktiva
    end note
```
## **Tillståndsdiagram: Partiets tillstånd**
 
```mermaid
%% Täcker use cases: UC-01 (Starta parti mot dator), UC-02 (Starta parti, bjud in vän),
%% UC-03 (Anslut till parti via länk), UC-04 (Spela igen mot samma motspelare),
%% UC-05 (Avbryt väntan vid timeout), UC-07 (Pausa och återuppta parti),
%% UC-09 (vinst-/oavgjortkontroll), UC-11 (Förhindra obehöriga från att ansluta),
%% UC-20 (Avsluta/lämna pågående parti)
stateDiagram-v2
    classDef neutral fill:#f3f4f6,stroke:#6b7280,color:#374151,stroke-width:1px
    classDef waiting fill:#fef3c7,stroke:#b45309,color:#78350f,stroke-width:1px
    classDef active fill:#dbeafe,stroke:#1d4ed8,color:#1e3a8a,stroke-width:1px
    classDef paused fill:#e0e7ff,stroke:#4338ca,color:#312e81,stroke-width:1px
    classDef ended fill:#dcfce7,stroke:#15803d,color:#14532d,stroke-width:1px
    classDef cancelled fill:#fee2e2,stroke:#b91c1c,color:#7f1d1d,stroke-width:1px
 
    [*] --> EjStartat
    EjStartat --> VäntarPåMotståndare : Startar parti med vän
    EjStartat --> Pågående : Startar parti mot dator
 
    VäntarPåMotståndare --> Pågående : Motståndare ansluter
    VäntarPåMotståndare --> Avbrutet : Timeout eller avbryts
 
    Pågående --> Pausad : Pausar
    Pausad --> Pågående : Återupptar
 
    Pågående --> AvslutatVinst : Vinst
    Pågående --> AvslutatOavgjort : Oavgjort, fullt bräde
 
    Pågående --> AvbrutetIFörtid : Avslutar/lämnar
    Pausad --> AvbrutetIFörtid : Avslutar/lämnar
 
    AvslutatVinst --> Pågående : Spelar igen
    AvslutatOavgjort --> Pågående : Spelar igen
 
    AvslutatVinst --> [*] : Avslutar
    AvslutatOavgjort --> [*] : Avslutar
    Avbrutet --> [*]
    AvbrutetIFörtid --> [*]
 
    class EjStartat neutral
    class VäntarPåMotståndare waiting
    class Pågående active
    class Pausad paused
    class AvslutatVinst ended
    class AvslutatOavgjort ended
    class Avbrutet cancelled
    class AvbrutetIFörtid cancelled
 
    note right of VäntarPåMotståndare
        Länken är giltig i 5 minuter.
        Vid fler än två anslutningsförsök
        nekas ytterligare spelare
    end note
 
    note right of AvbrutetIFörtid
        Vid online-spel informeras kvar-
        varande spelare om att motståndaren
        lämnat partiet
    end note
```


## 8.2 Aktivitetsdiagram
| Diagram | Täcker Use case| 
| ----------- | ----------- | 
|    Cookie-hantering |UC-17, UC-18, UC-19| 
|    Starta parti |UC-01, UC-08, UC-02, UC-03, UC-05, UC-11| 
|    Spelloop |UC-06, UC-16, UC-12, UC-07, UC-20| 
|    Efter avslutat parti |UC-04| 
