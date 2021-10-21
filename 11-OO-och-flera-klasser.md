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
    public int getCluesCollected() {
        return cluesCollected; // kan även stå this.cluesCollected
    }

    public void addClue() {
        cluesCollected++; // Om vi hittar en ny ledtråd ökar vi cluesCollected med 1
    }

    // Enkapsulering av attributet "name"
    public String getName() {
        return name;
    }

    // Enkapsulering av attributet "name"
    public void setName(String newName) {
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

https://www.w3schools.com/java/java_encapsulation.asp

## Arv

https://www.w3schools.com/java/java_inheritance.asp

Arv är aktuellt när flera olika klasser har många saker gemensamt. Katter och hundar är kanske olika djur - men de är båda djur. Det betyder att vi skulle kunna ha en hierarki som ser ut såhär:

- class Animal
  - class Dog
  - class Cat

Sättet vi skapar en hierarki som denna i Java är att vi använder ordet "extends" när vi deklarerar våra klasser. Så här:

Animal.java:

```java
public class Animal {
    int numberOfLegs;
    String greeting;

    public Animal(numberOfLegs) {
        this.numberOfLegs = numberOfLegs;
    }

    public void hello() {
        System.out.println(greeting);
    }
}
``` 

Cat.java:

```java
public class Cat extends Animal {
    // ... your code here
}
``` 

Dog.java:

```java
public class Dog extends Animal {
    // ... your code here
}
```

**Extends gör att Dog och Cat ärver attribut och metoder som deklarerats i Animal.**

Om vi nu gör detta:

```java
Dog myDog = new Dog(4);
myDog.greeting = "Hello, I'm a dog.";
myDog.hello();
```

Kommer metoden `hello()` och attributet `greeting` finnas i Dog.

### Men vad gör vi med `Cat` och `Dog` då?

Nu kommer vi in på det som dessa djur inte har gemensamt. Exempelvis är katter bättre på att smyga än hundar, så i klassen `Cat` kanske vi har en metod för det:


```java
public class Cat extends Animal {
    public void sneak() {
        System.out.println("I'm a cat and I am sneaking.");
    }
}
``` 

## Polymorfism

https://www.w3schools.com/java/java_polymorphism.asp

Polymorfism handlar om att göra ändringar **i någonting vi ärvt** efter att vi ärvt något. Detta inkluderar "Override" och "Overload".

Konkret så kanske en hund och en katt båda hälsar, men hunden gör det lite annorlunda. Så här:

```java
public class Dog extends Animal {
    public void hello() {
        System.out.println("The dog is very exited to see you!");
        System.out.println(greeting);
    }
}
```

Här "override:ar" vi metoden `hello()` som vi ärvde från Animal. Vi har gjort en liten ändring i hur den fungerar.

# Glosor

## Access modifiers: public, private, protected

- public betyder att informationen är tillgänglig för alla. Vem som helst kan komma åt eller ändra ett attribut, eller anropa en metod
- private betyder att endast klassen som metoden eller attributet eller metoden deklareras i får komma åt den
- protected är som private men även klasser som ärver kommer åt attributen eller metoderna
- https://www.w3schools.com/java/java_modifiers.asp
- https://iq.opengenus.org/public-private-protected-in-java/

# static

Om du sätter ett attribut till `static` så delas det med alla andra instanser av den klassen. Om du ändrar en så ändras det för alla.

- https://www.w3schools.com/java/java_modifiers.asp

## TODO

Det här är en början. Fortsättning följer!