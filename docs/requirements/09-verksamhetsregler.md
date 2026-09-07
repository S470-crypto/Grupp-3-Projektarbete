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








## VR-03: Regler för spelare och konton







## VR-04: Regler för data och integritet






##
