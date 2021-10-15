# Kodäventyr #5 - ArrayList

Vi fortsätter att öva med metoder, och använder ArrayList som vi introducerat under den här veckan.

## Uppgift

Innan du börjar på det här kodäventyret så vill jag att du gör detta:

- Skapa ett konto på GitHub om du inte redan har det
- Gå in på Wikin (denna wiki) och stjärnmarkera det här repot (uppe i högra hörnet)
- Installera GitHub Desktop (https://desktop.github.com/)
- När du är klar vill jag att du ska ha laddat upp din kod i ett publikt (ej privat) repo på GitHub (se video från 2021-10-15) (Har du jätteproblem med Git löser vi det i klassrummet nästa vecka)

Du ska göra ett program som innehåller detta:

- En meny där användaren får skapa en lista över sina favoritsaker (eller något annat roligt)
- Användaren ska kunna lägga till nya saker i listan
- Användaren ska kunna ta bort saker från listan
- Användaren ska kunna visa hela listan
- Användaren ska kunna ändra på en specifik sak i listan
- Det ska vara tydligt för en ny användare hur programmet fungerar och vad som förväntas skrivas in

Gällande koden så vill jag se detta:

- Menyn ska skrivas ut i en egen metod som heter `printMenu()`
- När du läser in en information från användaren ska du använda metoderna `getUserString` och `getUserInt`
- En metod som heter `getUserString` som retunerar en Sträng
- En metod som heter `getUserInt` som retunerar en int (se exempel från video 2021-10-14)
- Deklarera din `ArrayList` i klassen, och ej i metoderna (se video 2021-10-15)
- Deklarera dina `Scanner` i metoderna, och inte i klassen. Scanner ska endast finnas med i metoderna `getUserString` och `getUserInt`

Level up (gör en eller fler av dessa):

- Använd dig av HashMaps också. Kanske för att betygsätta filmer? Eller för att skriva in hur många paket flingor användaren har i skafferiet. Om det är svårt att få in det i det här programmet så skriv ett nytt program och använd det där.
- Experimentera med LinkedList
- Experimentera med HashSet
- Titta på dina gamla kodäventyr och se hur du skulle ändra på dem idag. Skapa nya projekt (skriv inte över den gamla koden) och försök göra de gamla kodäventyren igen.
- Det viktigaste med LinkedList och HashSet är att du vet om att de finns och ungefär hur de fungerar, så att om du i framtiden stöter på ett problem så vet du att de sakerna finns och kan kolla upp dem vid behov.

### Vidare uppgifter (om du är klar med det andra)

#### Java

Skapa en LinkedList och spara integers i dem. Skapa metoder som gör följande:

- Räknar ut totalen av alla integers i listan
- Räknar ut median av alla integers i listan
- Räknar ut medelvärdet av alla integers i listan

Eller om du vill göra andra matterelaterade uppgifter:
- Räknar ut hypotenusan av en triangel

#### Git

Läs på om git, kolla YouTube och leta efter introduktioner. Om du hittar en bra video dela med dig av den på Discord till dina klasskamrater.

#### Bash

Vi har pratat lite kort om Linux i klassrummet den här veckan, och inte gått på några djupare detaljer. Det kommer längre presentationer senare under kursen.

Bash är något du kommer använda mycket i framtiden när du jobbar med Linux-maskiner.

Bash är ett så kallat "skal", eller "shell". Det är ett textbaserat användargränssnitt som används i terminaler.

Om du kör Windows och installerat Git via IntelliJ så har du ett program som heter git-bash. Om du startar det kommer du till en terminal med ett bash-skal.

Om du kör Mac så har du redan ett program som heter Terminal. Om du skriver kommandot `echo $SHELL` får du se vilket skal du kör - det kan vara zsh eller något annat än bash. `zsh` och `bash` har många likheter, men också en del olikheter. Du ska fortfarande kunna följa många introduktionsvideos du hittar på YouTube och andra platser. Frågor tar vi i klassrummet nästa vecka - det är mycket lättare att visa där.

Om du är klar med grunduppgiften (med eller utan Level-Ups) så kolla YouTube efter introduktioner till bash och till shellscripting.