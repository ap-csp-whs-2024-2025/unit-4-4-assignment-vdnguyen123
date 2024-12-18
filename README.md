# unit-4-4-assignment

## To compile code
All code must be compiled before you can run it.  To compile means that you are converting your C++ code into a language that the computer can understand (e.g., binary).  To compile C++ code, run the following command in a terminal:
```
g++ fileName.cpp -o outFileName
```
This tells the C++ compiler to compile your file named `fileName.cpp`, and output it (`-o`) as a file named `outFileName`.

## To run code
After you have compiled the code, run your output file by running
```
./outFileName
```

## Compile and Run Example
Suppose I have a file named `classwork.cpp`.  I compile and run the file by doing
```
g++ classwork.cpp -o output
./output
```

## Problem 1
Prompt the user for a number from 1 to 100. Using a while loop, if they entered an invalid number, tell them the number entered is invalid and then prompt them again for a number from 1 to 100. If they enter a valid number - thank them for their input.

* Prompt the user for a number from 1 to 100
* While that number is less than 1 or that number is more than 100
* Output that they entered an invalid number
* Prompt them again for a number from 1 to 100
* Output to the user, thanking them for their input

## Problem 2
Prompt the user to guess your favorite color. Using a while loop, if the user didn't guess your favorite color [pick one for this activity] then tell them they are incorrect, then ask them again. Whenever they guess the color correctly, output that they are correct and how many guesses it took them.

* Create a variable and assign it the value of 1
* Prompt the user to guess your favorite color
* While their guess is not equal to your favorite color
* Tell them they are incorrect
* Prompt them to guess again
* Add one to the variable above
* Output to the user, they were correct and how many attempts it took using the variable
 

## Problem 3
Ask the user how many numbers for which they want to calculate the sum. Using a for loop, prompt the user to enter that many numbers, one-by-one, keeping track of the sum. At the end, after the user entered all numbers, output the sum.

* Create a variable and assign it the value of 0
* Prompt the user for how many numbers they have
* With a for loop, set it to repeat enough times to get all their values
* Prompt the user for a number
* Add that number to the variable that started as 0
* Output to the user, the sum of all values

# Sample Solution
```c++
#include <iostream>
#include <string>

int main()
{
    // Problem 1: Prompt the user for a number from 1 to 100
    int number;
    std::cout << "Please enter a number from 1 to 100: ";
    std::cin >> number;

    while (number < 1 || number > 100)
    {
        std::cout << "Invalid number entered. Please enter a number from 1 to 100: ";
        std::cin >> number;
    }
    std::cout << "Thank you for your input!" << std::endl;

    // Problem 2: Prompt the user to guess your favorite color
    std::string favoriteColor = "blue"; // you can change this to any color
    std::string guess;
    int attempts = 1;

    std::cout << "Guess my favorite color: ";
    std::cin >> guess;

    while (guess != favoriteColor)
    {
        std::cout << "Incorrect! Try again: ";
        std::cin >> guess;
        attempts = attempts + 1;
    }

    std::cout << "Correct! You guessed my favorite color in " << attempts << " attempt(s)." << std::endl;

    // Problem 3: Ask the user how many numbers they want to sum
    int numCount;
    int sum = 0;
    std::cout << "How many numbers would you like to sum? ";
    std::cin >> numCount;

    for (int i = 1; i <= numCount; i = i + 1)
    {
        int num;
        std::cout << "Enter number " << i << ": ";
        std::cin >> num;
        sum = sum + num;
    }

    std::cout << "The sum of all the numbers is: " << sum << std::endl;

    return 0;
}
```
