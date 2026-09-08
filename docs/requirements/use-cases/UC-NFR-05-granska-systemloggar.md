[Tillbaka till README](../../../README.md)


# UC-NFR05: Granska systemloggar

## Meta


**Use case:** Graska systemloggar

**Use case ID:** UC-NFR05

**Primär aktör:** Administratör
**Sekundär aktör:** Dataansvarig

**Syfte:** Säkerställa att implementering av RBAC är korrekt när det gäller granskning av systemloggar.


## Förvillkor
* Administratör/dataansvarig har ett giltigt konto med rollbaserat behörighet till system och administrationsportalen.

* Minst en loggtyp som finns tillgänglig för granskning

## Trigger
Administratören eller dataansvarig behöver granska en eller flera systemloggar i incidentutredning eller felsökningssyfte. 


## Huvudflöde 

1. Aktören loggar in i system-och administrationsportalen.
2. Akötren väljer vilken logg den vill granska.
3. Systemet verifierar att aktörens roll har behörighet att see den valida loggtypen.
4. Aktören genomför sin granskning.
5. Aktörens granskning registreras i sin tur som en spårbar händelse i administratörsloggen.

## Alternativaflöden

A1: Obehörig aktör försöker komma åt en logg. 

## Eftervillkor

* Endast aktörer med rätt rollbaserad behörighet har fått tillgpng till respektive loggtyp.

* Granskningen registreras som en egen spårbar händelse i administratörlogge.

## Testbar avslutning

En aktör med rätt roll kan se granska vald logg och granskningen skall registrerar i administratörloggen. 


   
