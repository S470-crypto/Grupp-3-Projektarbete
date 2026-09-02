# UC-20: Avsluta/lämna pågående spel
 
## Meta
- **Use case:** Avsluta/lämna pågående spel
- **Use case ID:** UC-20
- **Primär aktör:** Spelare
- **Syfte:** Ge spelaren möjlighet att avbryta en pågående match, antingen genom ett aktivt val i gränssnittet eller genom att lämna webbplatsen, och säkerställa att systemet hamnar i ett definierat och konsekvent tillstånd oavsett hur avslutet sker.

## Förvillkor
- En match pågår eller är pausad (ej redan avslutad med ett resultat)
- Spelaren har en aktiv session kopplad till matchen

## Trigger
Spelaren väljer att lämna matchen, antingen aktivt via en "avsluta match"-knapp i gränssnittet, eller passivt genom att stänga webbläsarfliken.

## Huvudflöde
1. Spelaren klickar på "avsluta match"-knappen i gränssnittet
2. Systemet visar en bekräftelsedialog som frågar om spelaren verkligen vill avsluta matchen
3. Spelaren bekräftar avslutet
4. Systemet sparar matchens aktuella tillstånd
5. Systemet markerar matchen som avslutad i förtid eller pausad, beroende på spelläge
6. Vid enspelarläge (mot dator): matchen avslutas helt utan att någon annan användare påverkas
7. Vid online-spel: motspelaren informeras om att spelaren lämnat matchen

## Alternativa flöden
- **A1 – Passivt avslut (stänger flik/kraschar):** Spelaren stänger fliken eller webbläsaren kraschar utan direkt knapptryck. Systemet kan inte reagera proaktivt, utan förlitar sig på att matchens tillstånd redan sparats löpande via icke-nödvändiga cookies.
- **A2 – Motspelaren lämnar ett online-spel:** Den andra spelaren (motståndaren) lämnar matchen istället för den spelare som anropar use caset. Kvarvarande spelare ska informeras om detta av systemet, så att matchen inte hänger i ett odefinierat väntetillstånd.

## Eftervillkor
- Matchen är inte längre aktivt spelbar för den spelare som lämnat
- Matchens tillstånd är sparat och definierat (avslutad i förtid, eller pausad för ev. återupptagning)
- Vid online-spel har den kvarvarande spelaren informerats om att motståndaren lämnat
- Vid enspelarläge finns ingen annan användare eller session som påverkats

## Testbar avslutning
- **T1:** Vid explicit knapptryck på "avsluta match" och bekräftelse avslutas/pausas matchen, och tillståndet sparas korrekt.
- **T2:** Om spelaren stänger fliken utan varning finns matchens senaste tillstånd sparat och återställbart vid nästa besök.
- **T3:** I online-spel: om spelare A lämnar, får spelare B en tydlig indikation om detta inom en rimlig, definierad tidsgräns.
