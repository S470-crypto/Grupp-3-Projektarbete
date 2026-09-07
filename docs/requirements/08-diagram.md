[Tillbaka till README](../../README.md)
# 8. Diagram

## 8.1 Tillståndsdiagram
| Diagram | Täcker Use case| 
| ----------- | ----------- | 
|    Cookie-samtycke |UC-17, UC-18, UC-19| 
|    Partiets tillstånd |UC-01, UC-02, UC-03, UC-04, UC-05, UC-07, UC-09, UC-11, UC-20| 
|    Administratörskonto |UC-10, UC-13, UC-14, UC-15| 

**Tillståndsdiagram: Cookie-samtycke**
 
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

## 8.2 Aktivitetsdiagram
| Diagram | Täcker Use case| 
| ----------- | ----------- | 
|    Cookie-hantering |UC-17, UC-18, UC-19| 
|    Starta parti |UC-01, UC-08, UC-02, UC-03, UC-05, UC-11| 
|    Spelloop |UC-06, UC-16, UC-12, UC-07, UC-20| 
|    Efter avslutat parti |UC-04| 
