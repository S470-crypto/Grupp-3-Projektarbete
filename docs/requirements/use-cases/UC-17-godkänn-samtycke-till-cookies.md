# **UC-17 Godkänn samtycke till cookies**

## **Meta**
Use case: Godkänn samtycke till cookies

Use case ID: UC-17

Primär aktör: Spelare

Syfte: Ge spelaren möjlighet att aktivt acceptera användning av cookies, i enlighet med GDPR.

## **Förvillkor**

- Spelaren besöker webbplatsen för första gången, eller har tidigare rensat sina cookies
- Inget giltigt samtyckesval finns registrerat för spelaren
- Cookie-dialogen är korrekt konfigurerad och tillgänglig i gränssnittet

  ## **Trigger**
Spelaren laddar en sida på webbplatsen där ingen tidigare registrerad samtyckesstatus finns, vilket gör att cookie-dialogen visas.

## **Huvudflöde**
1. Spelaren navigerar till webbplatsen
2. Systemet kontrollerar om ett giltigt samtyckesval redan finns lagrat
3. Systemet visar en cookie-dialog med information om vilka typer av cookies som används samt alternativ att godkänna eller neka
4. Spelaren läser informationen och klickar på "Godkänn"
5. Systemet registrerar samtycket lokalt hos spelaren
6. Systemet aktiverar cookie-samling för spelaren
7. Cookie-dialogen stängs och spelaren kan fortsätta använda webbplatsen normalt

## **Alternativa flöden**

- **A1 – Spelaren stänger dialogen utan att välja:** Om spelaren stänger bannern (t.ex. via kryss) utan att aktivt klicka "Godkänn" eller "Neka", ska detta *inte* tolkas som samtycke. Systemet behandlar detta som om inget val gjorts, och dialogen bör visas igen vid nästa sidladdning.
- **A2 – Spelaren ändrar tidigare godkännande:** Om spelaren senare vill ändra sitt samtycke (t.ex. via en cookie-inställningslänk i sidfoten), leder detta till samma flöde som ovan men med möjlighet att uppdatera ett redan existerande val.

## **Eftervillkor**

- Spelarens samtyckesval är sparat och kopplat till spelarens webbläsare/session
- Endast de cookie-kategorier som spelaren godkänt är aktiva
- Cookie-dialogen visas inte igen förrän samtycket löper ut, återkallas, eller rensas av spelaren
Systemets gränssnitt reflekterar exakt det turtillstånd som systemet har internt för samtliga spelare i matchen.

## **Testbar avslutning**

* Vid matchstart visar gränssnittet korrekt vilken spelare som går först

* Indikatorn ska uppdateras direkt efter ett drag är gjort, utan att sidan ska behöva laddas om

* I onlineläge ser båda spelare samma turinformation 

