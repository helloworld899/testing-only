En "while"-loop är en bit kod som körs om och om igen så länge villkoret som är matad till den är "sant" (`true`).

    int counter = 0;
    
    while (counter < 5) {
      System.out.println("Counting: " + counter);
      counter++; // Öka värdet av variabeln counter med 1
    }
    
    System.out.println("Färdigräknat");

Den koden skriver ut det här:

    Counting: 0
    Counting: 1
    Counting: 2
    Counting: 3
    Counting: 4
    Färdigräknat

## När och varför vill vi använda en while-loop?

De enklare program vi börjat skriva körs en gång och sedan stängs de av direkt. Många program vi använder i verkligheten fungerar dock inte så. Istället är de igång tills vi väljer att stänga av dem. Det är därför vanligt att en while-loop är bland det första en skriver i ett nytt program.

Pseudokod:

    while (program är igång) {
      kasta en tärning
      visa vad tärningens resultat är

      om användaren vill kasta en till tärning:
          gör ingenting, fortsätt
      annars:
          stäng av program
    }

De är också väldigt bra att ha för att köra vissa saker flera gånger tills vi har nått ett resultat vi vill ha - men utan att vi i förväg vet hur många försök det tar att nå det resultatet. Exempelvis så kanske vi vill kasta om en tärning om den visar en etta, men det nya kastet kanske också landar på en etta? Då vill vi göra det igen ända tills tärningen visar något annat än en etta.

Pseudokod:

    poäng = 0
    kasta en tärning

    om (tärningen har ett värde större än 1) {
      skriv ut "Du fick en tvåa/trea/fyra/femma/sexa"
      lägg till tärningens värde till poängen
    } annars {
    
      while (tärningen har värde 1) {
        skriv ut "Du fick en etta! Kastar igen!"
        kasta tärningen igen
        skriv ut tärningens värde
      }

      lägg till tärningens nya värde till poängen
    }

    skriv ut hur många poäng användaren fick

## För kalla dagar

Det här är första exemplet kod som kan få din dators fläktar att börja snurra och som kan ge dig lite problem. Om du någon gång varit med om att program kanske bara slutar svara och din mobil inte reagerar vad du än gör så kan det vara någonting i stil med detta som hänt. Även om detta är ett ganska förenklat exempel.

    // Kör på egen risk
    while (true) {
      System.out.println("Hello");
    }

Den här kommer skriva ut texten "Hello" så länge programmet är igång, och det enda sättet du kan få programmet att avsluta är genom att tvångsavsluta det. **I IntelliJ avbryter du det genom att trycka på den röda fyrkanten till vänster om där den skriver ut "Hello", där nere i programmet.**

## Se även

* Mer exempel och övningar: https://www.w3schools.com/java/java_while_loop.asp