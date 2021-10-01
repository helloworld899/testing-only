Metoder är nästa steg som kommer öppna upp många dörrar för er.

## Vad är metoder?

Du har redan använt dig av metoder. Mer specifikt har du använt dig av **en** metod, nämligen `main`-metoden, som kommer i början av varje program du kört. Den brukar se ut så här:

    public class MyClass {
        public static void main(String[] args) { // Det här är "main-metoden", och den anropas alltid automatiskt när vi kör vår kod.
        }
    }

"Anropa" är vad vi säger när vi "kör en metod".

När vi pratar om att skriva egna metoder, så skulle det kunna se ut så här:

    public class MyClass {
         // Det här är "main-metoden", och den anropas alltid automatiskt när vi kör vår kod.
        public static void main(String[] args) {
            int number1 = 10;
            int number2 = 20;
            
            // Här anropar vi metoden "addition" med två argument (number1, number2) och sparar vad den metoden retunerar i variabeln "myTotal".
            int myTotal = addition(number1, number2);
            
            System.out.println("The total is: " + myTotal);
        }

        public static int addition(int numA, int numB) { // Det här är vår nya metod
            int total = numA + numB;
            
            // Här skickar vi tillbaka innehållet i variabeln "total" till där vi anropade den här metoden
            return total;
        }
    }

## Varför använder vi metoder?

Metoder är ett sätt att dela upp kod. Istället för att ha ett jättelångt program där vi upprepar oss flera gånger kan vi istället ha en metod som gör saker enklare för oss. Se exempel länkade nedan.

Fördelar med metoder:

* Det gör vår kod mer läsbar
* Vi kan dela upp koden i olika "syften"
* Vi behöver inte upprepa oss lika mycket
* Det är lättare att ta med oss kod från ett projekt till ett annat
* Koden blir lättare att testa (Se sidan "09 Junit och tester")

Exempel finns här: https://github.com/zocom-bjorn-pettersson/CAWS21/tree/main/methodIntro

I det första exemplet är koden utan metoder, och sedan ändrar vi koden lite för varje nytt exempel. Titta på dem en efter en och jämför dem. Testa köra dem och experimentera själv.

## Hur säger vi vad en metod ska retunera?

Den här metoden retunerar ingenting:

    public static void myMethod1() {
        System.out.println("Hello.");
    }

Den här metoden retunerar en int:

    public static int myMethod2() {
        int myNumber = 3;
        return myNumber;
    }

Den här metoden retunerar en array av integers:

    public static int[] myMethod3() {
        int[] myArray = new int[2]; // En array av längden två
        myArray[0] = 5;
        myArray[1] = 2;
        
        return myArray; // Retunera arrayen
    }

## Övningar

Titta först på länkarna till w3schools nedanför och länken ovanför med mitt exempel.

När du gjort det så kan du börja experimentera själv med metoder. Skapa metoder som retunerar följande:

* En integer
* En String
* En char
* En boolean

Gör dessa en-och-en och anropa dem från din `main()`-metod.

## Se även

* Läs även om metoder på W3Schools: https://www.w3schools.com/java/java_methods.asp
* Övningar finns här: https://www.w3schools.com/java/exercise.asp?filename=exercise_methods1