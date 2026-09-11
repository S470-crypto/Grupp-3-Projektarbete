[Tillbaka till README](../../../README.md)
# Use case: UC-14 Logga ut som behörig

## Meta

**Use case:** Logga ut som behörig

**Use case ID:** UC-14

**Primär aktör:** Admin eller Dataansvarig

**Syfte:** En admin eller dataansvarig med behörighet ska kunna avsluta en inloggad session på ett kontrollerat sätt så att inte obehöriga kan komma åt sidan och påverka dess funktioner.

## Förvillkor

- Admin eller dataansvarig är inloggad på ett aktivt konto.

## Trigger

- Admin är klar med sina uppgifter och väljer att logga ut.

## Huvudflöde

1. Admin väljer att logga ut.

2. Systemet avslutar sessionen.

3. Admin loggas ut, sidan för inloggning visas.

## Alternativa flöden

**A1: Utloggning pga inaktivitet**

- Admin har varit inaktiv 15 minuter vilket triggar systemet att logga ut

- Systemet avslutar den aktiva sessionen per automatik.

- Ett meddelande visas (med information om att sessionen avslutats pga inaktivitet) och sidan för inloggning visas då admin kan välja att logga in på nytt.

## Eftervillkor

- Admin är utloggad och sessionerna har avslutats.Det är inte möjligt att "backa tillbaka" för att komma till inloggat läge igen, ny inloggning behöver göras för att logga in igen.

## Testbar avslutning

En admin som har en aktiv session loggar ut och alla sessioner avslutas då. Det går inte att få tillgång till de funktioner som hör till dennes roll i utloggat läge.
