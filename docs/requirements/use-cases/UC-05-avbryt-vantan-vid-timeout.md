[Tillbaka till README](../../../README.md)
# Use Case-ID: UC-05 Avbryt väntan vid timeout

## Meta:

**Use case:** Avbryt väntan vid timeout

**Use case ID:** UC-05

**Primär aktör:** Spelare

**Sekundär aktör:** Systemet (tidsgräns)

**Syfte:** Delad länk (länk-ID) ska vara giltig/aktiv i 5 minuter sedan ska länken bli ogiltig/inaktiveras. Spelare ska inte behöva vänta för länge på att motståndare ska ansluta till partiet, när tidsgräns har passerats avbryts partiets väntande tillstånd och spelaren får alternativ för att komma vidare (starta nytt parti eller avsluta spel). 

## Förvillkor:
- Spelaren har startat ett parti och delat en länk med motståndare.
- Partiet är i ett väntande läge/väntar på motståndare att ansluta.
- Motståndaren har inte klickat på länken/anslutit till partiet.

## Trigger:
- Det finns en tidsgräns på 5 minuter i systemet som har passerats utan att motståndare anslutit till partiet via den delade länken. 

## Huvudflöden:
1. Systemet identifierar att tidsgränsen på 5 minuter har passerat utan att motståndaren har anslutit till partiet.
2. Systemet avbryter väntande tillstånd automatiskt och länken inaktiveras, partiet avbryts.
3. Systemet meddelar väntande spelaren att väntetiden har gått ut då motståndaren inte anslöt inom tidsgränsen.
4. Systemet visar spelaren två val: starta nytt parti eller avsluta spel.
5. Spelaren gör ett val och systemet utför den valda åtgärden.

## Alternativa flöden:
**A1: Spelaren avbryter partiet inom tidsgränsen**
- Spelaren avbryter det startade partiet innan motståndaren klickat på länken.
- Systemet avbryter väntande tillstånd och partiet avbryts.
- Spelaren dirigeras om till startsidan.

**A2: Motståndare försöker ansluta efter tidsgränsen**
- Motståndaren klickar på länken efter att tidsgränsen har passerats och länken har inaktiverats.
- Systemet detekterar att länken är inaktiverad.
- Systemet nekar anslutning och felmeddelande visas med information om att länken är ogiltig då tidsgränsen har passerats. 

## Eftervillkor:
- Partiet är inte längre aktivt och det går inte att komma åt det tidigare partiet, länken är inaktiv/ogiltig.
- Spelaren har fått meddelande med information samt möjlighet att komma vidare genom att starta nytt parti eller avsluta. 

## Testbar avslutning:
Spelare väntar på att inbjuden motståndare ska ansluta. När 5 minuter har passerat (efter tidsgräns) då avbryts "vänta på spelare" automatiskt och meddelande visas där det framgår att motståndare inte har anslutit samt erbjuds möjlighet att gå vidare genom att starta nytt parti eller avsluta.
