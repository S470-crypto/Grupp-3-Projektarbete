[Tillbaka till README](../../../README.md)
# Use Case ID: UC-10 Skapa konto som admin

## Meta
**Use case:** Skapa konto som admin

**Use case ID:** UC-10

**Primär aktör:** Admin

**Syfte:** Ett personligt konto ska gå att skapa till en ny person med rätt behörighetsroll (Dataansvarig eller Admin/Administratör).

## Förvillkor
- Admin har ett konto med behörighet att lägga upp nya konton och tilldela behörighetsroller i systemet i system- och administrationsportalen (som är skild från spelarnas kontofria spelflöde).
- Admin är inloggad på sitt konto.

## Trigger
- En ny person t.ex. dataansvarig behöver ett eget konto med en rollbaserad behörighet för att kunna logga in i systemet och överse samt hantera sina ansvarsområden. Admin initierar processen med att skapa nytt konto. 

## Huvudflöde
1. Admin går in på funktionen för att skapa nytt konto.
2. Admin anger uppgifter som efterfrågas (namn, epost, roll: Dataansvarig)
3. Systemet skickar en inbjudningslänk till den angivna epostadressen för att verifiera att uppgifterna stämmer, godkänna ansvar som kommer med behörigheten samt att informationen lagras.
4. Nytt lösenord skapas via länken.
5. Systemet aktiverar kontot när nytt lösenord har skapats.

## Alternativt flöde

**A1: Inbjudningslänken aktiveras inte**
1. Kontot blir inte aktiverat via länken inom en rimlig tid (1 timme). 
2. Kontot förblir inaktivt, admin kan trigga systemet att skicka ut en ny länk med inbjudan eller radera kontot.

**A2: Angiven epostadress finns redan registrerad**
1. Systemet upptäcker att epostadressen redan finns registrerad.
2. Systemet visar ett felmeddelande med en varning för admin.
3. Admin får kontrollera uppgifterna och åtgärda problemet. 

## Eftervillkor
- Ett konto har skapats med rätt behörighet. 
- Kontot har aktiverats.
- Användaren har godkänt att informationen lagras.

## Testbar avslutning
Admin med behörighet att registrera nya konton har skapat ett nytt konto och tilldelat rätt behörighetsroll till ny användare, länk med inbjudan skickas till det nya kontots angivna epost. När länken aktiverats och nytt lösenord skapats kan användaren logga in på kontot.
