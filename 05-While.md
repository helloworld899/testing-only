En "while"-loop är en bit kod som körs om och om igen så länge villkoret som är matad till den är "sant" (`true`).

    int counter = 0;
    
    while (counter < 5) {
      System.out.println("Counting: " + counter);
      counter++; // Öka värdet av variabeln counter med 1
    }
    
    System.out.println("Färdigräknat");

## För kalla dagar

Det här är första exemplet kod som kan få din dators fläktar att börja snurra och som kan ge dig lite problem. Om du någon gång varit med om att program kanske bara slutar svara och din mobil inte reagerar vad du än gör så kan det vara någonting i stil med detta som hänt. Även om detta är ett ganska förenklat exempel.

    // Kör på egen risk
    while (true) {
      System.out.println("Hello");
    }

Den här kommer skriva ut texten "Hello" så länge programmet är igång, och det enda sättet du kan få programmet att avsluta är genom att tvångsavsluta det.

## Se även

* Mer exempel och övningar: https://www.w3schools.com/java/java_while_loop.asp