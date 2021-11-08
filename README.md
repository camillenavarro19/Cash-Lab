package com.company;

import javax.swing.*;
import java.util.Scanner;

public class Main {

    private static Scanner scan;

    public static void main(String[] args) {
        // write your code here
        Scanner input = new Scanner(System.in);

        System.out.print("Enter dollar amount (ex: 9.50): ");
        double amount = input.nextDouble();
        while (amount <=0)
        {
            System.out.print("Invalid input, please try again: ");
            amount = input.nextDouble();}

            int cents = (int)(amount * 100);

            int numofquarters = cents / 25;
            cents = cents % 25;

            int numofdimes = cents / 10;
            cents = cents % 10;

            int numofnickels = cents / 5;
            cents = cents % 5;

            int numofpennies = cents;
            System.out.println("Your dollar amount " + amount + " has \n"
                    + numofquarters + " quarters\n"
                    + numofdimes + " dimes\n"
                    + numofnickels + " nickels\n"
                    + numofpennies + " pennies");
        }
    }
