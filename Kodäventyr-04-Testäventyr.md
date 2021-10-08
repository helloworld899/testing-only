# Testäventyr och Kodäventyr #04

Det här kodäventyret är lite annorlunda, då istället för att fokusera på en uppgift så kommer vi dela upp denna i två.

Den första biten är ganska liten kodmässigt, men kommer introducera er till att skriva era första tester.

Den andra biten är en valfri lite klurigare uppgift för er som klarat Kodäventyr #03.

## Uppgiftsprioritering

- Gör först Testäventyret som beskrivs nedan
- Gör sedan klart Kodäventyr #03
- Gör efter det Level-Up-uppgifterna på Kodäventyr #03
- Efter det så gör Kodäventyr #04 som beskrivs nedan

Om du totalt fastnar på Level-up-uppgifterna på Kodäventyr #03 och behöver ta en paus från det så kan du börja titta på Kodäventyr #04, men om du gör det så vill jag att du skriver kommentarer i Kodäventyr #03 om vad du fastnade på och vad du testat. Det måste inte vara en lång kommentar.

# Testäventyr

Du kan använda dig av ett befintligt projekt, eller skapa ett nytt. Om det är första gången du gör det så rekommenderar jag dig att skapa ett nytt projekt - för att undvika problem med att IntelliJ inte fungerar som det ska, eller tvingar oss att göra vissa justeringar som kan vara svåra att hitta.

Om du skapar ett nytt projekt så skapa några metoder som gör lite olika saker. Exempelvis:
- En metod som adderar två tal `public static int add(int a, int b) {` som retunerar summan av de talen
- En metod som dubblerar ett tal `public static int double(int num) {` som retunerar `num * 2` 

Med det har vi lite kod som vi kan testa lägga in tester i.

- Se på den inspelade videon från 2021-10-08 när jag introducerar tester
  -  Det kortkommando jag använder i Maven-filen (`pom.xml`) och när jag lägger till tester för mina metoder är `Alt + Insert`. Det är en genväg till "Generate", som du också ser om du högerklickar i koden
    - I `pom.xml` genererar jag en "Dependency" (junit-jupiter)
    - I min java-fil genererar jag ett test

Vad jag gör i videon är detta:

- Skapar en klass som jag vill testa
- Högerklickar på projektet upp till vänster och väljer "Add framework support"
- Kryssar i Maven och går vidare
- Ändrar groupID i `pom.xml`
- Klickar "Reload Maven configuration"
- Går tillbaka till min klass
- Högerklickar i den och väljer "Generate" och sedan "Tests", kryssar i rutorna för de metoder jag vill skapa tester för
- Går till pom.xml och lägger in beroendet till junit-jupiter (högerklicka -> Generate -> Dependency)
- Klickar "Reload Maven configuration"
- Skriver mina tester i filen IntelliJ genererade åt oss

Det vi kan använda för att skriva våra första tester är till exempel:

- assertEquals
- assertNotEquals

### Mitt exempel från Videon

    import static org.junit.jupiter.api.Assertions.*;
    
    class CaesarCipherExampleTest {
    
        @org.junit.jupiter.api.Test
        void caesar() {
            assertEquals("B", CaesarCipherExample.caesar("A", 1));
            assertEquals(" ", CaesarCipherExample.caesar("Ö", 1));
            assertEquals("A", CaesarCipherExample.caesar(" ", 1));
            assertEquals("A", CaesarCipherExample.caesar("B", -1));
            assertEquals(" ", CaesarCipherExample.caesar("A", -1));
    
        }
    }

## Glosor

- Framework: Ett "ramverk", någonting vi använder när vi programmerar som gör mycket av jobbet åt oss
- Beroenden/dependencies: Saker vårt projekt är beroende av. Exempelvis `java.util.Scanner` eller `java.util.Random`. Vissa beroenden är en del av Java. Vissa andra beroenden måste vi importera med andra verktyg, som Maven. Ett beroende som vi importerar i det här kodäventyret är `org.junit.jupiter`.
- Maven: Ett ramverk som bland annat tar hand om vårt projekts beroenden (som JUnit)
- JUnit: Ett test-ramverk som inte är en del av grundpaketen i Java, och därför behöver importeras med Maven
- Assert: Engelska för "försäkra", som i "Försäkra oss att `add(7,3)` ger tillbaka siffran 10". Om svaret är något annat så misslyckas testet. Om det är det vi förväntar oss så passerar testet. 

## Läs mer här

- Om vad vi kan testa: https://howtodoinjava.com/junit5/junit-5-assertions-examples/

# Kodäventyr #04

## Alternativ 1 (avancerat)

Det här är en övning för de som vill kolla vidare på lite saker utanför kursen, men som kan vara väldigt bra att kunna. Det handlar om två-dimensionella arrayer och nästlade for-loopar.

Vi har tidigare deklarerat arrayer såhär:

    int myArray = new int[10];

Vilket ger oss en array med plats för 10 element.

För att skapa en tvådimensionell array kan vi göra såhär:

    int myArray = new int[10][10];    // exempel 1
    char myArray = new char[10][10];  // exempel 2
    
Det här är en array som innehåller 10 arrayer som är 10 arrayer stora vardera. Det betyder att vi kan spara 100 värden i myArray.

### Varför vill vi använda tvådimensionella arrayer?

De kan vara väldigt användbara. De går att använda som koordinater, exempelvis i ett spel. Den första dimensionen innehåller x (bredd) och den andra innehåller y (höjd). Tillsammans kan vi peka ut en exakt plats på vår skärm.

De går även att använda som en klocka. Det här exemplet kanske inte är så praktiskt, men det kanske gör det lättare att förstå vad dimensionerna betyder:

    int myClock = new int[24][60];
    
Den första dimensionerna är timmarna och varje timma på dygnet har 60 minuter.

    int myClock = new int[24][60];
    
    for (int i = 0; int i < myClock.length; i++) {
        System.out.println("Cuckoo! Cuckoo!");
        
        for (int j = 0; int j < myClock[i].length; j++) {
            System.out.printf("%d:%d", i, j);
        }
    }

## Alternativ 2

Repetition. Öva på det vi gått igenom tidigare i kursen. Kolla w3-schools och den här wikin för att påminna dig om vad de är för saker.

Du kan titta på det google-dokument vi skapade tillsammans tidigare med idéer om vad vi kan göra med programmering. Om du inte hittar det så fråga någon på Discord om var det finns. Du kan skapa ett nytt eget projekt där du försöker göra vad du vill utifrån det vi lärt oss.

### En mer konkret övning till alternativ 2

Om du vill så kan du skapa ett nytt program och öva på att använda arrayer, for-loopar och metoder.

Skapa metoder som retunerar:

- En sträng
- en integer
- en array av strängar
- en boolean
- en array av booleans

Testa göra lite mattemetoder. Metoder som gör enkla matematiska uträkningar. Exempelvis

- add(int a, int b) som retunerar summan av a och b
- double(int a, int b) som dubblar värdet av a och b
- divide(int a, int b) som delar a med b och retunerar svaret. Obs: Du kan behöva retunera en float här, då division inte alltid blir till heltal

Anropa dessa metoder ifrån din `main`-metod. Testa kalla en metod från en annan metod.

Samla felmeddelanden (anteckna dem någonstans och ta med till nästa lektion).

## Inspiration

Titta på den kod jag laddat upp här: https://github.com/zocom-bjorn-pettersson/CAWS21