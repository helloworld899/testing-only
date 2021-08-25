Att kunna jämföra värden är en av de grundläggande delarna av programmering.

    Less than: a < b
    Less than or equal to: a <= b
    Greater than: a > b
    Greater than or equal to: a >= b
    Equal to a == b
    Not Equal to: a != b

Observera att för att kolla om två värden är identiska så används `==` och inte ett enkelt `=`. Det senare använder vi när vi tilldelar ett värde till en variabel, det första använder vi om vi vill kolla om de är identiska.

Exempel:

    int x = 10;
    int y = 10;
    
    // Enkelt användande med bara if
    if (x == y) {
      System.out.println("x och y är identiska");
    }
    
    // if och else
    if (x == y) {
      System.out.println("x och y är identiska");
    } else {
      System.out.println("x och y är inte identiska");
    }
    
    // if, else if, och else
    if (x == y) {
      System.out.println("x och y är identiska");
    } else if (x > y) {
      System.out.println("x är större än y");
    } else {
      System.out.println("x och y är inte identiska och x är inte större än y");
    }

Det går även att göra flera jämförelser samtidigt med `&&` ("och").

    // Jämför flera variabler samtidigt med && ("och")
    int x = 11;
    int y = 11;
    int z = 11;
    
    if (x == y && x == z) {
      System.out.println("x är samma som y och x är samma som z");
    }

... eller att bara ena villkoret måste vara sant med `||` ("eller"):

    // Jämför flera variabler samtidigt med || ("eller")
    int x = 11;
    int y = 11;
    int z = 12;
    
    if (x == y || x == z) {
      System.out.println("x är samma som y ELLER x är samma som z");
    }

## Övning

Testa olika jämförelser. Klura ut ett eget exempel från din vardag att använda som utgångspunkt. Exempelvis en klocka med ett larm, om en microvågsugn ska plinga, eller vilket lag som vinner i en sportmatch.

Vad händer om du försöker jämföra två olika datatyper, som en `String` med en `int`? Om du får ett felmeddelande, vad säger det?

## Se även

* Fler exempel och övningar finns här: https://www.w3schools.com/java/java_conditions.asp