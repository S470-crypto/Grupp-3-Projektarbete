# **UC-17 Visa vems tur det är**

## **Meta**

ID: UC-17

Namn: Visa vems tur det är

Aktör: System

Syfte: Systemet ska visa spelare vems tur det är att göra drag.

## **Förvillkor**

* Systemet har ett giltigt turtillstånd

* Matchen är startad och pågående

## **Huvudflöde**

1. Systemet hämtar aktuellt turtillstånd

2. Systemet renderar en visuell indikator för att visa vilken spelares tur det är

3. Indikatorn uppdateras direkt när turtillståndet ändras

4. Vid online ska indikatorn visas för båda spelare så att båda ser samma information samtidigt

## **Alternativt flöde**

A1 - Spel mot dator
När det är datorns tur ska indikatorn visa t.ex "datorn tänker" istället för en annans spelares namn, tills datorns drag är slutfört.

## **Postconditions**

Systemets gränssnitt reflekterar exakt det turtillstånd som systemet har internt för samtliga spelare i matchen.

## **Testbar avslutning**

* Vid matchstart visar gränssnittet korrekt vilken spelare som går först

* Indikatorn ska uppdateras direkt efter ett drag är gjort, utan att sidan ska behöva laddas om

* I onlineläge ser båda spelare samma turinformation 

