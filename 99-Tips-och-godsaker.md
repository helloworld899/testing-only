Här samlar vi lite kodsnuttar som snabbt ger dig ett ställe att starta på.

## Slumpa tal

Importera bibliotek:

    import java.util.Random;

Slumpa tal:

    Random myRandom = new Random();
    int dice_value = myRandom.nextInt(6) + 1;

I detta exempel får du ett tal mellan 1 och 6. `6` i `.nextInt(6)` är antalet värden du kan få, det lägsta talet är 0 och med 6:an blir det högsta talet du kan få en 5:a (0 till 5 är sex värden). I det här exemplet gör den alltså dig ett tal mellan 0 och 5 som adderar 1 till.


## Läsa användardata

Till detta använder vi Scanner:

        import java.util.Scanner;  // Import the Scanner class

        class Main {
          public static void main(String[] args) {
            Scanner myScanner = new Scanner(System.in);  // Create a Scanner object
            System.out.println("Enter username");

            String userName = myScanner.nextLine();  // Read user input
            System.out.println("Username is: " + userName);  // Output user input
          }
        }


Mer information: https://www.w3schools.com/java/java_user_input.asp

## Avancerat: Läsa användardata med Integer.getInt(), metod, while och try/catch

* Läs mer om try/catch här: https://www.w3schools.com/java/java_try_catch.asp
* Video som presenterar denna kod speladen in 2021-10-14

```java
import java.util.Scanner;

public class ScannerGetIntExample {
    public static void main(String[] args) {
        System.out.println("Get integer:");
        int myFantasticInteger = getInt();
        System.out.println("I picked the integer " + myFantasticInteger);
    }

    public static int getInt() {
        Scanner myScanner = new Scanner(System.in);

        int myInteger;

        while (true) {
            try {
                myInteger = Integer.parseInt(myScanner.nextLine());
                break;
            } catch (Exception e) {
                //System.out.println("Exception: " + e);
                System.out.println("Felaktig indata");
            }
        }

        return myInteger;
    }
}
```

## Print format: `printf()`

Se inspelning från 2021-10-01.

https://w3.cs.jmu.edu/molloykp/teaching/cs149/cs149_2020Fall/labs/ScannerPrintfLab/printf_reference.pdf

## Att dela upp strängar

Säg att du använder Scanner och ska skriva in dina favoritfilmer, men du vill inte göra menyvalet 12 gånger om du vill skriva in 12 filmer. Istället kan du låta användaren skriva in en gång men kommaseparera filmerna, typ såhär:

    Vilken är din favoritfilm?
    > Wild Wild West, Independence Day

Med `split()` kan vi dela den här strängen till 2 filmtitlar.

https://www.w3schools.com/java/java_ref_string.asp

    split() 	Splits a string into an array of substrings 	String[]

Så om vi i koden har detta:

```java
    String favoriteMovies = getUserString();
    String[] favoriteMovieArray = favoriteMovies.split(",");
```

Och sedan kan du använda en for-loop och lägga in alla filmer i arrayen `String[]`.

## Att göra musik med Java

Se kod här: https://github.com/zocom-bjorn-pettersson/CAWS21/blob/main/Music/ToneExperiment.java