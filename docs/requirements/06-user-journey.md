# 6. User journey


## UJ-01: Spelaren samtycker till cookie

```mermaid
journey
    title Cookie Consent: Spelaren godkänner cookie
    section Informerat samtycke
        Ser cookie-banner: 4: Spelare
        Godkänner cookie: 5: Spelare
    section Funktionalitet oberoende av val
        Cookie sätts: 5: Systemet
        Spelar parti: 5: Spelare
    section Effekt på lagring
        Lämnar sidan mitt i partiet: 3: Spelare
        Sparar partiets tillstånd: 5: Systemet
        Återvänder till länken: 4: Spelare
        Partiet återställs exakt: 5: Spelare
    section Rätt att återkalla 
        Kan ändra samtycke senare: 5: Spelare
```

## UJ-02: Spelaren nekar samtycke till cookie

```mermaid
journey
    title Cookie Consent: Spelaren avböjer cookie
    section Informerat samtycke
        Ser cookie-banner: 4: Spelare
        Avböjer cookie: 3: Spelare
    section Funktionalitet oberoende av val
        Info visas, ingen cookie sätts: 3: Systemet
        Spelar parti: 5: Spelare
    section Effekt på lagring
        Lämnar sidan mitt i partiet: 3: Spelare
        Ingen data att spara: 2: Systemet
        Återvänder till länken: 3: Spelare
        Partiet saknas: 1: Spelare
    section Rätt att återkalla 
        Kan ändra samtycke senare: 4: Spelare
```


_Koden till ovan diagram i mermaid har tagits fram med hjälp av AI (claude.ai)_ 
