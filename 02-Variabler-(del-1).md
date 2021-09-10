I Java finns många olika sorters variabler. Här är några exempel av variabler av olika "datatyper":

    int myNum = 5;
    float myFloatNum = 5.99f;
    char myLetter = 'D';
    boolean myBool = true;
    String myText = "Hello";

Alla dessa är så kallade "primitiva datatyper" med undantaget String, som inte är en primitiv datatyp. Det kommer vi prata om mer senare.

En i taget:

* En `int` är en "integer", även kallat ett heltal, som siffran 1, 24, 4829 eller -127
* En `float` är ett tal med decimaler, exempelvis 0.12, 3.14159 eller 1.0, och deklareras med bokstaven "f" efter (se ovan)
* En `char` är ett enda tecken eller bokstav, så som D, K eller ett utropstecken, och det tecknet skrivs inom "enkelfnuttar": `'`
* En `boolean` har ett värde som antingen är sant eller falskt, inget annat. Dessa kallas `true` eller `false`.
* En `String` är en sträng med tecken, allt från en tom sträng "", till något längre meddelande "Här är en lite längre sträng med tecken!". Dessa strängar skrivs till skilnad från `char` inom "dubbelfnuttar": `"`

Observera att alla typer ovan skrivs med små bokstäver utom just "String". Anledningen till detta kommer senare, just nu behöver du bara veta att "det är så".

Vad vi också kan se är ordningen orden ovan kommer i. Exempel:

    int myNum = 5;

Första ordet är vilken typ det är (en integer). Andra ordet är namnet på variabeln. Sen kommer ett likamedtecken. Efter det kommer värdet variabeln har (5), och i slutet av raden kommer ett semikolon (;).

I talat språk säger vi att vi **"deklarerar variabeln myNum av typen integer med värdet 5"**.

Det finns fler sorters variabler, och fler sorters integers, men de sparar vi till senare i kursen.

## Övning

Experimentera med de olika datatyperna. Ta exemplet från vår Hello World och skriv om det.

Originalet:

    System.out.println("Hello world");

Med en variabel:

    String myVariable = "Hello world";
    System.out.println(myVariable);

Testa deklarera fler variabler och skriv ut dem med `System.out.println()`. Vad gör denna kod, och vad är det som händer?

    int favoritsiffra = 489;
    String namn = "Batman";
    
    System.out.println("En person vid namn " + namn + " har favoritnumret " + favoritsiffra);

## Övning 2

Skriv ett program som skriver ut följande:

    Förnamn: förnamn
    Efternamn: efternamn
    Fullständigt namn: förnamn efternamn
    Ålder: 30
    Mening: Jag heter förnamn efternamn och jag är så här gammal: 200!

Ett nästan komplett lösningsförslag, eller inspiration, finns här: https://gist.github.com/zocom-bjorn-pettersson/da1330537635e85ff660c304a53ad608

### Övning 2: Tips

Gör en variabel `firstName` av typ `String` som har ditt förnamn som värde.
Gör en variabel `lastName` av typ `String` som har ditt efternamn som värde.
Gör en variabel av typ `int` som har din ålder som värde.
Skriv ut ditt fullständiga namn genom att använda `System.out.println(firstName + " " + lastName);`.

## Att ändra ett värde

Efter att ha deklarerat en variabel kan vi ge den ett nytt värde utan att nämna datatypen igen.

Exempelvis skriver detta...

    int myNumber = 10;
    myNumber = 12;

    System.out.println(myNumber);

... ut samma sak som detta:

    int myNumber = 12;
    
    System.out.println(myNumber);

Däremot kan du inte byta datatyp senare. Vad får du för felmeddelande om du försöker köra den här koden nedan?

    int myNumber = 12;
    myNumber = "Tolv";
    
    System.out.println(myNumber);

## Något att klura på

* Varför använder vi variabler?
* Varför får vi inte ändra datatyp (som siffran 12 till strängen "Tolv" ovan)?

### Stora tal

2 000 000 000, eller två miljoner miljarder, är ett stort tal. Enligt matematikens alla regler så är den här uträkningen rätt:

    2 000 000 000 * 2 = 4 000 000 000

Eller hur? Men vad händer om du försöker räkna ut det i Java? Blir resultatet vad du förväntade dig? Om inte, varför inte?

Notera att i Java så måste tal skrivas ihop utan mellanslag, men för att göra det mer läsbart kan du använda tecknet `_` mellan siffrorna:

    int aBigNumber = 2_000_000_000;
    System.out.println(aBigNumber * 2);

## Glosor

* variabel
* deklarera
* värde
* datatyp
* integer
* float
* char
* boolean
* String

## Se även

* Fler beskrivningar och övningar finns här: https://www.w3schools.com/java/java_variables.asp