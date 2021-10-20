# Objektorienterad programmering

**Vad är ett objekt?** Ett objekt är en sak, precis som i "den riktiga världen". Ett objekt, eller sak, kan exempelvis vara en bil (klassiskt programmeringsexempel), eller en boll, eller vad som helst.

## Exempel: Det stora mysteriet

Definitioner:

- Användaren: Den som sitter vid datorn och spelar spelet
- Huvudkaraktären (Player): Den karaktär som användaren styr
- Främlingar (Strangers): Personer som kan hjälpa dig på vägen
- Ledtrådar (Clue): Saker du kan samla på dig, som ett tidningsutklipp eller en potatisskalare som du hittar på ett udda ställe

För att sätta ihop det här till ett spel måste vi även ha lite kringliggande grejer - exempelvis en startpunkt för vårt program: Detta är var vår `main`-metod finns.

Om vi kallar vårt projekt (som projektnamnet i IntelliJ) för The Big Mystery, så är ett vanligt val att ha en fil som heter `src/TheBigMystery.java` som används för vår main-metod. I den här filen skapar kommer vi skapa instanser av de andra klasserna - våra objekt.

**En instans av en klass är ett objekt.**

De andra klasserna vi vill skapa är:

- Player.java
- Stranger.java
- Clue.java

Uppmärksamma att vi inte använder plural för klassnamnen. Det heter **Stranger** och inte **Strangers**.

### Player.java

`Player.java` kan se ut såhär:

```java
public class Player {
    private String name;
    private int cluesCollected;

    // Det här är en konstruktor. Den används när vi skriver Player = new Player("Namn");
    public Player(String name) {
        this.name = name; // "this." refererar till attributet några rader upp. this.name är "private String name" och name är det på raden ovanför denna.
        this.cluesCollected = 0; // Sätt attributet till 0 per default
    }

    // Dessa två metoder kallas för "setter" och "getter".
    // När vi använder detta säger vi att vi "enkapsulerar" attributet cluesCollected
    // Just denna metod kanske inte kommer användas så mycket - när vill vi egentligen sätta det här till ett specifikt värde? Kanske vill vi använda den för att sätta det till 0 någon gång, så det skadar inte att ha.
    public static void setCluesCollected(int cluesCollected) {
        this.cluesCollected = cluesCollected;
    }

    // Hur många ledtrådar har vi samlat på oss?
    public static int getCluesCollected() {
        return cluesCollected; // kan även stå this.cluesCollected
    }

    public static void addClue() {
        cluesCollected++; // Om vi hittar en ny ledtråd ökar vi cluesCollected med 1
    }

    // Enkapsulering av attributet "name"
    public static String getName() {
        return name;
    }

    // Enkapsulering av attributet "name"
    public static void setName(String newName) {
        this.name = newName;
    }
}
```

### Ny `Player` i `main()`

Med detta kan vi skapa en instans av klassen `Player` i vår main-klass.

```java
public class TheBigMystery {
    public static void main(String[] args) {
      Player myPlayer = new Player("Björn"); // "Björn" används i konstruktorn ovan

      System.out.println(myPlayer.getName()); // Kommer vara "Björn"
      myPlayer.setName("Blupp");              // Ändra namnet
      System.out.println(myPlayer.getName()); // Kommer nu vara "Blupp"

      System.out.println(myPlayer.getCluesCollected()); // kommer vara 0
      myPlayer.addClue();                               // Lägg till en ledtråd
      System.out.println(myPlayer.getCluesCollected()); // kommer vara 1
    }
}
```

## Varför använder vi enkapsulering? Hur gör vi utan det?

Enkapsulering är inte ett måste men gör dina program mer framtidssäkra. 

## TODO

Det här är en början. Fortsättning följer!