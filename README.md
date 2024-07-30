# Guess_Numbering_Game

// Project :- Number Guessing Game

#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main(){
    int number,guess,nguesses=1;
    srand(time(0));
    number=rand()%100 + 1;
    // printf("The number is %d",number);

    do{
        printf("Guess the number between 1 and 100\n");
        scanf("%d",&guess);
        if(guess>number){
            printf("Lower number please!\n");
        }
        else if(guess<number){
            printf("Greater number please!\n");
        }
        else{
            printf("You guessed it in %d attempts\n",nguesses);
        }
        nguesses++;
    }while(number!=guess);
    return 0;

}
