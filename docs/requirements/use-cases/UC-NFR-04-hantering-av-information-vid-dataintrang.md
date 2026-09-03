# UC-NFR-04 Hantering av information vid dataintrång

## Meta

**Use case:** Hantering av information vid dataintrång

**Use case ID:** UC-NFR-04

**Primär aktör:** Spelare

**Sekundär aktör:** Dataansvarig

**Syfte:** Säkerställa att systemet uppfyller lagstadgade krav på anmälan och information vid eventuell personuppgiftsincident (art. 33-34 GDPR).

## Förvillkor:

- Systemet larmar för att personuppgiftsincident kan ha skett pga dataintrång.

- Förteckning/rapport från loggar finns gällande vilka data som kan ha påverkats.

## Trigger:

- Dataansvarig informeras om att personuppgifter kan ha exponerats för obehöriga.

## Huvudflöde:

1. Dataansvarig bedömmer dataintrångets omfattning och risknivå samt gör en uppskattning av antalet aktiva spelsessioner som pågått under perioden som omfattas av incidenten.

2. Om dataansvarig bedömmer att risken är på en nivå som kräver anmälan till tillsynsmyndigheten så rapporteras det inom 72 timmar (enl GDPR art. 33).

3. Dataansvarig formulerar ett offentligt meddelande med tydlig information om vad som skett som ska visas på spelsidan i en banner (GDPR art. 34.3 eftersom spelarna saknar konton med kontaktuppgifter och kan inte kontaktas personligen).

4. Dataansvarig sammanställer informationen och dokumenterar incidenten, åtgärder och beslut (enl GDPR art. 33)



## Alternativa flöden:

**A1:** Risken bedöms vara låg

- Om det är osannolikt att incidenten medför finns en risk för spelarnas rättigheter behöver det inte rapporteras till tillsynsmyndigheten men incidenter ska alltid dokumenteras av dataansvarig. 



## Eftervillkor:

- Tillsynsmyndigheten har informerats inom 72 timmar om incidenten omfattas av anmälningsskyldighet.

- Dataansvarig har publicerat information om incidenten i en banner för att informera spelarna.

- Incidenten har dokumenterats av dataansvarig.



## Testbar avslutning:

Vid dataintrång som kan ha exponerat personuppgifter ska dataansvarig göra en riskbedömning ifall tillsynsmyndigheten bör meddelas. Information om incidenten ska publiceras i en banner på startsidan och incidenten ska dokumenteras.
