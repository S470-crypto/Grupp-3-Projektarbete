# UC-NFR-03 Hantera begäran om integritetsinformation

## Meta

**Use case:** Hantera begäran om integritetsinformation

**Use case ID:** UC-NFR-03

**Primär aktör:** Spelare
**Sekundär aktör:** Dataansvarig

**Syfte:** Spelaren har möjlighet att begära och information om den personliga data som hanteras och behandlas (enligt GDPR artikel 12-13).

## Förvillkor:

- Spelaren skickar en förfrågan till dataansvarig via epost till supportadress.

- Länk-ID anges i förfrågan kopplat till ett aktivt parti.

## Trigger:

- Spelaren vill veta vad som sparas om hen och skickar förfrågan via epost till supportadress.

## Huvudvillkor:

1. Spelaren begär att få information om vilken data som hanteras kopplat till länk-ID och hur den data behandlas.
2. Dataansvarig tar emot begäran och verifierar att länk-ID:t är giltigt/aktivt.
3. Dataansvarig söker upp partidata kopplat till länk-ID:t på servern.
4. Dataansvarig sammanställer informationen: aktuell partidata kopplat till länk-ID (spelbräde, brickor och status), generell information om att IP-adress lagras en begränsad tid (berättigat intresse) samt information om hur cookies hanteras vid samtycke, vilken funktion cookies har för spelet och att det samtycke ligger kvar i 6 månader (om det inte återkallas).
5. Dataansvarig svarar spelaren via epost inom en månad.

## Alternativa flöden:

**A1:** Spelaren undrar specifikt om samtycke till cookies

- Dataansvarig svarar spelaren med information om var spelaren själv kan kontrollera sitt samtycke samt hur hen kan se när samtycke skett i webbläsaren/klienten.

**A2:** Det saknas tillräckligt med information

- Länk-ID saknas eller är ogiltigt och det finns inte tillräckligt med identifierande information för att kunna söka i servern.
- Dataansvarig återkopplar till spelaren via mail och efterfrågar mer information, t.ex. till ett aktivt länk-ID med en pågående spelsession.

## Eftervillkor:

Spelaren får besked att endast minimalt med information lagras, varför den lagras och att det endast är strikt nödvändig information som lagras.

## Testbar avslutning:

När spelaren skickat begäran om integritetsinformation kopplat till länk-ID hanteras det av dataansvarig som tar fram informationen och återkopplar till spelaren.
