# Object Oriented Programming in C++

## Overview

Object-oriented programming (OOP) uses objects in programming. The main aim of OOP is to implement real-world entities like inheritance, hiding, polymorphism, etc., in programming. It aims to bind together the data and the functions that operate on them so that no other part of the code can access this data except that function.

## Key Concepts of OOP

OOP is based on several fundamental concepts, which act as its building blocks:

1. **Class**: A blueprint for creating objects (a particular data structure), providing initial values for state (member variables or fields), and implementations of behavior (member functions or methods).

    ### Class
    The building block of C++ that leads to Object-Oriented programming is a Class. It is a user-defined data type, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class. A class is like a blueprint for an object.

    For Example: Consider the Class of Cars. There may be many cars with different names and brands but all of them will share some common properties like all of them will have 4 wheels, Speed Limit, Mileage range, etc. So here, the Car is the class, and wheels, speed limits, and mileage are their properties.

    ```cpp
    class Car {
        int speedLimit;
        int mileage;
    public:
        void applyBrakes() {}
        void increaseSpeed() {}
    };
    ```

2. **Objects**: Instances of classes. Objects hold data and can perform functions defined by their class.

    ### Object
    An Object is an identifiable entity with some characteristics and behavior. An Object is an instance of a Class. When a class is defined, no memory is allocated but when it is instantiated (i.e., an object is created) memory is allocated.

    ```cpp
    // C++ Program to show the syntax/working of Objects as a part of Object Oriented Programming
    #include <iostream>
    using namespace std;

    class Person {
        char name[20];
        int id;
    public:
        void getDetails() {}
    };

    int main() {
        Person p1; // p1 is an object
        return 0;
    }
    ```

    Objects take up space in memory and have an associated address like a record in Pascal or structure or union. When a program is executed, the objects interact by sending messages to one another. Each object contains data and code to manipulate the data.

    [Copy Code](# "class Person { char name[20]; int id; public: void getDetails() {} }; int main() { Person p1; return 0; }")

    [Run Code](https://onlinegdb.com/fork/rJmSx4_FH "class Person { char name[20]; int id; public: void getDetails() {} }; int main() { Person p1; return 0; }")

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
![OOPs-Concepts](https://github.com/user-attachments/assets/8e54733e-f1a9-47a8-9ac8-d373b44a3d41)

## Conclusion

OOP in C++ facilitates the creation of programs that are more modular, easier to maintain, and more intuitive to understand. By mastering these concepts, developers can build robust and scalable software applications.

---

## References

- [OOP Concepts](https://www.geeksforgeeks.org/object-oriented-programming-in-cpp/)
- [Detailed OOP in C++](https://www.javatpoint.com/cpp-oops-concepts)

---

Feel free to contribute to this repository by adding more examples or improving the explanations of the OOP concepts.
