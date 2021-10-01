# Kodäventyr #3: Metodiska tärningskast

I den här uppgiften vill jag ni använder er av de tre tekniker vi gått igenom nyligen, nämligen:

* array
* for-loopar
* metoder

## Uppgift

Den här uppgiften är baserad på tärningsspelet Yatzy.

* Par betyder två tärningar som visar samma sak
* Triss är tre tärningar som visar samma sak
* Fyrtal är när fyra tärningar visar samma sak
* Yatzy är när alla fem tärningar visar samma sak
* Två-par är två stycken par, som två tvåor och två femmor
* Kåk är en triss och ett par (exempelvis tre femmor och två fyror)

Skapa ett program som innehåller detta:

* En meny där användaren får två val
* * Det första valet är att kasta 5 tärningar
* * Det andra valet är att avsluta programmet
* * När användaren gjort ett val och den valda koden har körts, så ska användaren komma tillbaka till menyn
* Metod som heter `throwDie()`
* * Inga argument
* * Retunerar en integer som är ett slumpat tal mellan 1 och 6
* Metod som heter `throwMultipleDice()`
* * Syfte: Slumpa fram `numberOfDice` antal tal
* * Tar emot ett argument `int numberOfDice`
* * Retunerar en array av integers där varje element i arrayen är ett slumpat tal mellan 1 och 6. Antalet element (integers i detta fall) i arrayen är `numberOfDice`
* Metod som heter `sumNumbers()`
* * Syfte: Retunera summan av alla tal i arrayen du ger som argument till metoden
* * Tar emot ett argument som är en array av integers
* * Använder en for-loop för att räkna ut summan av alla integers i arrayen
* * Retunerar summan av alla element i arrayen
* Metod som heter `numberOfValue()`
* * Syfte: Retunera antalet av `searchingFor` i arrayen `arrayToSearch`
* * Tar emot två argument
* * Det ena argumentet är en integer som heter `searchingFor`
* * Det andra talet är en array av integers (förslagsvis tärningarna du kastat tidigare) som heter `arrayToSearch`
* * Retunera antalet `searchingFor`i arrayen `arrayToSearch` (se exempel nedan)

Hur spelet fungerar:

* Om användaren får två tärningar som visar samma värde (exempelvis två treor) ska användaren få ett meddelande om att de fått ett par
* Om användaren får tre tärningar som visar samma värde (exempelvis tre sexor) ska användaren få ett meddelande om att de fått triss
* Om användaren får fyra tärningar som visar samma värde (exempelvis fyra ettor) ska användaren få ett meddelande om att de fått fyrtal
* Om användaren får fem tärningar som visar samma sak får användaren YATZY
* För level-up (större utmaningar) se nedan

## Mer detaljer om metoden `numberOfValue()`

Om vi har en array som ser ut såhär:

    int myArray = {1, 2, 3, 3, 5};

Så ska den här koden...

    int numberOfThrees = numberOfValue(myArray, 3);

... göra att variabeln `numberOfThrees` innehåller talet `2`, då det är två treor i vår array.

## Level Up

Blir du klar och vill fortsätta testa svårare saker så gör en eller fler av följande:
* Om användaren får två stycken par får användaren två-par
* Om användaren får en triss och ett par får användaren kåk
* Om användaren får 1-5 blir det en låg stege
* Om användaren får 2-6 blir det en hög stege
* Poängen är baserad på vad användaren får (par, triss, kåk, et cetera) och vad dessa tal blir tillsammans totalt
* * Exempelvis ger ett par i femmor 10 poäng
* * Triss i treor ger 9 poäng
* * Kåk ger totalen av alla fem tärningar