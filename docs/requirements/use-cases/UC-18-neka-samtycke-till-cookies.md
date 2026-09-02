**UC-18 Upptäcka vinst**

# UC-18: Neka samtycke till cookies
 
## Meta
- **Use case:** Neka samtycke till cookies
- **Use case ID:** UC-18
- **Primär aktör:** Spelare
- **Syfte:** Ge spelaren möjlighet att aktivt avböja icke-nödvändiga cookies, samtidigt som webbplatsens kärnfunktionalitet (spelet) förblir fullt tillgänglig.

## Förvillkor
- Spelaren besöker webbplatsen för första gången, eller har tidigare rensat sina cookies
- Inget giltigt samtyckesval finns registrerat för spelaren
- Cookie-dialogen är korrekt konfigurerad och tillgänglig i gränssnittet

## Trigger
Spelaren laddar en sida på webbplatsen där ingen tidigare registrerad samtyckesstatus finns, vilket gör att cookie-dialogen visas.

## Huvudflöde
1. Spelaren navigerar till webbplatsen
2. Systemet kontrollerar om ett giltigt samtyckesval redan finns lagrat
3. Systemet visar en cookie-dialog med information om vilka typer av cookies som används samt alternativ att godkänna eller neka
4. Spelaren läser informationen och klickar på "Neka"
5. Systemet registrerar det nekade samtycket lokalt hos spelaren
6. Systemet ser till att endast strikt nödvändiga cookies (t.ex. för att spelet ska fungera, som autosave av pågående match) förblir aktiva
7. Cookie-dialogen stängs och spelaren kan fortsätta spela utan att någon icke-nödvändig cookie sätts


## Alternativa flöden
- **A1 – Spelaren ändrar tidigare nekat samtycke till godkännande:** Spelaren kan senare ändra sitt val via cookie-inställningar, vilket leder över till UC-17.
- **A2 – Tekniskt fel vid lagring av nekat samtycke:** Om det nekade valet av tekniska skäl inte kan sparas, ska systemet ändå inte aktivera icke-nödvändiga cookies, och bör visa dialogen igen vid nästa besök.

## Eftervillkor
- Spelarens nekande är sparat och kopplat till spelarens session
- Inga icke-nödvändiga cookies är aktiva
- Spelet är fortsatt fullt spelbart trots nekat samtycke
- Cookie-dialogen visas inte igen förrän valet löper ut, ändras, eller rensas av spelaren

## 2.7 Testbar avslutning
- **T1:** Efter klick på "Neka" döljs dialogen och inga icke-nödvändiga cookies (t.ex. analytics) sätts.
- **T2:** Spelet (t.ex. att starta match, göra drag, pausa/återuppta) fungerar fullt ut även efter nekat samtycke – ingen kärnfunktion får vara blockerad.
