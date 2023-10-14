# Practice
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    // Seed the random number generator with the current time
    srand(time(0));
    int randomNumber = (rand() % 100) + 1;
    int userGuess;
    int attempts = 0;

   printf("Welcome to the Number Guessing Game!\n");
    printf("I've selected a random number between 1 and 100. Try to guess it!\n");

   do {
        printf("Enter your guess: ");
        scanf("%d", &userGuess);
        attempts++;

   if (userGuess < randomNumber) {
            printf("Too low. Try again.\n");
        } else if (userGuess > randomNumber) {
            printf("Too high. Try again.\n");
        } else {
            printf("Congratulations! You've guessed the correct number, which is %d\n", randomNumber);
            printf("You took %d attempts to guess the number.\n", attempts);
        }
    } while (userGuess != randomNumber);

   return 0;
}
