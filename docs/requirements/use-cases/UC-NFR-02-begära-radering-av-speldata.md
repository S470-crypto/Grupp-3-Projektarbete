# UC-21: Begära radering av speldata
 
## 1.1 Meta
- **Use case:** Begära radering av speldata
- **Use case ID:** UC-21
- **Primär aktör:** Spelare
- **Syfte:** Ge spelaren möjlighet att begära att all speldata kopplad till en specifik session/länk-ID raderas, i enlighet med rätten till radering (GDPR art. 17).
## 1.2 Förvillkor
- Spelaren har en aktiv eller tidigare pausad match kopplad till ett session-/länk-ID
- Systemet har lagrad speldata kopplad till detta ID (t.ex. via autosave)
- Spelaren har tillgång till en funktion i gränssnittet för att begära radering (eller en angiven kontaktväg för sådana begäranden)
## 1.3 Trigger
Spelaren väljer att begära radering av sin speldata, t.ex. via en knapp/länk i gränssnittet ("Radera min speldata") eller genom att skicka en begäran via en angiven kanal.
 
## 1.4 Huvudflöde
1. Spelaren initierar en raderingsbegäran, kopplad till sitt session-/länk-ID
2. Systemet identifierar vilken lagrad data som är kopplad till det angivna ID:t
3. Systemet visar en bekräftelsevy som beskriver vad som kommer raderas (t.ex. brädtillstånd, matchhistorik, tur-status)
4. Spelaren bekräftar raderingsbegäran
5. Systemet raderar all identifierad speldata kopplad till session-/länk-ID:t permanent
6. Systemet bekräftar för spelaren att raderingen är genomförd

## 1.5 Alternativa flöden
- **A1 – Ingen data hittas för angivet ID:** Om systemet inte hittar någon lagrad data kopplad till det angivna session-/länk-ID:t (t.ex. redan raderad eller aldrig sparad), informeras spelaren om detta utan att en felaktig raderingsbekräftelse visas.
- **A2 – Radering begärs för en pågående match:** Om matchen fortfarande pågår aktivt (t.ex. en motspelare är fortsatt inne i matchen vid online-spel), ska motspelaren informeras om att matchen avslutats i förtid på grund av raderingen.
- **A3 – Spelaren avbryter bekräftelsevyn:** Vid steg 3–4, om spelaren väljer att avbryta istället för att bekräfta, sker ingen radering och all data kvarstår oförändrad.
- **A4 – Tekniskt fel vid radering:** Om raderingen av tekniska skäl misslyckas (t.ex. lagringsfel), ska spelaren informeras tydligt om att raderingen inte kunde slutföras, snarare än att systemet felaktigt bekräftar en lyckad radering.
## 1.6 Eftervillkor
- All speldata kopplad till det angivna session-/länk-ID:t är permanent borttagen ur systemet
- Spelaren har fått en tydlig bekräftelse på att raderingen genomförts (eller ett tydligt felmeddelande om den misslyckats)
- Länken/session-ID:t kan inte längre användas för att återuppta matchen
## 1.7 Testbar avslutning
- **T1:** Efter en genomförd raderingsbegäran finns ingen lagrad speldata kvar kopplad till det angivna session-/länk-ID:t.
- **T2:** Ett försök att återuppta matchen via samma länk efter radering misslyckas (länken är ogiltig).
- **T3:** Om ingen data finns för angivet ID visas ett korrekt informationsmeddelande, inte en felaktig raderingsbekräftelse.
- **T4:** Om spelaren avbryter bekräftelsevyn kvarstår all data helt oförändrad.
- **T5:** Vid ett tekniskt fel under radering informeras spelaren korrekt, och systemet visar inte en felaktig "lyckad radering"-bekräftelse.
- **T6:** Raderingsåtgärden är loggad (utan att i sig innehålla onödig persondata) för att kunna verifieras vid en eventuell revision.
