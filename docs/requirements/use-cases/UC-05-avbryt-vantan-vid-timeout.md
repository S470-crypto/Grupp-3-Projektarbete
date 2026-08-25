# Use Case-ID: UC-05 Avbryt väntan vid timeout

**Meta:**
- Aktör: Spelare (initierare)
- Relaterade use cases: UC-02 starta parti bjud in vän.

**Förutsättningar:**
- Spelaren har startat ett parti och delat en länk med vän/motspelare.
- Vännen har inte klickat på länken/anslutit till partiet.
- Partiet är i ett väntande läge/väntar på spelare att ansluta.

**Triggar:**
- Det finns en tidsgräns i systemet som passerats utan att motspelare anslutit till partiet via den delade länken. 

**Huvudflöden:**
1. Spelaren (initierare) startar part och delar länken.
2. Systemet väntar på att spelare ska ansluta och nedräkning till tidsgräns påbörjas. 
3. Tidsgränsen passeras utan att motspelaren anslutit.
4. Systemet avbryter väntan automatiskt och länken är inte längre giltig. 
5. Systemet meddelar väntande spelaren att väntetiden har gått ut. 

**Alternativa flöden:**
??

**Postconditions:**
- Partiet är inte längre aktivt och har lämnat väntandeläge.
- Spelare har fått meddelande. 

**Testable end condition:**
Spelare (initierare) väntar på att inbjuden motspelare ska ansluta. När X minuter passerat (efter tidsgräns) då avbryts "vänta på spelare" automatiskt och meddelande visas där det framgår att motspelare inte anslutit.
