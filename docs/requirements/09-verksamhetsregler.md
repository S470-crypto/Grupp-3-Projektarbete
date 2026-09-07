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
| VR-02-.5 | 






## VR-03: Regler för spelare och konton







## VR-04: Regler för data och integritet






##
