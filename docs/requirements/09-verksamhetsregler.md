[Tillbaka till README](../../README.md)
# 9. Verksamhetsregler för Gomoku spel

Verksamhets regler beskriver de regler som styr hur Gomoku-spelet ska fungera och hur spelare, partier och information ska hanteras.
Reglerna kompletterar de funktionella och icke-funktionella kraven genom att beskriva vad som alltid ska gälla, oavsett hur resultat bestäms, vilka rättigheter spelare har , hur inbjudningar hanteras och hur spel- och användardata behandlas. Reglerna gäller från ett parti har börjat spelar till det avslutas, sparas eller tas bort. De ska också förhindra att spelare gör saker som inte är tillåtna eller får tillgång till information och funktioner som de inte har rätt till.



## VR-01: Spelregler

| ID | Regler |
|----|------|
| VR-01.1 | Ett parti består av två spelare: en spelare och en motståndare(vän), eller en spelare och Dator(AI). |
| VR-01.2 | En spelare får endast placera en bricka på en ledig spelruta. |
| VR-01.3 | Spelarna ska turas om att göra ett drag. |
| VR-01.4 | En spelare får inte ändra eller ta bort en bricka som är redan placerad. |
| VR-01.5 | Ett drag ska tillhöra den spelare vars tur det är. |
| VR-01.6 | En spelare vinner genom att få fem egna brickor (i rad horisontellt, vertikalt eller diagonalt). |
| VR-01.7 | Det behövs inte att skapa konto för att starta ett parti eller för att spela. |
| VR-01.8 | Ett parti mellan två spelare ska kunna startas genom en inbjudningslänk. |
| VR-01.9 | Endast två spelare får delta samtidigt i ett parti. |
| VR-01.10 | En tredje spelare får inte ansluta till ett parti som redan har två deltagare. |
| VR-01.11 | Inbjudningslänk är endast giltig under den angivna giltighetstiden (5 minuter). |
| VR-01.12 | Efter att ett parti har avslutat ska spelarna kunna starta ett nytt parti. |
| VR-01.13 | Spelet tar slut direkt när någon vinner, eller när hela brädet är fullt. |



## VR-02: Regler för spelresultat

| ID | Regler |
|----|------|
| VR-02.1 | Ett parti avslutats på tre sätt: vinst, förlust eller oavgjort. |
| VR-02.2 | Den spelare som uppfyller vinstvillkoret blir vinare och motståndaren blir förlorare. |
| VR-02.3 | Om spelbrädet blir fullt utan att någon av spelare fått fem i rad blir resultatet oavgjort. |
| VR-02.4 | Resultatet ska visas direkt när partiet är avslutat. |
| VR-02.5 | En spelare kan avsluta ett pågående parti när som helst och det räknas inte som en vanlig vinst/förlust genom fem i rad. |
| VR-02.6 | Ett parti ska alltid ha en tydlig början och ett tydligt slut. |


## VR-03: Regler för Dator (AI)

| ID | Regler |
|----|------|
| VR-03.1 | En spelare ska kunna spela mot datorn (AI) i stället mot en annan spelare. |
| VR-03.2 | Spelaren ska kunna välja lätt, medel eller svår innan partiet börjar. |
| VR-03.3 | AI ska kunna göra sina drag enligt samma spelregler som en mänsklig spelare.



## VR-04: Regler för nya partier och inbjudan

| ID | Regler |
|----|------|
| VR-04.1 | Ett parti mellan två spelare ska ha en egen spelanslutning. |
| VR-04.2 | Ett nytt parti ska börja utan tidigare drag. |
| VR-04.3 | Resultatet från ett tidigare parti får inte påverka till ett nytt parti. |
| VR-04.4 | En spelare får bjuda in en motståndare med en inbjudningslänk. |
| VR-04.5 | En inbjudningslänk ska bara fungerar under den bestämda tiden. |
| VR-04.6 | Om ingen motståndaren ansluter innan tiden går ut, ska väntan avslutas. |
| VR-04.7 | När ett parti inte längre är aktivt ska spelaren få information om att partiet inte kan försätta. |


## VR-05: Regler för paus, återupptagning och avslut 

