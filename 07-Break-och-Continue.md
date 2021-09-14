`break` och `continue` kan vara väldigt användbara i `for`- och `while`-loopar.

`break` kan användas för att avbryta och hoppa ur en for-loop.

    for (int i = 0; i < 10; i++) {
      if (i == 4) {
        break;
      }
      System.out.println(i);
    }
    System.out.println("Slut");

I exemplet ovan så ska for-loopen räkna till 10, men när `i` kommer till 4 så hoppar den ur innan den skriver ut siffran 4. Så här blir resultatet:

    0
    1
    2
    3
    Slut

`continue` kan på ett liknande sätt användas för att avbryta - men den avbryter bara _just den här gången_ och går vidare till nästa direkt.

    for (int i = 0; i < 10; i++) {
      if (i == 4) {
        continue;
      }
      System.out.println(i);
    }
    System.out.println("Slut");

Denna kommer hoppa till slutet av det kodblocket (näst sista raden, `}`) och börja om från början av for-loopen när `i` har värdet 4. Som du kan se så har den hoppat över siffran 4:

    0
    1
    2
    3
    5
    6
    7
    8
    9
    Slut

## Se även

* Mer exempel och övningar https://www.w3schools.com/java/java_break.asp