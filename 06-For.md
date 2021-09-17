Nu börjar vi komma till lite mer spännande saker, nämligen "for"-loopar. Det kanske ser lite komplicerat ut, men det är oerhört kraftfullt med få rader kod. Lite kreativa tillämpningar nämns även nedan.

## Syntax

    for (statement 1; statement 2; statement 3) {
        // code block to be executed
    }
    
* Statement 1 is executed (one time) before the execution of the code block
* Statement 2 defines the condition for executing the code block
* Statement 3 is executed (every time) after the code block has been executed
    
Detta exempel kommer skriva ut siffran 0 till 4:

    for (int i = 0; i < 5; i++) {
      System.out.println(i);
    }

## Terminologi och historia

För länge sedan fanns det ett populärt programmeringsspråk som hette Fortran. I detta språk användes `i` som namn på en variabel av typen integer som ändrade värde, precis som i vårt exempel ovan. Av historiska skäl, och som en sorts konvention, så används `i` ofta som ett kort namn på en variabel vars namn "inte riktigt spelar så stor roll". Om du behöver använda fler variabler i samma veva så används `j`, `k`, et cetera. I dagligt språk kanske du skulle säga x, y och z. Här används alltså ofta i, j och k istället.


## Kreativt användande

Vad gör denna kod? Kan du med papper och penna räkna ut vad den gör, steg för steg?

    for (int i = 0; i < 5; i++) {
      for (int j = 0; j < 5; j++) {
        System.out.print(i);            // Obs .print() och inte .println()
      }
      
      System.out.println();
    }

## Övning

Vi har tidigare (som i Kodäventyr #1) kastat tärning. Hur kan du använda en for-loop för att kasta tärningen flera gånger?

Extra:
* Använd Scanner för att låta användaren bestämma hur många gånger tärningen ska kastas
* Ha en variabel som heter `total` som du sparar totalen av alla tärningar (om 5 tärningskast landar på 5 blir det 25 poäng, exempelvis)

## Se även

* Mer exempel och övningar: https://www.w3schools.com/java/java_for_loop.asp