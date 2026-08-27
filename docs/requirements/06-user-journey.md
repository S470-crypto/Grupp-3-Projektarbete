# 6. User journey


## Spår 1: Spelaren godkänner kakan

```mermaid
journey
    title Cookie Consent: Spelaren godkänner kakan
    section Informerat samtycke
        Ser cookie-banner: 4: Spelare
        Godkänner kakan: 5: Spelare
    section Funktionalitet oberoende av val
        Kaka sätts: 5: Systemet
        Spelar parti: 5: Spelare
    section Effekt på lagring
        Lämnar sidan mitt i partiet: 3: Spelare
        Sparar partiets tillstånd: 5: Systemet
        Återvänder till länken: 4: Spelare
        Partiet återställs exakt: 5: Spelare
    section Rätt att återkalla 
        Kan ändra samtycke senare: 5: Spelare
```

## Spår 2: Spelaren avböjer kakan

```mermaid
journey
    title Cookie Consent: Spelaren avböjer kakan
    section Informerat samtycke
        Ser cookie-banner: 4: Spelare
        Avböjer kakan: 3: Spelare
    section Funktionalitet oberoende av val
        Info visas, ingen kaka sätts: 3: Systemet
        Spelar parti: 5: Spelare
    section Effekt på lagring
        Lämnar sidan mitt i partiet: 3: Spelare
        Ingen data att spara: 2: Systemet
        Återvänder till länken: 3: Spelare
        Partiet saknas: 1: Spelare
    section Rätt att återkalla 
        Kan ändra samtycke senare: 4: Spelare
```
