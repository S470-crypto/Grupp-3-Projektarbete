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


## UJ-03: Spelaren startar parti mot dator (AI)
 
```mermaid
journey
    title Starta parti: Spelaren mot dator (AI)
    section Val av motståndare
      Navigerar till startsidan: 5: Spelare
      Väljer dator (AI) som motståndare: 5: Spelare
    section Matchstart
      Matchen startas direkt: 5: Systemet
      Initierar nytt tomt spelbräde: 5: Systemet
    section Turordning
      Avgör vem som börjar (slump/fast regel): 5: Systemet
      Visar spelbrädet och markerar vems tur det är: 5: Systemet
    section Redo att spela
      Partiet är redo att spelas: 5: Spelare
```

## UJ-04: Motståndare ansluter till parti via länk
 
```mermaid
journey
    title Ansluta till parti via länk
    section Åtkomst via länk
      Klickar på länken: 5: Motståndare

    section Verifiering
      Verifierar att länken är aktiv och att partiet väntar på spelare: 5: Systemet
    section Anslutning

      Ansluter motståndaren till partiet: 5: Systemet
    section Redo att spela

      Visar att båda spelarna är anslutna och vems tur det är: 5: Systemet
```
