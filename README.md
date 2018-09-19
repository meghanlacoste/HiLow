package com.company;

/**
 * Created by 13549lac on 19/09/2018.
 */

import static com.company.ProjConstants.*;
public class HiLo {

    private int secretNumb = INVALID; private int guess = INVALID; private boolean higher;

    public HiLo(int i, int i1) {
    }

    public void setSecretNumb ( int randomNumb) {
        if (randomNumb >= MIN && randomNumb <= MAX) {
            secretNumb = randomNumb;
        }
    }

    public int getSecretNumb () {
        return secretNumb;

    }


    public void setGuess ( int userInput){
        if (userInput >= MIN && userInput<= MAX) {
            guess = userInput;
        }



    }

    public int getGuess (){

        return guess;

    }

    public void setHigher () {
        if (getGuess()!= INVALID && getSecretNumb()!= INVALID) {

            if (guess < secretNumb) {
                higher = true;
            }
            else {
                higher = false;
            }// end if guess < secretNumb


        } // end if not valid
        else {
            System.out.print("\n INVALID");
        }
    } // end method setHigher


    public boolean getHigher () {
        return higher;
    }
} // end HiLow Class
