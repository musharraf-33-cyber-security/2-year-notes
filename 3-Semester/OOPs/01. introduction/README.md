# Object Oriented Programming in C++

## Overview

Object-oriented programming (OOP) uses objects in programming to implement real-world entities like inheritance, hiding, polymorphism, etc. It aims to bind together the data and the functions that operate on them so that no other part of the code can access this data except that function.

## Key Concepts of OOP

### Class

A blueprint for creating objects (a particular data structure), providing initial values for state (member variables or fields), and implementations of behavior (member functions or methods).

### Object

Instances of classes. Objects hold data and can perform functions defined by their class.

### Encapsulation

The bundling of data and the methods that operate on that data within one unit, e.g., a class in C++. It restricts direct access to some of the object's components, which can prevent the accidental modification of data.

### Abstraction

The concept of hiding the complex reality while exposing only the necessary parts. It helps in reducing programming complexity and effort.

### Polymorphism

The ability of different objects to respond to the same function call in different ways. It allows one interface to be used for a general class of actions.

### Inheritance

A mechanism by which one class can inherit the properties and methods of another class. It provides a way to create a new class using the properties and methods of an existing class.

### Dynamic Binding

The code to be executed in response to a function call is determined at runtime.

### Message Passing

Objects communicate with one another by sending and receiving information to each other. Messages (function calls) are sent to invoke behavior.

## Visual Representation

The following image depicts the core OOP concepts:

![OOPs-Concepts](https://github.com/user-attachments/assets/915fd2f6-6cb6-4b14-ac47-ae2dee274be2)

 

## Practical Examples

### Example 1: Class and Object

```cpp
#include <iostream>
using namespace std;

class Geeks {
public:
    string geekname;
    int id;

    void printname() {
        cout << "Geekname is: " << geekname;
    }

    void printid() {
        cout << "Geek id is: " << id;
    }
};

int main() {
    Geeks obj1;
    obj1.geekname = "xyz";
    obj1.id = 15;
    obj1.printname();
    obj1.printid();
    return 0;
}
