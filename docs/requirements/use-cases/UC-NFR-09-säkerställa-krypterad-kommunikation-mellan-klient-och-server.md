# UC-NFR-09 Säkerställa krypterad kommunikation mellan klient och server 

## Meta 
Use case: Säkerställa krypterad kommunikation mellan klient och server

Use case ID: UC-NFR-09

Primär aktör: System

Sekundär aktör: Spelare, Motståndare (indirekt skyddade av åtgärden)

Syfte: Skydda all data som skickas mellan klient och server från avlyssning och manipulation genom kryptering (NFR-06.2).

## Förvillkor: 
Systemet är konfigurerat att endast tillåta krypterade anslutningar (t.ex. HTTPS/WSS)
Ett giltigt TLS-certifikat är installerat och aktivt
Trigger: 
En klient (spelarens webbläsare) initierar kommunikation med servern, t.ex. vid sidladdning, drag, eller realtidsuppdatering i ett online-parti.

## Huvudflöde: 
Klienten initierar en anslutning till servern
Servern och klienten upprättar en krypterad anslutning (TLS-handskakning)
All efterföljande kommunikation (t.ex. drag, tur-status) skickas krypterat
Spelaren använder spelet utan att märka av krypteringen

## Alternativa flöden: 
**A1:** Klienten försöker ansluta okrypterat (t.ex. via http:// istället för https://)
* Servern omdirigerar automatiskt till en krypterad anslutning, eller nekar anslutningen om omdirigering inte är möjlig.
**A2:** TLS-certifikatet har gått ut eller är ogiltigt
* Webbläsaren varnar spelaren och blockerar som standard anslutningen. Detta ska aldrig inträffa i produktion och bör fångas av övervakning innan spelare påverkas.
**A3:** Anslutningen försöker nedgraderas p.g.a. en föråldrad klient/webbläsare

Systemet nekar anslutningen istället för att tillåta en svagare, osäker krypteringsnivå.
## Eftervillkor: 
All kommunikation mellan klient och server under sessionen har skett krypterat
Ingen känslig data (t.ex. länk-ID, speldata) har skickats i klartext
## Testbar avslutning: 
**T1:** Ett anslutningsförsök via okrypterad HTTP omdirigeras till HTTPS, eller nekas.
T2: Nätverkstrafik som fångas upp (t.ex. via paketinspektion i en testmiljö) visar krypterat innehåll, inte klartext.
T3: En anslutning med ett ogiltigt/utgånget certifikat nekas eller varnas för, i enlighet med standardbeteende i moderna webbläsare.
T4: Endast moderna, säkra krypteringsprotokoll (t.ex. TLS 1.2 eller senare) accepteras av servern.
