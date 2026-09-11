[Tillbaka till README](../../../README.md)
# Use case: UC-13 Logga in som behörig

## Meta

**Use case:** Logga in som behörig

**Use case ID:** UC-13

**Primär aktör:** Admin eller Dataansvarig

**Syfte:** 
En admin eller dataansvarig med behörighet har tillgång till de funktioner som hör till dennes roll i system- och administrationsportalen (som skiljer sig från spelarnas kontofria spelvy).

## Förvillkor

- Admin eller dataansvarig har redan ett aktivt konto med lösenord

## Trigger

- Aktören behöver logga in i portalen för att utföra en uppgift som kräver administratörs- eller dataansvarigs behörighet (t.ex. övervaka drift eller besvara en GDPR-begäran) och navigerar till inloggningssidan.

## Huvudflöde

1. Admin navigerar till inloggningssidan

2. Admin anger giltig e-post och lösenord

3. Systemet verifierar uppgifterna och kontrollerar att kontot är aktivt

4. Systemet loggar in administratören och visar de funktioner som matchar dennes behörighet/roll

## Alternativa flöden

**A1:** Felaktiga inloggningsuppgifter

- Felaktiga inloggningsuppgifter (fel epost och/eller lösenord) har angetts.
Systemet kan inte verifiera uppgifterna
- Ett felmeddelande visas (utan att avslöja om det var e-post eller lösenord som var fel)
- Personen kan försöka igen eller återställa lösenordet

**A2:** Kontot är inaktiverat/borttaget

- Kontot har blivit inaktiverat eller spärrat
Ett felmeddelande visas med information om att åtkomst nekas

## Eftervillkor

- Admin är inloggad och har en aktiv, autentiserad session på sidan

- Endast funktioner som matchar dennes behörighet/roll i systemet är tillgängliga för personen

## Testbar avslutning

När korrekta inloggningsuppgifter angetts för ett aktivt konto kan personen logga in och få tillgång till de funktioner som hör till dennes roll.
