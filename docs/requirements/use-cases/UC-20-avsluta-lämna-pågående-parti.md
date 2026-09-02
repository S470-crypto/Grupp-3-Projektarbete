# UC-20: Avsluta/lämna pågående parti
 
## Meta
- **Use case:** Avsluta/lämna pågående parti
- **Use case ID:** UC-20
- **Primär aktör:** Spelare
- **Syfte:** Ge spelaren möjlighet att avbryta ett pågående parti, antingen genom ett aktivt val i gränssnittet eller genom att lämna webbplatsen, och säkerställa att systemet hamnar i ett definierat och konsekvent tillstånd oavsett hur avslutet sker.

## Förvillkor
- Ett parti pågår eller är pausad (ej redan avslutad med ett resultat)
- Spelaren har en aktiv session kopplad till partiet

## Trigger
Spelaren väljer att lämna spelet, antingen aktivt via en "avsluta parti"-knapp i gränssnittet, eller passivt genom att stänga webbläsarfliken.

## Huvudflöde
1. Spelaren klickar på "avsluta parti"-knappen i gränssnittet
2. Systemet visar en bekräftelsedialog som frågar om spelaren verkligen vill avsluta partiet
3. Spelaren bekräftar avslutet
4. Systemet sparar spelets aktuella tillstånd
5. Systemet markerar partiet som avslutad i förtid eller pausad, beroende på spelläge
6. Vid enspelarläge (mot dator): partiet avslutas helt utan att någon annan användare påverkas
7. Vid online-spel: motspelaren informeras om att spelaren lämnat spelet

## Alternativa flöden
- **A1 – Passivt avslut (stänger flik/kraschar):** Spelaren stänger fliken eller webbläsaren kraschar utan direkt knapptryck. Systemet kan inte reagera proaktivt, utan förlitar sig på att partiet tillstånd redan sparats löpande via icke-nödvändiga cookies.
- **A2 – Motspelaren lämnar ett online-spel:** Den andra spelaren (motståndaren) lämnar partiet istället för den spelare som anropar use caset. Kvarvarande spelare ska informeras om detta av systemet, så att spelet inte hänger i ett odefinierat väntetillstånd.

## Eftervillkor
- Partiet är inte längre aktivt spelbar för den spelare som lämnat
- Partiets tillstånd är sparat och definierat (avslutad i förtid, eller pausad för ev. återupptagning)
- Vid online-spel har den kvarvarande spelaren informerats om att motståndaren lämnat
- Vid enspelarläge finns ingen annan användare eller session som påverkats

## Testbar avslutning
- **T1:** Vid explicit knapptryck på "avsluta parti" och bekräftelse avslutas/pausas partiet, och tillståndet sparas korrekt.
- **T2:** Om spelaren stänger fliken utan varning finns partiets senaste tillstånd sparat och återställbart vid nästa besök.
- **T3:** I online-spel: om spelare A lämnar, får spelare B en tydlig indikation om detta inom en rimlig, definierad tidsgräns.
