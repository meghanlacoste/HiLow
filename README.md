# HiLow
package com.company;

import static com.company.ProjConstants.*;
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) {
	// write your code here

        // Creates a new object from HiLo Class which has the minimum and maximum parameters. This would
        // allow one to use the minimum and maximum values from the main class in the HiLo class, even though
        // the ProjConstants class used already fulfills such.

        HiLo calcHL = new HiLo(MIN, MAX);


        int userInput = INVALID;
        Boolean higher;

        Random rand = new Random();

        //   Generate Random number between 1 - 100 and set to secretNumb
        int secretNumb = rand.nextInt(MAX) + MIN;

        //  Set secretNumb to the SecretNumb in the HiLo Class
        calcHL.setSecretNumb(secretNumb);


        while (userInput != secretNumb) {


            System.out.print("\nEnter an integer between 1 and 100: ");
            Scanner s = new Scanner(System.in);

            if (s.hasNextInt()){

                userInput = s.nextInt();

                if (userInput >= MIN && userInput <= MAX)  {
                    if (userInput!= secretNumb){

                        calcHL.setGuess(userInput);
                        // Call on the setHigher method from the HiLo Class

                        calcHL.setHigher();

                        higher = calcHL.getHigher();


                        if (higher) {

                            System.out.print("\n higher than " + userInput + "\n");

                        } else {

                            System.out.print("\n lower than " + userInput + "\n");
                        }


                    } else {

                        System.out.print("Correct! The secret number was: " + secretNumb +"\n\n");

                    }


                } else {
                    System.out.print("That is not within the bounds of 1-100");
                }


            } else {
                System.out.print("\n That is not an integer value, try again");
            }


        } // end while guess isnt correct




    } // end main method
} // end main class
