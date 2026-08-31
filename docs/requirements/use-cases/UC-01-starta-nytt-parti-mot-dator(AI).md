 # Use Case: UC-01 - Starta nytt parti mot dator (AI)

 **Meta**

 **Use Case ID:** UC-01

 **Namn:** Starta nytt parti

 **Primär aktör:** Spelare

 **Syfte:** Spelaren vill skapa ett nytt Gomoku-parti för att spela.



 **Förvillkor:**

 * Spelaren har webbsidan öppen i en webbläsare (dator eller mobil)
 * Inget konto krävs
 * Ingen aktiv match pågående sedan tidigare



 **Huvudflöde:**

  1. Spelaren navigerar till startsidan.
  2. Spelaren väljer vem hen vill spela mot (dator eller online).
  3. Om spelare väljer dator startas matcken direkt.
  4. Om spelaren väljer online så genereras en unik länk som delas med motståndaren.
  5. Systemet initierr ett nytt tomt spelbräde.
  6. Systemet avgör slumpmässigt eller enligt fast regel vem som börjar.
  7. Systemet visr spelbrädet och markerr vems tur det är.
  8. Partiet är nu redo att spelas.



  **Undatntagsflöde:**

  * Spelaren har ingen internetanslutning
  * Vännen ansluter inte 
  * Sidan kraschar



  **Testbar avslutning**

  Ett nytt tomt Gokomu-parti har skapats och är redo att spelas. 


  


