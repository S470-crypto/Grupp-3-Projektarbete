[Tillbaka till README](../../../README.md)


# UC-NFR-05: Granska systemloggar

## Meta


**Use case:** Granska systemloggar

**Use case ID:** UC-NFR-05

**Primär aktör:** Admin

**Sekundär aktör:** Dataansvarig

**Syfte:** Säkerställa att implementering av RBAC är korrekt när det gäller granskning av systemloggar.


## Förvillkor
* Admin/dataansvarig har ett giltigt konto med rollbaserat behörighet till system och administrationsportalen.

* Minst en loggtyp som finns tillgänglig för granskning

## Trigger
Admin eller dataansvarig behöver granska en eller flera systemloggar i incidentutredning eller felsökningssyfte. 


## Huvudflöde 

1. Aktören loggar in i system-och administrationsportalen.
2. Aktören väljer vilken logg den vill granska.
3. Systemet verifierar att aktörens roll har behörighet att see den valida loggtypen.
4. Aktören genomför sin granskning.
5. Aktörens granskning registreras i sin tur som en spårbar händelse i administratörsloggen.

## Alternativa flöden

**A1: Obehörig aktör försöker komma åt en logg**

- Dataansvarig försöker komma åt t.ex. driftlogg som hen saknar behörighet till.
- Systemet nekar åtkomst till loggen.
- Åtkomstförsöket loggas.
- Dataansvarig ser över listan över tillgängliga loggar. 

## Eftervillkor

* Endast aktörer med rätt rollbaserad behörighet har fått tillgpng till respektive loggtyp.

* Granskningen registreras som en egen spårbar händelse i administratörloggen.

## Testbar avslutning

En aktör med rätt roll kan se granska vald logg och granskningen skall registrerar i administratörloggen. 


   
