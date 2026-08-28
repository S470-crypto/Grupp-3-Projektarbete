# Use Case: UC-15 - Försätta spelet


**Meta**


**Use case:** Försätta spelet

**Use case ID:** UC-15

**Primär aktör:** Spelare

**Syfte:** Spelarn vill försätta ett tidigare pausat spel utan att börja om.



## Förutsättningar:

* Det finns en tidigare pausat och sparat spel
* Spelaren väljer att försätta ett tidigare spel


## Trigger:

Spelaren väljer **Försätta spelet**


## Huvudflöde:

1. Spelaren öppnar Gomoku
2. Systemet kontrollerar om det finns sparat spel
3. Systemet visar Försätt spel
4. Spelaren väljer Försätt spel
5. Systemet öppnar det sparade spelet
6. Systemet visar vems tur det är
7. Spelaren kan försätta spela.


## Alternativaflöden

* Spelaren öppnar Gomoku
* Spelaren väljer **Försätta spelet**.
* Systemet kontrollerar om det finns ett sparat fel.
* Systemet hittar inget sparat spel.
* Systemet visar ett meddelande.
* Spelaren kan välja **Starta nytt spel**.

## Postcondition:

Det tidigare spelet är öppnat och spelaren kan försätta spelar där hen slutade


## Testbar avslutning:

Spelaren kan öppna ett tidigare sparat spel och försätta från samma läge som innan det pausas.

