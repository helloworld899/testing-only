`break` och `continue` kan vara väldigt användbara i `for`- och `while`-loopar.

`break` kan användas för att avbryta och hoppa ur en for-loop.

    for (int i = 0; i < 10; i++) {
      if (i == 4) {
        break;
      }
      System.out.println(i);
    }

I exemplet ovan så ska for-loopen räkna till 10, men när `i` kommer till 4 så hoppar den ur innan den skriver ut siffran 4.

`continue` kan på ett liknande sätt användas för att avbryta - men den avbryter bara _just den här gången_ och går vidare till nästa direkt.

    for (int i = 0; i < 10; i++) {
      if (i == 4) {
        continue;
      }
      System.out.println(i);
    }

Denna kommer hoppa till slutet av det kodblocket och börja om från början av for-loopen när `i` har värdet 4.

## Se även

* Mer exempel och övningar https://www.w3schools.com/java/java_break.asp