Här samlar vi lite kodsnuttar som snabbt ger dig ett ställe att starta på.

## Slumpa tal

Importera bibliotek:

    import java.util.Random;

Slumpa tal:

    Random myRandom = new Random();
    int dice_value = myRandom.nextInt(5) + 1;

I detta exempel får du ett tal mellan 1 och 6. `5` i `.nextInt(5)` är maxtalet och det lägsta talet är per automatik 0. I det här exemplet gör den alltså dig ett tal mellan 0 och 5 som adderar 1 till.


## Läsa användardata

Till detta använder vi Scanner:

        import java.util.Scanner;  // Import the Scanner class

        class Main {
          public static void main(String[] args) {
            Scanner myScanner = new Scanner(System.in);  // Create a Scanner object
            System.out.println("Enter username");

            String userName = myScanner.nextLine();  // Read user input
            System.out.println("Username is: " + userName);  // Output user input
          }
        }


Mer information: https://www.w3schools.com/java/java_user_input.asp