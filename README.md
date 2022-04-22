# Guess-the-number-
#include<stdio.h>
#include<stdlib.h>
#include<time.h>

    int main()
    {
        int number, guess,nguess=1;
        srand(time(0));
        number=rand()%100 + 1; //generate random number between 1 to 100
       // printf("The number is %d",number);
        
        //keep running the loop until the umber is guessed
        
        do{
            printf("Guess the number between 1 to 100 \n");
            scanf("%d",&guess);
            if(guess>number)
                printf("Lower number please !\n");
            else if(guess<number)
                printf("Higher number please !\n");
            else
            {
                printf("You win\n");
                printf("You guessed in %d attempts",nguess);
            }
            nguess++;
        }while(guess!=number);
        
        return 0;
    }
