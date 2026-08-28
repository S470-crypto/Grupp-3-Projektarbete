# Use Case-ID: UC-05 Avbryt väntan vid timeout

## Meta:

**Use case:** Avbryt väntan vid timeout

**Use case ID:** UC-05

**Primär aktör:** Spelare

**Syfte:** Länk ska vara aktiv i 5 minuter, sedan ska den inaktiveras. 

## Förvillkor:
- Spelaren har startat ett parti och delat en länk med motståndare.
- Motståndaren har inte klickat på länken/anslutit till partiet.
- Partiet är i ett väntande läge/väntar på motståndare att ansluta.

## Triggar:
- Det finns en tidsgräns i systemet som passerats utan att motståndare anslutit till partiet via den delade länken. 

## Huvudflöden:
1. Spelaren startar parti och delar länk med motståndare.
2. Systemet väntar på att motståndare ska ansluta och nedräkning till tidsgräns (5 minuter) påbörjas. 
3. Tidsgränsen passeras utan att motståndaren anslutit.
4. Systemet avbryter väntan automatiskt och länken är inte längre giltig. 
5. Systemet meddelar väntande spelaren att väntetiden har gått ut. 

## Alternativa flöden:
**A1:**

## Eftervillkor:
- Partiet är inte längre aktivt och har lämnat väntandeläge.
- Spelare har fått meddelande. 

## Testar avslutning:
Spelare väntar på att inbjuden motståndare ska ansluta. När 5 minuter passerat (efter tidsgräns) då avbryts "vänta på spelare" automatiskt och meddelande visas där det framgår att motståndare inte anslutit.
