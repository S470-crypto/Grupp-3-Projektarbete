# Use case: UC-14 Logga ut som admin

## Meta

**Use case:** Logga ut som behörig

**Use case ID:** UC-14

**Primär aktör:** Administratör (eller Dataansvarig)

**Syfte:** En administratör eller dataansvarig med behörighet ska kunna avsluta en inloggad session på ett kontrollerat sätt så att inte obehöriga kan komma åt sidan och påverka dess funktioner.

## Förvillkor

- Administratör (eller dataansvarig) är inloggad på ett aktivt konto.

## Trigger

- Administratören är klar med sina uppgifter och väljer att logga ut.

## Huvudvillkor

1. Administratören väljer att logga ut.

2. Systemet avslutar sessionen.

3. Administratören loggas ut, sidan för inloggning visas.

## Alternativa flöden

**A1:** Utloggning pga inaktivitet

- Administratören har varit inaktiv 15 minuter vilket triggar systemet att logga ut

- Systemet avslutar den aktiva sessionen per automatik.

- Ett meddelande visas (med information om att sessionen avslutats pga inaktivitet) och sidan för inloggning visas då administratören kan välja att logga in på nytt.

## Eftervillkor

- Administratören är utloggad och sessionerna har avslutats.Det är inte möjligt att "backa tillbaka" för att komma till inloggat läge igen, ny inloggning behöver göras för att logga in igen.

## Testbar avslutning

En administratör som har en aktiv session loggar ut och alla sessioner avslutas då. Det går inte att få tillgång till de funktioner som hör till dennes roll i utloggat läge.
