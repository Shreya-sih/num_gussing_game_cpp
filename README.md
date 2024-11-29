#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;
int main() {
    // Seed the random number generator
    srand(static_cast<unsigned int>(time(0)));
    // Generate a random number between 1 and 100
    int randomNumber = rand() % 100 + 1;
    int userGuess = 0;
    int attempts = 0;
    cout << "Welcome to the Number Guessing Game!" << endl;
    cout << "I have chosen a number between 1 and 100." << endl;
    cout << "Can you guess what it is? Let's begin!" << endl;
    do {
        cout << "Enter your guess: ";
        cin >> userGuess;
        if (userGuess < randomNumber) {
            cout << "Too low! Try again." << endl;
        } else if (userGuess > randomNumber) {
            cout << "Too high! Try again." << endl;
        } else {
            cout << "Congratulations! You guessed it right." << endl;
        }
        attempts++;
    } while (userGuess != randomNumber);
    cout << "You guessed the number in " << attempts << " attempts!" << endl;
    return 0;
}
