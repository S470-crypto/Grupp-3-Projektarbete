# UC-NFR-2: Begära radering av speldata
 
## Meta
- **Use case:** Begära radering av speldata
- **Use case ID:** UC-NFR-02
- **Primär aktör:** Spelare
- **Sekundär aktör:** Dataansvarig
- **Syfte:** Ge spelaren möjlighet att begära att all speldata kopplad till en specifik session/länk-ID raderas, i enlighet med rätten till radering (GDPR art. 17), oavsett om spelare har registrerat konto.
## Förvillkor
- Spelaren har en aktiv eller tidigare pausad match kopplad till ett session-/länk-ID
- Systemet har lagrad speldata kopplad till detta ID
- Spelaren har tillgång till en funktion i gränssnittet för att begära radering
## Trigger
Spelaren skickar en begäran till dataansvarig att radera sin speldata, t.ex. via en knapp/länk i gränssnittet ("Radera min speldata").
 
## Huvudflöde
1. Spelaren initierar en raderingsbegäran, kopplad till sitt session-/länk-ID
2. Dataansvarig identifierar vilken lagrad data som är kopplad till det angivna ID:t
3. Systemet visar en bekräftelsevy som beskriver vad som kommer raderas (t.ex. brädtillstånd, matchhistorik, tur-status)
4. Spelaren bekräftar raderingsbegäran
5. Dataansvarig raderar all identifierad speldata kopplad till session-/länk-ID:t permanent
6. Systemet bekräftar för spelaren att raderingen är genomförd

## Alternativa flöden
- **A1 – Ingen data hittas för angivet ID:** Om dataansvarig inte hittar någon lagrad data kopplad till det angivna session-/länk-ID:t, informeras spelaren om detta utan att en felaktig raderingsbekräftelse visas.
- **A2 – Radering begärs för en pågående match:** Om matchen fortfarande pågår aktivt (t.ex. en motspelare är fortsatt inne i matchen vid online-spel), ska motspelaren informeras om att matchen avslutats i förtid på grund av raderingen.

## Eftervillkor
- All speldata kopplad till det angivna session-/länk-ID:t är permanent borttagen av dataansvarig
- Spelaren har fått en tydlig bekräftelse på att raderingen genomförts (eller ett tydligt felmeddelande om den misslyckats)
- Länken/session-ID:t kan inte längre användas för att återuppta matchen
  
## Testbar avslutning
- **T1:** Efter en genomförd raderingsbegäran finns ingen lagrad speldata kvar kopplad till det angivna session-/länk-ID:t.
- **T2:** Ett försök att återuppta matchen via samma länk efter radering misslyckas (länken är ogiltig).
- **T3:** Om ingen data finns för angivet ID visas ett korrekt informationsmeddelande, inte en felaktig raderingsbekräftelse.
- **T4:** Om spelaren avbryter bekräftelsevyn kvarstår all data helt oförändrad.
- **T5:** Raderingsåtgärden är loggad (utan att i sig innehålla onödig persondata) för att kunna verifieras vid en eventuell revision.
