Certainly! Below is a simple C++ program that accomplishes this task:

```cpp
#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    // Initialize the random number generator with the current time
    srand(static_cast<unsigned int>(time(0)));

    // Generate a random number between 1 and 100
    int secretNumber = rand() % 100 + 1;
    
    int guess = 0;
    int attempts = 0;

    std::cout << "Welcome to the Number Guessing Game!" << std::endl;

    while (guess != secretNumber) {
        std::cout << "Enter your guess (between 1 and 100): ";
        std::cin >> guess;
        attempts++;

        if (guess < secretNumber) {
            std::cout << "Too low! Try a higher number." << std::endl;
        } else if (guess > secretNumber) {
            std::cout << "Too high! Try a lower number." << std::endl;
        } else {
            std::cout << "Congratulations! You guessed the right number in " << attempts << " attempts." << std::endl;
        }
    }

    return 0;
}
```

This program uses the `rand()` function to generate a random number between 1 and 100. It then prompts the user to guess the number and provides feedback based on whether the guess is too high or too low. The program continues to prompt the user for guesses until they correctly guess the number. Once the correct number is guessed, the program displays the number of attempts it took to guess the number and ends.

You can compile and run this program in any C++ compiler to play the number guessing game.
