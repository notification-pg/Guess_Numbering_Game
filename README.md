# Guess_Numbering_Game

// Project :- Number Guessing Game

#include<stdio.h>
#include<stdlib.h>   // this is for generating random number
#include<time.h>

int main()  {
    int number, guess, nguesses=1;
    srand(time(0));
    number = rand()%100 + 1;       // Generates a random number between 1 and 100
    printf("The number is %d\n", number);

    // keep running the loop until the number is guessed
    do
    {
        printf("Guess the number between 1 to 100\n");
        scanf("%d\n", &guess);

        if (guess>number)   {
            printf("Lower Number please!\n");
        }else if (guess<number) {
            printf("Higher Number please!\n");
        }else   {
            printf("You guessed it in %d attemps \n", nguesses);
        }
        nguesses++;

    } while(guess!=number);
    
    return 0;
}
