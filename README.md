# Guess-the-word-game-
C program
#include <stdio.h>
#include <string.h>

int main() {
    char secretWord[] = "apple";
    char guess[20];
    int attempts = 5;

    printf("=== Guess the Word Game ===\n");
    printf("Hint: It's a fruit 🍎\n");

    while (attempts > 0) {
        printf("\nEnter your guess: ");
        scanf("%s", guess);

        if (strcmp(guess, secretWord) == 0) {
            printf("🎉 Congratulations! You guessed the word correctly.\n");
            break;
        } else {
            attempts--;
            printf("❌ Wrong guess. Attempts left: %d\n", attempts);
        }
    }

    if (attempts == 0) {
        printf("\n😢 Game Over! The correct word was: %s\n", secretWord);
    }

    return 0;
}
