## Kodäventyr #06 - Objekt i butik 

Vi fortsätter att öva med objekt, och använder klasser som vi introducerat under den här veckan.

Material: Wikin, lektionsinspelningar, youtube och internet. Och varandra, förstås!

Det används många nya ord här nere. Alla de orden har jag gått igenom på föreläsningen och finns även under sidan "Glosor" på wikin.

## Uppgift

Innan du börjar på det här kodäventyret så vill jag att du gör detta:

- Skapa ett konto på GitHub om du inte redan har det
- Gå in på Wikin (denna wiki) och stjärnmarkera det här repot (uppe i högra hörnet)
- Installera GitHub Desktop (https://desktop.github.com/)
- När du är klar vill jag att du ska ha laddat upp din kod i ett publikt (ej privat) repo på GitHub (se video från 2021-10-15) (Har du jätteproblem med Git löser vi det i klassrummet nästa vecka)

### Filer (dina klasser)

* Skapa ett nytt projekt i IntelliJ och kalla det för `MyShop`. Kryssa inte i rutan för att skapa projekt.
* Skapa en ny klass i mappen `src/` och kalla den klassen för `MyShop`
* Skapa en ny klass i mappen `src/` och kalla den klassen för `Product`
* Skapa en ny klass i mappen `src/` och kalla den `Main`

### Vad programmet ska göra

Du ska göra ett program som innehåller detta:

- Det är en affär där du får köpa konstiga saker
- En meny där användaren får lista alla saker som finns i affären - det som ska skrivas ut är namnet på saken och vad den kostar (ej beskrivningen)
- Användaren ska kunna lägga saker i sin kundkorg
- Användaren ska kunna fråga hur mycket alla saker i kundkorgen kostar
- Användaren ska kunna ta bort saker från kundkorgen
- Användaren ska kunna fråga butiksägaren om beskrivning av en specifik produkt
- Det ska vara tydligt för en ny användare hur programmet fungerar och vad som förväntas skrivas in

Gällande koden så vill jag se detta:

- Menyn ska skrivas ut i en egen metod som heter `printMenu()`
- När du läser in en information från användaren ska du använda metoderna `getUserString` och `getUserInt`
- En metod som heter `getUserString` som retunerar en Sträng
- En metod som heter `getUserInt` som retunerar en int (se exempel från video 2021-10-14)
- Deklarera din `ArrayList` i klassen (`MyShop`), och ej i metoderna (se video 2021-10-15)
- Deklarera dina `Scanner` i metoderna, och inte i klassen. Scanner ska endast finnas med i metoderna `getUserString` och `getUserInt`. Detta är i klassen `MyShop`.

### Metoder

#### Klassen Main

* Klassen `Main` ska ha en `main`-metod: Det är här ditt program startar. Det enda du behöver i main-metoden är detta:

```java
MyShop shop = new MyShop();
shop.start();
```

#### Klassen MyShop

Resten av logiken finns i klassen MyShop, inklusive menyn.

Klassen `MyShop` ska...

* ... **inte** ha en `main`-metod, för det här är bara en klass som används av andra klasser
* ... Ha en `ArrayList` som innehåller flera objekt av typen `Product`
* Din meny och övriga metoder, som metoden `start()` där du nog vill ha din while-loop (`while (programRunning)` eller vad du nu vill använda)

#### Klassen Product

Klassen `Product` ska...

* ... ska ha minst tre "attribut" ("klassvariabler"): Namn ("name"), Pris ("price"), beskrivning ("description")
* ... ska ha en "construktor" ("konstruktor" på svenska) som tar tre argument: Namn, pris och beskrivning
* ... Encapsulation: en "getter" och en "setter" för varje attribut (setName/getName, setPrice/getPrice, setDescription/getDescription, et cetera)

### Level Up (gör en eller fler av dessa)

- Om användaren frågar om en produkt som inte finns så ska butiksägaren fråga "Jag vet inte vad X är, menade du Y?" där X är vad användaren skrivit in och Y är en slumpad sak som finns i butiken
- Lägg till kvantitet - hur många av varje produkt finns det? Om användaren köper en banan så ska antalet bananer minska med ett
- Om det inte finns några bananer kvar så ska kunden inte kunna lägga fler sådana i korgen
- Lägg till plånbok - se till att en kund inte kan köpa mer än vad de har i plånboken
- Titta på dina gamla kodäventyr och se hur du skulle ändra på dem idag. Skapa nya projekt (skriv inte över den gamla koden) och försök göra de gamla kodäventyren igen.
- Det viktigaste med LinkedList och HashSet är att du vet om att de finns och ungefär hur de fungerar, så att om du i framtiden stöter på ett problem så vet du att de sakerna finns och kan kolla upp dem vid behov.

### Vidare uppgifter (om du är klar med det andra)

#### Git

Läs på om git, kolla YouTube och leta efter introduktioner. Om du hittar en bra video dela med dig av den på Discord till dina klasskamrater.

#### Bash

Vi har pratat lite kort om Linux i klassrummet den här veckan, och inte gått på några djupare detaljer. Det kommer längre presentationer senare under kursen.

Bash är något du kommer använda mycket i framtiden när du jobbar med Linux-maskiner.

Bash är ett så kallat "skal", eller "shell". Det är ett textbaserat användargränssnitt som används i terminaler.

Om du kör Windows och installerat Git via IntelliJ så har du ett program som heter git-bash. Om du startar det kommer du till en terminal med ett bash-skal.

Om du kör Mac så har du redan ett program som heter Terminal. Om du skriver kommandot `echo $SHELL` får du se vilket skal du kör - det kan vara zsh eller något annat än bash. `zsh` och `bash` har många likheter, men också en del olikheter. Du ska fortfarande kunna följa många introduktionsvideos du hittar på YouTube och andra platser. Frågor tar vi i klassrummet nästa vecka - det är mycket lättare att visa där.

Om du är klar med grunduppgiften (med eller utan Level-Ups) så kolla YouTube efter introduktioner till bash och till shellscripting.