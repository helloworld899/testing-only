## Syntax

    public class Main {
      public static void main(String[] args) {
        System.out.println("Hello World");
      }
    }

## Stora och små bokstäver

Ett Java-program börjar alltid med en klass som heter "Main" och en metod med namnet "main". Observera att Java är _case sensitive_, vilket betyder att det är viktigt och petigt med stor och liten bokstav. Om det inte är rätt så kommer du få felmeddelanden, ofta som säger något i stil med "du har använt dig av `persilja` vilket jag inte har någon aning om vad det är", när du kanske menade `Persilja`. Du och jag kanske tycker datorn är lite väl kinkig ibland, men i datorns värld så är dessa två ord helt olika ord som inte har någonting med varandra att göra.

## Kodblock och konstiga paranteser

Inom programmering använder vi ofta tecken som du kanske inte är vad vid annars. Exempelvis så avslutas en "instruktion" i Java med ett semikolon - `;`, som sista tecken i `System.out.println("Hello World");`.

Vanliga paranteser `(` och `)`används för att inkaplsa "argument" eller "parametrar". Exempelvis är `"Hello World"` en parameter till en metod som heter `System.out.println()` i `System.out.println("Hello World");`.

Mustaschparanterserna `{` och `}` används för att markera start och slut av så kallade "kodblock". I vårt exempel för Hello world ovan så finns det två kodblock. Kan du se dem?

Hakparanteserna `[` och `]` används ofta för _listor_ eller _arrayer_. Dessa kommer vi till senare.

Ibland kommer vi även använda `<` och `>`. Dessa har två funktioner. I ett sammahang är de precis som i matematiken "mindre än" och "större än", men de har även en till funktion som vi kommer till senare.

De mer formella namnen på dessa paranteser är enligt Wikipedia detta:

    (...) – rundparentes,[1] bågparentes, bågar eller bara parentes
    [...] – hakparentes[1] eller hård parentes
    {...} – fågelkrok, klammerparentes,[1] spetsparentes,[1] krullparentes, måsvingar eller ackolad

Har du något bättre namnförslag du vill dela med dig av?