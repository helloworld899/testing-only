# Kodäventyr #1: Tärningskastet

Er första hemuppgift.

Den här uppgiften kommer ni göra individuellt (alla ska göra den), men ni får gärna prata med varandra om hur ni löser den, och visa varandra er kod. Jag tipsar om att ni skärmdelar på Discord under måndag och tisdag.

Ni kommer under fredagen (när denna uppgift delas ut) delas in i grupper om tre. Ni tre ska checka in med varandra under måndag och tisdag, både på förmiddag (exempelvis kl 10) och igen på eftermiddagen (exempelvis kl 15). Det här är inget formellt krav, utan ett sätt för er att lära känna varandra, och något som jag tror kommer ge er mycket i utbildningen.

Det ni kan prata om vid dessa tillfällen är saker som:
* Förstår ni uppgiften?
* Vet ni vad ni ska göra?
* Är det något som känns lätt?
* Är det något som känns svårt?

Och på eftermiddagen:
* Hur har det gått idag? Vad har jag stött på eller löst för problem?
* Vad har ni lärt er idag? Även de minsta småsaker räknas!

## Redovisning

På onsdag när den här uppgiften ska vara klar så kommer ni presentera för varandra i mindre grupper. Jag kommer kolla läget med alla, se hur det har gått för er, och höra vad ni har för frågor.

Den här uppgiften är inte betygsgrundande.

## Errata - ett fel har hittats sedan i fredags

Denna rad som var med i fredags:

    int dice_value = myRandom.nextInt(5) + 1;

Ska egentligen vara så här:

    int dice_value = myRandom.nextInt(6) + 1;

Annars kommer ni aldrig på upp siffran 6.

Detta uppdaterades nedan måndag morgon.

## Uppgiften

Skapa ett nytt projekt i IntelliJ, i stil med instruktionen här, men med små ändringar:
* https://github.com/zocom-bjorn-pettersson/CAWS21/wiki/99-IDE,-IntelliJ-IDEA#starta-ditt-f%C3%B6rsta-projekt

Ändringar från den instruktionen:
* Project name: **AdventureDice**
* Base Package: **se.jensen.caws21.adventuredice**

**De exakta namnen är viktiga.**

Ersätt sedan hela filen med texten nedan:

    package se.jensen.caws21.adventuredice;
    
    /* Importera biblioteket som behövs för att generera slumpade tal */
    import java.util.Random;
    
    public class Main {
        public static void main(String[] args) {
            System.out.println("Kodäventyr #1: Tärningskast");
    
            /* Dessa två rader genererar ett tal mellan 1 och 6. Exakt hur kommer vi prata om senare. */
            Random myRandom = new Random();
            int dice_value = myRandom.nextInt(6) + 1;
    
            /* Ta bort de fem raderna nedan och ersätt dem med följande:
             * o Deklarera en variabel "points" av typen integer med värde 0, denna kommer användas för att räkna poäng
             * o Lägg till flera if-satser som gör olika jämförelser med variabeln dice_value (deklarerad ovan):
             *   o Om det är siffran 1 får du 1 poäng,
             *   o om du får siffran 2 får du tärningens värde delat med 2 poäng
             *   o om du får siffran 3 får du tärningens värde multiplicerat med 2 poäng
             *   o om du får siffran 4 får du tärningens värde plus 10 minus 5 poäng
             *   o om du får siffran 5 får du tärningens värde gånger tärningens värde poäng
             *   o om du får siffran 6 får du 0 poäng och uppmuntras med ett textmeddelande att kasta igen
             * o Efter detta så skriver du ut hur många poäng spelaren fick. Fick de under 10 poäng har de har de förlorat, fick de 10 poäng eller över så har de vunnit
             * o Level up: Om du blir klar och vill utmana dig kan du även göra följande:
             *   o Om talet är udda dubbla poängen (tips: du kan använda dig av "modulus", "%").
             *   o Ersätt if-satserna med en switch-sats
             *
             * Läsvärt:
             * Allt du behöver finns på dessa sidor:
             * o https://github.com/zocom-bjorn-pettersson/CAWS21/wiki/00-Javas-syntax
             * o https://github.com/zocom-bjorn-pettersson/CAWS21/wiki/01-Hej-V%C3%A4rlden
             * o https://github.com/zocom-bjorn-pettersson/CAWS21/wiki/02-Variabler-(del-1)
             * o https://github.com/zocom-bjorn-pettersson/CAWS21/wiki/03-Villkor-(if-else)
             * o https://www.w3schools.com/java/java_variables.asp
             * o https://www.w3schools.com/java/java_conditions.asp
             * o https://www.w3schools.com/java/java_operators.asp
             * 
             * Extra tankar och övningar finns här:
             * o https://github.com/zocom-bjorn-pettersson/CAWS21/wiki/%C3%96vningar
             * o https://github.com/zocom-bjorn-pettersson/CAWS21/wiki/99-Tips-och-godsaker
             * o https://github.com/zocom-bjorn-pettersson/CAWS21/wiki/Studieteknik
             */
    
            /* Ändra koden under denna rad */
            if (dice_value == 1) {
                System.out.println("Tärningen visar siffran 1! Du vinner!");
            } else {
                System.out.println("Tärningen visar siffran " + dice_value + " - tyvärr vinner du inte. Testa köra programmet igen?");
            }
        }
    }

