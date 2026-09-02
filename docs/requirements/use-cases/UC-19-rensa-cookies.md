# UC-19: Rensa cookies
 
## Meta
- **Use case:** Rensa cookies
- **Use case ID:** UC-19
- **Primär aktör:** Spelare
- **Syfte:** Ge spelaren möjlighet att aktivt återkalla sitt tidigare samtyckesval genom att rensa lagrade cookies, så att systemet behandlar spelaren som en ny besökare i samtyckeshänseende.

## Förvillkor
- Spelaren har sedan tidigare ett registrerat samtyckesval (godkänt eller nekat, enligt UC-17/UC-18)
- Spelaren har tillgång till antingen webbläsarens egna cookie-/webbplatsinställningar, eller en av systemet tillhandahållen "rensa cookies"/"hantera samtycke"-funktion i gränssnittet

## Trigger
Spelaren initierar en rensning av cookies, antingen via en funktion i webbplatsens gränssnitt eller via webbläsarens inbyggda cookie-hantering.

## Huvudflöde
1. Spelaren navigerar till funktionen för att hantera eller rensa cookie-inställningar
2. Systemet visar spelarens aktuella samtyckesstatus
3. Spelaren bekräftar att den vill rensa/återkalla sitt samtyckesval
4. Systemet tar bort den lagrade samtyckesinformationen samt eventuella icke-nödvändiga cookies som satts baserat på tidigare samtycke
5. Systemet återställer spelarens status till "inget registrerat samtycke"
6. Vid nästa sidladdning visas cookie-dialogen på nytt (kopplar till UC-17/UC-18)

## Alternativa flöden
- **A1 – Rensning via webbläsaren istället för via gränssnittet:** Spelaren rensar cookies direkt i webbläsarens inställningar, utanför systemets kontroll. Systemet kan inte fånga detta som en aktiv händelse, utan upptäcker det passivt först vid nästa sidladdning (ingen giltig samtyckesdata hittas, dialogen visas enligt UC-17/UC-18).
- **A2 – Tekniskt fel vid rensning:** Om rensningen av tekniska skäl misslyckas, ska systemet informera spelaren om detta och inte felaktigt visa att inget samtycke finns kvar om data i själva verket ligger orörd.

## Eftervillkor
- Tidigare lagrad samtyckesinformation är borttagen
- Spelarens samtyckesstatus är återställd till "inget val gjort"
- Cookie-dialogen kommer att visas igen vid nästa relevanta sidladdning

## Testbar avslutning
- **T1:** Efter rensning via gränssnittets funktion visas cookie-dialogen på nytt vid nästa sidladdning.
- **T2:** Efter rensning finns inga kvarvarande icke-nödvändiga cookies satta av tidigare samtycke.
