# C++ Programming Exercises

This README file provides a collection of C++ programming exercises along with their implementations. Each program addresses a specific problem or task.

## Table of Contents
1. [Q1. Write a program that reads in two integers and determines and prints if the first is a multiple  of the second. 
](#1-multiple-check)
2. [Q2. Write a program that reads in the size of the side of a square and then prints a hollow square of that size out of asterisks and blanks.Your program should work for squares of all side sizes between 1 and 20.For example, if your program reads a size of 5, it should print
                 *****
                 *   *
                 *   *
                 *   *
                 *****                  ](#2-hollow-square)
3. [Palindrome Check](#3-palindrome-check)
4. [Exponent Calculation](#4-exponent-calculation)
5. [Rounding Numbers](#5-rounding-numbers)
6. [Greatest Common Divisor](#6-greatest-common-divisor)
7. [Towers of Hanoi](#7-towers-of-hanoi)
8. [Tokenize and Reverse](#8-tokenize-and-reverse)
9. [Complex Numbers](#9-complex-numbers)
10. [String Concatenation](#10-string-concatenation)
11. [Complex Number Enhancements](#11-complex-number-enhancements)
12. [Shape Hierarchy](#12-shape-hierarchy)
13. [Function Template](#13-function-template)
14. [Exception Handling](#14-exception-handling)
15. [Destructor Call Order](#15-destructor-call-order)
16. [Constructor Failure](#16-constructor-failure)

### 1. Multiple Check
```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;
    cout << "Enter two integers: ";
    cin >> a >> b;

    if (b == 0) {
        cout << "Cannot divide by zero." << endl;
    } else if (a % b == 0) {
        cout << a << " is a multiple of " << b << endl;
    } else {
        cout << a << " is not a multiple of " << b << endl;
    }

    return 0;
}

```


## 2. Hollow Square

**[Move Up](#table-of-contents)**




