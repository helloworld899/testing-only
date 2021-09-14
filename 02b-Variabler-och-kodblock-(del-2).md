## Variablers synlighet

Det är viktigt _var_ vi deklarerar våra variabler.

Ett exempel, titta extra på raderna med variabeln `lastValue`:

    public class variabeltest {
        public static void main(String[] argv) {
                int counter = 0;
                int lastValue = 0; // här deklareras lastValue;
    
                while (counter < 5) {
                  System.out.println("Counting: " + counter);
                  lastValue = counter;  // Sätt sista värdet till samma sak som counter är
    
                  counter++; // Öka värdet av variabeln counter med 1
                }
    
                System.out.println("Sista talet är: " + lastValue);
        }
    }

Detta kommer skriva ut:

    Counting: 0
    Counting: 1
    Counting: 2
    Counting: 3
    Counting: 4
    Sista talet är: 4

Samma exempel där det inte fungerar, även om vi kanske tycker att det borde fungera:

    public class variabeltest2 {
        public static void main(String[] argv) {
                int counter = 0;
                // Nu deklarerar vi inte lastValue på den här raden
    
                while (counter < 5) {
                  System.out.println("Counting: " + counter);
                  int lastValue = 0;  // Nu deklarerar vi istället variabeln här, och inte uppe vid "int counter = 0;"
    
                  counter++; // Öka värdet av variabeln counter med 1
                }
    
                System.out.println("Sista talet är: " + lastValue);
        }
    }

Men den där koden fungerar inte. Vi säger ju var den ska användas, men inte på ett sätt datorn tycker om. Felmeddelandet vi får när vi testar den koden är det här:

    variabeltest2.java:12: error: cannot find symbol
                System.out.println("    Sista talet är: " + lastValue);
                                                            ^
      symbol:   variable lastValue
      location: class variabeltest2
    1 error

Och vad står det här? Det viktiga är den första raden `error: cannot find symbol`. Den säger också vilken fil det är i `variabeltest2.java` i detta fall, det kan stå `Main.java` där för er om ni lägger in detta i IntelliJ. Det står också vilken rad felet är på, direkt efter filnamnet, `:12` betyder "rad 12".

`symbol`, som den inte kan hitta, är i detta fall vår variabel.

Sen säger den också vilken variabel det är: `variable lastValue`.

Om vi räknar raderna så ser vi att rad 12, och den kodrad som skrivits ut, inte är när vi deklarerar variabeln (vilket är på rad 7), utan var vi använder den (på rad 12).

Det här hanlar om kodblock, och variablers "scope", eller _var variabler syns_. I detta fall så existerar inte `lastValue` på rad 12. `lastValue` existerar i detta fall endast i while-loopen, och när while-loopen är slut så försvinner allt som gjordes i den, _som inte berörde variabler som deklarerats utanför while-loopen_, som exempelvis `counter`.

Kodblock är en hierarki. Under `class`-blocket finns `public static void main`-blocket, och direkt under den finns både `counter` och `while`-blocket.

**Ett kodblock börjar med tecknet `{` och avslutas med tecknet `}`.**

Skillnaderna mellan de två olika exemplena:

* I det fungerande exemplet är `lastValue` deklarerad i `while`-blocket
* I det trasiga exemplet är `lastValue` deklarerad i `public static void main`-blocket, men det viktiga är inte att det deklareras i _just det blocket_ utan att det deklareras _innan_ och _ovanför_ `while`-blocket

För att:

* Ett kodblock kan använda variabler deklarerade i blocket i sig, men även variabler deklarerade _ovanför_
* Det betyder också att ett kodblock inte kan använda sig av variabler som deklareras i _underliggande_ block