| ID | Regler |
|----|------|
| VR-05.1 |  Ett pågående parti ska kunna pausas när kraven för att spara partiet är uppfyllda. |
| VR-05.2 | Ett pausat parti får återupptas så länge det fortfarande är giltigt. |
| VR-05.3 | Ett pausat parti som inte återupptas inom 24 timmar ska raderas. |
| VR-05.4 | Ett avslutat parti får inte återupptas som ett pågående parti. |
| VR-05.5 | Vid ett tekniskt avbrott ska spelet kunna återansluta utan att partiet förloras (om partiet fortfarande är giltigt). |
| VR-05.6 | Om ett parti inte längre är tillgängligt ska spelaren informeras tydligt. | 


## VR-06: Regler för spelare och konton

| ID | Regler |
|----|------|
| VR-06.1 | En spelare behöver inte registrera sig, logga in eller ange personuppgifter för att spela. |
| VR-06.2 | En inbjudningslänk får bara delas med den person som ska spela. |
| VR-06.3 | En inbjudan kan delas via en kanal som spelaren använder (t.ex. SMS, e-post eller WhatsApp. |
| VR-06.4 | Konto krävs endast för funktioner som behöver ett registrerats konto eller administrativ åtkomst. |
| VR-06.5 | Administratör och Dataansvarig får endast använda de funktioner som deras roll ger behörighet till. |
| VR-06.6 | Spelare får inte ha tillgång till administrativa funktioner från den vanliga spelvyn. |
| VR-06.7 | En spelare ska kunna avslutat spelet utan att skapa konto eller logga ut. |



## VR-07: Tillgänglighets- och informationsregler

| ID | Regler |
|----|------|
| VR-07.1 | Spelet ska vara gratis och kräva inte prenumeration eller betalning. |
| VR-07.2 | En spelare ska kunna förstå spelets grundregler utan tidigare kunskap om Gomoku. |
| VR-07.2 | Spelet ska kunna spelas i en webbläsare på dator eller mobil utan att installera extra program. |
| VR-07.3 | Spelets regler och villkor ska finnas tillgängliga innan spelaren börjar spela. |
| VR-07.4 | Systemet ska tydligt informera spelaren när ett parti avslutas eller inte längre tillgängligt. |
| VR-07.5 | Felmeddelande ska vara enkla och lätta att förstå. |
| VR-07.6 | Det ska finnas kontaktinformation för att rapportera fel eller problem med spelet. |
| VR-07.7 | Information om cookies, integritet och datahantering ska vara lätt att hitta. |
| VR-07.8 | Systemet ska ge en kort instruktion eller FAQ som förklarar hur man spelar och startar ett parti. |



## VR-08: Regler för data och integritet

| ID | Regler |
|----|------|
| VR-08.1 | Systemet får inte sätta cookies innan spelare har fått information och godkänt dem via en tydlig banner. |
| VR-08.2 | Spelaren kan när som helst säga nej till eller ta tillbaka sitt samtycke till cookies. |
| VR-08.3 | Ett pausat parti kan bara återupptas om spelaren har gett samtycke till nödvändiga cookies. |
| VR-08.4 | Data för ett pausat parti ska raderas automatiskt efter 24 timmar inaktivitet. |
| VR-08.5 | Spelaren kan begära att få se sin sparade personliga data genom att kontakta Dataansvarig via hemsidan. |
| VR-08.6 | Spelaren kan begära att sina personuppgifter raderas genom att kontakta Dataansvarig. |
| VR-08.7 | Vid en personuppgiftsincident ska Dataansvarig bedöma och om det krävs, rapportera incidenten till tillsynsmyndighet inom 72 timmar. |
| VR-08.8 | Information om personuppgiftsincident ska visas på spelsidan eftersom spelarna inte har lämnat kontaktuppgifter. |
| VR-08.9 | Personuppgifter ska skyddas genom kryptering och pseudonymisering. |
| VR-08.10 | Dataansvarig ansvarar för att reglerna om GDPR följs i systemet. |
| VR-08.11 | Allt åtgärder som Administratör eller Dataansvarig gör i systemet ska loggas. |
| VR-08.12 | Information om hur spelet hanterar data och cookies ska vara lätt att hitta på webbplatsen. |



## VR-09: Regler för behörighet och säkerhet

| ID | Regler |
|----|------|
| VR-09.1 | Endast behöriga roller får komma åt administrativa funktioner och loggar. |
| VR-09.2 | Kommunikation mellan klient och server ska skyddas mot obehörig åtkomst. |
| VR-09.3 | En spelare får inte kunna ändra motståndare drag eller speldata. |
| VR-09.4 | Administrativa åtgärder ska vara spårbara genom loggning. |




##
