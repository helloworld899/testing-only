Här är en lista på ord ni behöver förstå:

## Grundläggande Java

* variabel
* deklarera
* värde
* datatyp
* integer
* float
* char
* boolean
* String

## Kod i meningar på Svenska

```java
int myInteger = 5;
```

Vi deklarerar en variabel som heter `myInteger` av typen `int` som har värdet `5`.

```java
public static String getString() {
    return "Hello.";
}
```

En publik, statisk metod som heter `getString()` och retunerar en Sträng.

```java
public static void doSomething() {
    // code goes here...
}
```

En publik, statisk metod som heter `doSomething()` som inte retunerar något.

## Verktyg, ramverk och tillhörande begrepp

- Framework: Ett "ramverk", någonting vi använder när vi programmerar som gör mycket av jobbet åt oss
- Beroenden/dependencies: Saker vårt projekt är beroende av. Exempelvis `java.util.Scanner` eller `java.util.Random`. Vissa beroenden är en del av Java. Vissa andra beroenden måste vi importera med andra verktyg, som Maven. Ett beroende som vi importerar i det här kodäventyret är `org.junit.jupiter`.
- Maven: Ett ramverk som bland annat tar hand om vårt projekts beroenden (som JUnit)
- JUnit: Ett test-ramverk som inte är en del av grundpaketen i Java, och därför behöver importeras med Maven
- Assert: Engelska för "försäkra", som i "Försäkra oss att `add(7,3)` ger tillbaka siffran 10". Om svaret är något annat så misslyckas testet. Om det är det vi förväntar oss så passerar testet.

## Versionshantering med Git

### Förtydliganden

- GitHub är ett företag som låter dig ha dina Git-repon där. GitHub lägger till funktionalitet i form av Issues, Wiki, hantering av "Pull requests" och dylikt
- Git är ett verktyg utvecklat av de som arbetat med Linux-kärnan, med syfte att ersätta andra versionshanteringssystem som SVN ("Subversion") och CVS.
- GitHub Desktop är ett program för att hantera dina lokala git-repon du har på din dator, och hjälper dig skicka upp dina ändringar till GitHub så andra kan se dem. Hjälper dig även se Issues och andra saker.
- git-bash är vad IntelliJ använder i bakgrunden på Windows för att göra git-grejer. Du kan även starta det programmet själv och använda git som det ursprungligen var tänkt att användas - på kommandoraden och inte med ett grafiskt program som GitHub Desktop.

### Git-specifikt

- clone: Att klona ett repo är att göra en första kopia av det
- fork: En separat vidareutveckling av ett projekt
- commit: En ändring. Kan vara en eller flera filer, och det kan vara enskilda rader
- commit message: Ett commit-meddelande, en kort kommentar som beskriver ändringen
- pull: Att ladda ner commits
- push: Att ladda upp commits
- fetch: Laddar ner uppdateringar men "applicerar" dem inte. Detta är inte ett jättevanligt kommando.
- merge: När ändringar har skett på flera ställen samtidigt måste vi få dem att fungera tillsammans. Ibland görs detta utan konflikt, och ibland med konflikter om både du och någon annan har ändrat på precis samma ställe.
- rebase: Två syften. 1) Att ändra i sina commits, exempelvis byta ordning på dem innan du laddar upp dem. 2) Att vid en `pull` lägga sina ändringar åt sidan, lägga på ändringarna du laddat ner, och sedan lägga på de commits du har lokalt men inte laddat upp än
- origin: Där repot bor, under denna kurs på GitHub. Git är ett decentraliserat program vilket betyder att koden kan bo på flera ställen.
- remote: Oftast "origin", kan även vara en annan plattform annat än GitHub