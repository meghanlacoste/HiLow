package com.company;


import static com.company.ProjConstants.*;

public class HiLo {

    private int secretNumb = INVALID;

    private int guess = INVALID;

    private boolean higher;

    // serves as a demonstration of parameterized constructor with min and max as paramaters.

    public HiLo(int MIN, int MAX) {


    }

    public void setSecretNumb ( int randomNumb) {
        if ((randomNumb >= MIN) && (randomNumb <= MAX)) {
            secretNumb = randomNumb;
        }
    }

    public int getSecretNumb () {
        return secretNumb;

    }


    public void setGuess ( int userInput){
        if ((userInput >= MIN) && (userInput <= MAX)) {
            guess = userInput;
        }



    }

    public int getGuess (){

        return guess;

    }

    public void setHigher() {
        if ((getGuess() != INVALID) && (getSecretNumb() != INVALID)) {

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



