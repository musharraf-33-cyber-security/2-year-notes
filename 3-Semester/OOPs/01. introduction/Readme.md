# Object Oriented Programming in C++

## Overview

Object-oriented programming (OOP) uses objects in programming. The main aim of OOP is to implement real-world entities like inheritance, hiding, polymorphism, etc., in programming. It aims to bind together the data and the functions that operate on them so that no other part of the code can access this data except that function.

## Key Concepts of OOP

OOP is based on several fundamental concepts, which act as its building blocks:

1. **Class**: A blueprint for creating objects (a particular data structure), providing initial values for state (member variables or fields), and implementations of behavior (member functions or methods).

    **Example**:

    ```cpp
    class Car {
    public:
        int speed;
        int mileage;

        void applyBrakes() {
            // logic to apply brakes
        }
    };
    ```

    [Copy this code](#copy)

    [Run this code](#run)

2. **Objects**: Instances of classes. Objects hold data and can perform functions defined by their class.

    **Example**:

    ```cpp
    #include <iostream>
    using namespace std;

    class Person {
        char name[20];
        int id;

    public:
        void getDetails() {
            // logic to get details
        }
    };

    int main() {
        Person p1; // p1 is an object
        return 0;
    }
    ```

    [Copy this code](#copy)

    [Run this code](#run)

3. **Encapsulation**: The bundling of data and the methods that operate on that data within one unit, e.g., a class in C++. It restricts direct access to some of the object's components, which can prevent the accidental modification of data.

4. **Abstraction**: The concept of hiding the complex reality while exposing only the necessary parts. It helps in reducing programming complexity and effort.

5. **Polymorphism**: The ability of different objects to respond to the same function call in different ways. It allows one interface to be used for a general class of actions.

6. **Inheritance**: A mechanism by which one class can inherit the properties and methods of another class. It provides a way to create a new class using the properties and methods of an existing class.

7. **Dynamic Binding**: The code to be executed in response to a function call is determined at runtime.

8. **Message Passing**: Objects communicate with one another by sending and receiving information to each other. Messages (function calls) are sent to invoke behavior.

## Characteristics of an Object-Oriented Programming Language

OOP languages share several common characteristics, including but not limited to the above key concepts. They facilitate a modular approach to programming and make it easier to manage and modify complex systems.

## OOPS Concepts in C++

In C++, OOP is a paradigm that provides a clear modular structure for programs, making it good for defining abstract data types where implementation details are hidden. It emphasizes the following:

- **Class and Object creation**
- **Data Encapsulation and Abstraction**
- **Inheritance among classes**
- **Polymorphism through function overloading and operator overloading**

These concepts help in creating reusable code and reducing redundancy.

## Visual Representation

![OOP Concepts](image.png)

## Differences between Procedural and Object-Oriented Programming

### Procedural Programming

Procedural Programming can be defined as a programming model which is derived from structured programming, based upon the concept of calling procedures. Procedures, also known as routines, subroutines, or functions, simply consist of a series of computational steps to be carried out. During a program’s execution, any given procedure might be called at any point, including by other procedures or itself.

**Languages used in Procedural Programming**: FORTRAN, ALGOL, COBOL, BASIC, Pascal, and C.

### Object-Oriented Programming

Object-oriented programming can be defined as a programming model based upon the concept of objects. Objects contain data in the form of attributes and code in the form of methods. In object-oriented programming, computer programs are designed using the concept of objects that interact with the real world. Object-oriented programming languages are various but the most popular ones are class-based, meaning that objects are instances of classes, which also determine their types.

**Languages used in Object-Oriented Programming**: Java, C++, C#, Python, PHP, JavaScript, Ruby, Perl, Objective-C, Dart, Swift, Scala.

### Comparison

| **Procedural Oriented Programming**                                    | **Object-Oriented Programming**                                          |
|------------------------------------------------------------------------|--------------------------------------------------------------------------|
| In procedural programming, the program is divided into small parts     | In object-oriented programming, the program is divided into small parts  |
| called functions.                                                      | called objects.                                                          |
| Procedural programming follows a top-down approach.                    | Object-oriented programming follows a bottom-up approach.                |
| There is no access specifier in procedural programming.                | Object-oriented programming has access specifiers like private, public,  |
|                                                                        | protected, etc.                                                          |
| Adding new data and functions is not easy.                             | Adding new data and functions is easy.                                   |
| Procedural programming does not have any proper way of hiding data so  | Object-oriented programming provides data hiding so it is more secure.   |
| it is less secure.                                                     |                                                                          |
| In procedural programming, overloading is not possible.                | Overloading is possible in object-oriented programming.                  |
| In procedural programming, there is no concept of data hiding and      | In object-oriented programming, the concept of data hiding and           |
| inheritance.                                                           | inheritance is used.                                                     |
| In procedural programming, the function is more important than the     | In object-oriented programming, data is more important than function.    |
| data.                                                                  |                                                                          |
| Procedural programming is based on the unreal world.                   | Object-oriented programming is based on the real world.                  |
| Procedural programming is used for designing medium-sized programs.    | Object-oriented programming is used for designing large and complex      |
|                                                                        | programs.                                                                |
| Procedural programming uses the concept of procedure abstraction.      | Object-oriented programming uses the concept of data abstraction.        |
| Code reusability absent in procedural programming.                     | Code reusability present in object-oriented programming.                 |
| **Examples**: C, FORTRAN, Pascal, Basic, etc.                          | **Examples**: C++, Java, Python, C#, etc.                                |

## Functional Programming vs Object-Oriented Programming

### Functional Programming

In functional programming, we have to build programs using functions. An example of functional programming is the C language.

### Object-Oriented Programming

Object-oriented programming is built by using classes and objects. In this, we have concepts of encapsulation, inheritance, polymorphism, and data abstraction.

### Comparison

| **Functional Programming**                                             | **Object-Oriented Programming**                                          |
|------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Emphasizes the use of functions where each function performs a specific task | Based on the object-oriented concept where instances of objects are created |
| Fundamental elements used are variables and functions.                 | Fundamental elements used are objects and methods                        |
| Data in the functions are immutable (cannot be changed after creation) | Data used here are mutable data                                          |
| Importance is given to functions                                       | Importance is given to data rather than procedures                       |
| Follows a declarative programming model                                | Follows an imperative programming model                                  |
| Uses recursion for iteration                                           | Uses loops for iteration                                                 |
| Supports parallel object-oriented programming                          | Does not support parallel programming                                    |
| Statements do not need to follow a particular order while execution    | Statements need to follow an order i.e., bottom-up approach while execution |
| No access specifier                                                    | Has three access specifiers namely, Public, Private, and Protected       |
| Adding new data and functions is not easy                              | Provides an easy way to add new data and functions                       |
| No data hiding is possible. Hence, security is not possible            | Provides data hiding. Hence, secured programs are possible               |

### Conclusion

In the above article, we have covered functional programming and object-oriented programming and the difference between them. Both paradigms have their own advantages and are used according to the needs of the project. Languages like Python and Java support both paradigms, allowing flexibility in programming.

## Conclusion

OOP in C++ facilitates the creation of programs that are more modular, easier to maintain, and more intuitive to understand. By mastering these concepts, developers can build robust and scalable software applications.

---

## References

- [OOP Concepts](https://www.geeksforgeeks.org/object-oriented-programming-in-cpp/)
- [Detailed OOP in C++](https://www.javatpoint.com/cpp-oops-concepts)

---

Feel free to contribute to this repository by adding more examples or improving the explanations of the OOP concepts.
