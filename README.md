# HiLow
package com.company;

import static com.company.ProjConstants.*;
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) {
        // write your code here


        //Create a new object (High-Low Class)
        highLow calcHL = new highLow();


        int userInput = INVALID;

        Boolean higher;


  //Generate Random number between 1 - 100 and set to secretNumb

        Random rand = new Random();

        int secretNumb = rand.nextInt(MAX) + MIN;

       calcHL.setSecretNumb(secretNumb);


//Set secretNumb to the SecretNumb in the highLow Class


        while (userInput != secretNumb) {


                System.out.print("\nEnter an integer between 1 and 100\n");
                Scanner s = new Scanner(System.in);

                if (s.hasNextInt()){

                    userInput = s.nextInt();

                    if (userInput >= MIN && userInput <= MAX)  {
                        if (userInput!= secretNumb){

                            calcHL.setGuess(userInput);

                            calcHL.setHigher();

                            higher = calcHL.getHigher();


                            if (higher) {

                                System.out.print("\n higher \n");

                            } else {

                                System.out.print("\n lower \n");
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
