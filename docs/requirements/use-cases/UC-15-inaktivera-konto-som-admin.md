# Use case: Inaktivera konto som admin

## Meta

**Use case:** Inaktivera konto som admin

**Use case ID:** UC-15

**Primär aktör:** Administratör

**Syfte:** En administratör med behörighet kan inaktivera konton t.ex. om en person slutar och inte längre ska ha behörighet till systemet

## Förvillkor

- Administratören är inloggad i system- och administrationsportalen och har en aktiv session, denne har behörighet att inaktivera konton.

## Trigger

- Administratören får information om att ett konto med dataansvarigs roll/behörighet ska inaktiveras.

## Huvudvillkor

1. Administratören navigerar till översikten för konton, väljer det konto som ska inaktiveras och väljer inaktivera konto.

2. Systemet ställer kontrollfråga för att bekräfta att inaktiveringen är korrekt.

3. Administratören bekräftar inaktiveringen.

4. Systemet inaktiverar kontot, inloggning spärras och om det eventuella aktiva sessioner avslutas.

5. Systemet pseudonymiserar personliga uppgifter som kan användas för identifiering såsom epost och namn.

6. Historiska handlingar (loggar) sparas med pseudonymiserad information.

## Alternativa flöden

**A1:** Kontot är det enda med behörighet att redigera roller

- Systemet nekar inaktivering.

- Felmeddelande med information om att ny roll med denna behörighet måste läggas upp innan befintligt konto kan inaktiveras.

## Eftervillkor

- Kontot är inaktiverat och kan inte längre användas för inloggning.

- Inga personliga uppgifter som kan användas för att direkt identifiera en person finns kvar i det vanliga registret.

## Testbar avslutning

När en administratör bekräftat att ett konto ska inaktiveras i system- och administrationsportalen så ska kontot inaktiveras och inloggning är inte längre möjlig. Personliga uppgifter pseudonymiseras, historiska handlingar finns kvar för spårbarhet dock utan att kunna koppla direkt till person.





