# Use Case-ID: UC-05 Avbryt väntan vid timeout

## Meta:

**Use case:** Avbryt väntan vid timeout

**Use case ID:** UC-05

**Primär aktör:** Spelare

**Syfte:** Delad länk ska vara giltig/aktiv i 5 minuter sedan ska länken bli ogiltig/inaktiveras. Spelare kan vänta en rimlig tid på att motståndare ska ansluta till partiet, när tidsgräns passerats kan spelaren välja att starta nytt parti eller avsluta. 

## Förvillkor:
- Spelaren har startat ett parti och delat en länk med motståndare.
- Motståndaren har inte klickat på länken/anslutit till partiet.
- Partiet är i ett väntande läge/väntar på motståndare att ansluta.

## Trigger:
- Det finns en tidsgräns i systemet som har passerats utan att motståndare anslutit till partiet via den delade länken. 

## Huvudflöden:
1. Spelaren startar parti och delar länk med motståndare.
2. Systemet väntar på att motståndare ska ansluta och nedräkning till tidsgräns (5 minuter) påbörjas. 
3. Tidsgränsen passeras utan att motståndaren anslutit.
4. Systemet avbryter väntan automatiskt och länken är inte längre giltig. 
5. Systemet meddelar väntande spelaren att väntetiden har gått ut. 

## Alternativa flöden:
**A1:** Spelaren avbryter partiet
1. Spelaren avbryter det startade partiet innan motståndaren klickat på länken.
2. Systemet avbryter väntande tillstånd.
3. Information visas för spelare och motståndare som klickar på länken att spelet har avbrutits. 

## Eftervillkor:
- Partiet är inte längre aktivt och har lämnat väntandeläge.
- Spelare har fått meddelande med information samt möjlighet att komma vidare genom att starta nytt parti eller avsluta. 

## Testbar avslutning:
Spelare väntar på att inbjuden motståndare ska ansluta. När 5 minuter har passerat (efter tidsgräns) då avbryts "vänta på spelare" automatiskt och meddelande visas där det framgår att motståndare inte har anslutit samt erbjuds möjlighet att gå vidare genom att starta nytt parti eller avsluta.
