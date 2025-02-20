/**
 *Description:Group project
 * Designed print the first letter of the users name.
 *@author Michael Polk
 *@since Feb 17 2025
 */

import java.util.Scanner;

public class Conversion {

    private static final double YEN_TO_USD_RATE = 0.0066;

    public static void welcome() {
        System.out.println("++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++");
        System.out.println("This program converts Japanese Yen to US Dollars.");
        System.out.println("To use it, enter a value in Yen when prompted.");
        System.out.println("I hope you enjoy using my program and find it useful.");
        System.out.println("Now let's begin!");
        System.out.println("++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++");
    }

    public static double Yen2Dollar(double amountInYen) {
        return amountInYen * YEN_TO_USD_RATE;
    }

    public static int menu(Scanner in) {
        System.out.println("1. Yen to US Dollars");
        System.out.println("2. End the program");
        System.out.print("Enter your option: ");
        int option = in.nextInt();
        return option;
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int option;
        double amount;
        double convertedAmount;

        welcome();
        option = menu(in);

        switch (option) {
            case 1:
                System.out.print("Enter the amount in Japanese Yen: ");
                amount = in.nextDouble();
                convertedAmount = Yen2Dollar(amount);
                System.out.println(amount + " yen is equal to " + convertedAmount + " US Dollars.");
                break;

            case 2:
                System.out.println("Goodbye.");
                break;

            case 3:
                System.out.println("Invalid option.");
                break;
        }

            in.close();
        }
    }
