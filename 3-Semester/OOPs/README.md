# Table of Contents
1. [Object Oriented Programming in C++](#object-oriented-programming-in-c)
2. [Class](#1-class)
3. [Object](#2-object)
4. [Encapsulation](#3-encapsulation)
5. [Abstraction](#4-abstraction)
6. [Polymorphism](#5-polymorphism)
7. [Inheritance](#5-inheritance)
8. [Dynamic Binding](#6-dynamic-binding)


## Object Oriented Programming in C++                        
 
Object-oriented programming – As the name suggests uses objects in programming. Object-oriented programming aims to implement real-world entities like inheritance, hiding, polymorphism, etc. in programming. The main aim of OOP is to bind together the data and the functions that operate on them so that no other part of the code can access this data except that function.

## There are some basic concepts that act as the building blocks of OOPs.  [Move Up](#table-of-contents)

1. **Class**
2. **Objects**
3. **Encapsulation**
4. **Abstraction**
5.**Polymorphism**
6. **Inheritance**
7. **Dynamic Binding**
8. **Message Passing**
9. **Characteristics of an Object-Oriented Programming Language**

   
![OOPs-Concepts](https://github.com/user-attachments/assets/aa7bcab6-9d51-4867-bccb-52a0fc2a6259)





## 1. Class                                                                [Move Up](#table-of-contents)
The building block of C++ that leads to Object-Oriented programming is a Class. It is a user-defined data type, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class. A class is like a blueprint for an object. For Example: Consider the Class of Cars. There may be many cars with different names and brands but all of them will share some common properties like all of them will have 4 wheels, Speed Limit, Mileage range, etc. So here, the Car is the class, and wheels, speed limits, and mileage are their properties.

A Class is a user-defined data type that has data members and member functions.
Data members are the data variables and member functions are the functions used to manipulate these variables together these data members and member functions define the properties and behavior of the objects in a Class.
In the above example of class Car, the data member will be speed limit, mileage, etc and member functions can apply brakes, increase speed, etc.
We can say that a Class in C++ is a blueprint representing a group of objects which shares some common properties and behaviors.

## 2. Object                                                                [Move Up](#table-of-contents)
An Object is an identifiable entity with some characteristics and behavior. An Object is an instance of a Class. When a class is defined, no memory is allocated but when it is instantiated (i.e. an object is created) memory is allocated.


```cpp
// C++ Program to show the syntax/working of Objects as a
// part of Object Oriented PProgramming
#include <iostream>
using namespace std;

class person {
    char name[20];
    int id;

public:
    void getdetails() {}
};

int main()
{

    person p1; // p1 is a object
    return 0;
}
```


Objects take up space in memory and have an associated address like a record in pascal or structure or union. When a program is executed the objects interact by sending messages to one another. Each object contains data and code to manipulate the data. Objects can interact without having to know details of each other’s data or code, it is sufficient to know the type of message accepted and the type of response returned by the objects.

To know more about C++ Objects and Classes, refer to this article [C++ Classes and Objects](https://www.geeksforgeeks.org/c-classes-and-objects/)

## 3. Encapsulation                                                          [Move Up](#table-of-contents)
In normal terms, Encapsulation is defined as wrapping up data and information under a single unit. In Object-Oriented Programming, Encapsulation is defined as binding together the data and the functions that manipulate them. Consider a real-life example of encapsulation, in a company, there are different sections like the accounts section, finance section, sales section, etc. The finance section handles all the financial transactions and keeps records of all the data related to finance. Similarly, the sales section handles all the sales-related activities and keeps records of all the sales. Now there may arise a situation when for some reason an official from the finance section needs all the data about sales in a particular month. In this case, he is not allowed to directly access the data of the sales section. He will first have to contact some other officer in the sales section and then request him to give the particular data. This is what encapsulation is. Here the data of the sales section and the employees that can manipulate them are wrapped under a single name “sales section”.


![Encapsulation-in-C-1](https://github.com/user-attachments/assets/b82743e2-04b8-44f3-bcc3-dcbf9c6cd0c0)

Encapsulation also leads to data abstraction or data hiding. Using encapsulation also hides the data. In the above example, the data of any of the sections like sales, finance, or accounts are hidden from any other section.

To know more about encapsulation, refer to this article –[Encapsulation in C++](https://www.geeksforgeeks.org/encapsulation-in-cpp/)






           
## 4. Abstraction                                                            [Move Up](#table-of-contents)
Data abstraction is one of the most essential and important features of object-oriented programming in C++. Abstraction means displaying only essential information and hiding the details. Data abstraction refers to providing only essential information about the data to the outside world, hiding the background details or implementation. Consider a real-life example of a man driving a car. The man only knows that pressing the accelerator will increase the speed of the car or applying brakes will stop the car but he does not know how on pressing the accelerator the speed is actually increasing, he does not know about the inner mechanism of the car or the implementation of an accelerator, brakes, etc. in the car. This is what abstraction is.

Abstraction using Classes: We can implement Abstraction in C++ using classes. The class helps us to group data members and member functions using available access specifiers. A Class can decide which data member will be visible to the outside world and which is not.
Abstraction in Header files: One more type of abstraction in C++ can be header files. For example, consider the pow() method present in math.h header file. Whenever we need to calculate the power of a number, we simply call the function pow() present in the math.h header file and pass the numbers as arguments without knowing the underlying algorithm according to which the function is actually calculating the power of numbers. 
 
## Types of Abstraction:                                                     [Move Up](#table-of-contents)
1. **Data abstraction** – This type only shows the required information about the data and hides the 
                           unnecessary data.

2. **Control Abstraction** – This type only shows the required information about the implementation and 
                              hides unnecessary information.

 
## Abstraction using Classes                                                 [Move Up](#table-of-contents)
We can implement Abstraction in C++ using classes. The class helps us to group data members and member functions using available access specifiers. A Class can decide which data member will be visible to the outside world and which is not. 

## Abstraction in Header files                                               [Move Up](#table-of-contents)
One more type of abstraction in C++ can be header files. For example, consider the pow() method present in math.h header file. Whenever we need to calculate the power of a number, we simply call the function pow() present in the math.h header file and pass the numbers as arguments without knowing the underlying algorithm according to which the function is actually calculating the power of numbers.
 
## Abstraction using Access Specifiers                                      [Move Up](#table-of-contents)
Access specifiers are the main pillar of implementing abstraction in C++. We can use access specifiers to enforce restrictions on class members. For example:

- Members declared as public in a class can be accessed from anywhere in the program.
 
- Members declared as private in a class, can be accessed only from within the class. They are not allowed to be accessed from any part of the code outside the class.
We can easily implement abstraction using the above two features provided by access specifiers. Say, the members that define the internal implementation can be marked as private in a class. And the important information needed to be given to the outside world can be marked as public. And these public members can access the private members as they are inside the class.


**Example**                                                                  [Move Up](#table-of-contents)
```cpp
// C++ Program to Demonstrate the
// working of Abstraction
#include <iostream>
using namespace std;

class implementAbstraction {
private:
	int a, b;

public:
	// method to set values of
	// private members
	void set(int x, int y)
	{
		a = x;
		b = y;
	}

	void display()
	{
		cout << "a = " << a << endl;
		cout << "b = " << b << endl;
	}
};

int main()
{
	implementAbstraction obj;
	obj.set(10, 20);
	obj.display();
	return 0;
}
```

## Output
```
a = 10
b = 20
```
You can see in the above program we are not allowed to access the variables a and b directly, however, one can call the function set() to set the values in a and b and the function display() to display the values of a and b. 



## Advantages of Data Abstraction                                           [Move Up](#table-of-contents)
- Helps the user to avoid writing the low-level code
- Avoids code duplication and increases reusability.
- Can change the internal implementation of the class independently without affecting the user.
- Helps to increase the security of an application or program as only important details are provided to 
  the user.
- It reduces the complexity as well as the redundancy of the code, therefore increasing the readability.



To know more about C++ abstraction, refer to this article – [Abstraction in C++](https://www.geeksforgeeks.org/abstraction-in-cpp/)






## 5. Polymorphism                                                           [Move Up](#table-of-contents)
The word polymorphism means having many forms. In simple words, we can define polymorphism as the ability of a message to be displayed in more than one form. A person at the same time can have different characteristics. A man at the same time is a father, a husband, and an employee. So the same person possesses different behavior in different situations. This is called polymorphism. An operation may exhibit different behaviors in different instances. The behavior depends upon the types of data used in the operation. C++ supports operator overloading and function overloading.

- **Operator Overloading**: The process of making an operator exhibit different behaviors in different 
                              instances is known as operator overloading.
- **Function Overloading**: Function overloading is using a single function name to perform different 
                            types of tasks. Polymorphism is extensively used in implementing inheritance.

**Example**: Suppose we have to write a function to add some integers, sometimes there are 2 integers, 
             and sometimes there are 3 integers. We can write the Addition Method with the same name 
             having different parameters, the concerned method will be called according to parameters.

             


![polymorphismexample-660x460](https://github.com/user-attachments/assets/6fc562bb-b997-477b-a168-e585cb9f454e)


## Types of Polymorphism                                                     [Move Up](#table-of-contents)
   1. **Compile-time Polymorphism**
   2. **Runtime Polymorphism**
    
![Polymorphism-in-CPP](https://github.com/user-attachments/assets/8021cae9-fd1d-49f8-a581-961fb1f2ed9d)


## 1. Compile-Time Polymorphism
This type of polymorphism is achieved by function overloading or operator overloading.

**A. Function Overloading**                                                 [Move Up](#table-of-contents)
When there are multiple functions with the same name but different parameters, then the functions are said to be overloaded, hence this is known as Function Overloading. Functions can be overloaded by changing the number of arguments or/and changing the type of arguments. In simple terms, it is a feature of object-oriented programming providing many functions that have the same name but distinct parameters when numerous tasks are listed under one function name. There are certain Rules of Function Overloading that should be followed while overloading a function.

Below is the C++ program to show function overloading or compile-time polymorphism:

```cpp
// C++ program to demonstrate
// function overloading or
// Compile-time Polymorphism
#include <bits/stdc++.h>

using namespace std;
class Geeks {
public:
	// Function with 1 int parameter
	void func(int x)
	{
		cout << "value of x is " << x << endl;
	}

	// Function with same name but
	// 1 double parameter
	void func(double x)
	{
		cout << "value of x is " << x << endl;
	}

	// Function with same name and
	// 2 int parameters
	void func(int x, int y)
	{
		cout << "value of x and y is " << x << ", " << y
			<< endl;
	}
};

// Driver code
int main()
{
	Geeks obj1;

	// Function being called depends
	// on the parameters passed
	// func() is called with int value
	obj1.func(7);

	// func() is called with double value
	obj1.func(9.132);

	// func() is called with 2 int values
	obj1.func(85, 64);
	return 0;
}
```



## Output                                                                    [Move Up](#table-of-contents)
```
value of x is 7
value of x is 9.132
value of x and y is 85, 64
```
Explanation: In the above example, a single function named function func() acts differently in three different situations, which is a property of polymorphism. 
To know more about this, you can refer to the article – [Function Overloading in C++](https://www.geeksforgeeks.org/function-overloading-c/)


**B. Operator Overloading**                                                [Move Up](#table-of-contents)
C++ has the ability to provide the operators with a special meaning for a data type, this ability is known as operator overloading. For example, we can make use of the addition operator (+) for string class to concatenate two strings. We know that the task of this operator is to add two operands. So a single operator ‘+’, when placed between integer operands, adds them and when placed between string operands, concatenates them. 

Below is the C++ program to demonstrate operator overloading:
```cpp
// C++ program to demonstrate
// Operator Overloading or
// Compile-Time Polymorphism
#include <iostream>
using namespace std;

class Complex {
private:
	int real, imag;

public:
	Complex(int r = 0, int i = 0)
	{
		real = r;
		imag = i;
	}

	// This is automatically called
	// when '+' is used with between
	// two Complex objects
	Complex operator+(Complex const& obj)
	{
		Complex res;
		res.real = real + obj.real;
		res.imag = imag + obj.imag;
		return res;
	}
	void print() { cout << real << " + i" << imag << endl; }
};

// Driver code
int main()
{
	Complex c1(10, 5), c2(2, 4);

	// An example call to "operator+"
	Complex c3 = c1 + c2;
	c3.print();
}

```


## Output                                                                  [Move Up](#table-of-contents)

```
12 + i9
```

**Explanation**:  In the above example, the operator ‘+’ is overloaded. Usually, this operator is used to add two numbers (integers or floating point numbers), but here the operator is made to perform the addition of two imaginary or complex numbers.
To know more about this one, refer to the article – [Operator Overloading.](https://www.geeksforgeeks.org/operator-overloading-cpp/)



## 2. Runtime Polymorphism                                                 [Move Up](#table-of-contents)
This type of polymorphism is achieved by Function Overriding. Late binding and dynamic polymorphism are other names for runtime polymorphism. The function call is resolved at runtime in [runtime polymorphism](https://www.geeksforgeeks.org/virtual-functions-and-runtime-polymorphism-in-cpp/). In contrast, with compile time polymorphism, the compiler determines which function call to bind to the object after deducing it at runtime.

**A. Function Overriding**
[Function Overriding](https://www.geeksforgeeks.org/function-overriding-in-cpp/) occurs when a derived class has a definition for one of the member functions of the base class. That base function is said to be overridden.

![FunctionOverridingAlgo-474x660](https://github.com/user-attachments/assets/e8c78eca-73cb-424d-b509-9b45d7f6e21e)



**Runtime Polymorphism with Data Members**                                  [Move Up](#table-of-contents)
Runtime Polymorphism cannot be achieved by data members in C++. Let’s see an example where we are accessing the field by reference variable of parent class which refers to the instance of the derived class.

```cpp
// C++ program for function overriding with data members
#include <bits/stdc++.h>
using namespace std;

// base class declaration.
class Animal {
public:
	string color = "Black";
};

// inheriting Animal class.
class Dog : public Animal {
public:
	string color = "Grey";
};

// Driver code
int main(void)
{
	Animal d = Dog(); // accessing the field by reference
					// variable which refers to derived
	cout << d.color;
}
```

## Output                                                                   [Move Up](#table-of-contents)
```
Black
```
We can see that the parent class reference will always refer to the data member of the parent class.


**B. Virtual Function**
A [virtual function](https://www.geeksforgeeks.org/virtual-function-cpp/) is a member function that is declared in the base class using the keyword virtual and is re-defined (Overridden) in the derived class.

Some Key Points About Virtual Functions:
Virtual functions are Dynamic in nature. 
They are defined by inserting the keyword “virtual” inside a base class and are always declared with a base class and overridden in a child class
A virtual function is called during Runtime

**Below is the C++ program to demonstrate virtual function:**            [Move Up](#table-of-contents)
```cpp
// C++ Program to demonstrate
// the Virtual Function
#include <iostream>
using namespace std;

// Declaring a Base class
class GFG_Base {

public:
	// virtual function
	virtual void display()
	{
		cout << "Called virtual Base Class function"
			<< "\n\n";
	}

	void print()
	{
		cout << "Called GFG_Base print function"
			<< "\n\n";
	}
};

// Declaring a Child Class
class GFG_Child : public GFG_Base {

public:
	void display()
	{
		cout << "Called GFG_Child Display Function"
			<< "\n\n";
	}

	void print()
	{
		cout << "Called GFG_Child print Function"
			<< "\n\n";
	}
};

// Driver code
int main()
{
	// Create a reference of class GFG_Base
	GFG_Base* base;

	GFG_Child child;

	base = &child;

	// This will call the virtual function
	base->GFG_Base::display();

	// this will call the non-virtual function
	base->print();
}
```

## Output

```
Called virtual Base Class function

Called GFG_Base print function
```


## 5. Inheritance                                                          [Move Up](#table-of-contents)
The capability of a class to derive properties and characteristics from another class is called Inheritance. Inheritance is one of the most important features of Object-Oriented Programming.

Sub Class: The class that inherits properties from another class is called Sub class or Derived Class.
Super Class: The class whose properties are inherited by a sub-class is called Base Class or Superclass.
Reusability: Inheritance supports the concept of “reusability”, i.e. when we want to create a new class and there is already a class that includes some of the code that we want, we can derive our new class from the existing class. By doing this, we are reusing the fields and methods of the existing class.
Example: Dog, Cat, Cow can be Derived Class of Animal Base Class. 



![inheritance-660x454](https://github.com/user-attachments/assets/6783b901-2857-4d36-b585-78d4d9b842c8)

To know more about Inheritance, refer to this article – [Inheritance in C++](https://www.geeksforgeeks.org/inheritance-in-c/)



## 6. Dynamic Binding                                                 [Move Up](#table-of-contents)
In dynamic binding, the code to be executed in response to the function call is decided at runtime. C++ has [virtual functions](https://www.geeksforgeeks.org/virtual-functions-and-runtime-polymorphism-in-cpp/) to support this. Because dynamic binding is flexible, it avoids the drawbacks of static binding, which connected the function call and definition at build time.

**Example:**

```cpp
// C++ Program to Demonstrate the Concept of Dynamic binding
// with the help of virtual function
#include <iostream>
using namespace std;

class GFG {
public:
    void call_Function() // function that call print
    {
        print();
    }
    void print() // the display function
    {
        cout << "Printing the Base class Content" << endl;
    }
};
class GFG2 : public GFG // GFG2 inherit a publicly
{
public:
    void print() // GFG2's display
    {
        cout << "Printing the Derived class Content"
             << endl;
    }
};
int main()
{
    GFG geeksforgeeks; // Creating GFG's object
    geeksforgeeks.call_Function(); // Calling call_Function
    GFG2 geeksforgeeks2; // creating GFG2 object
    geeksforgeeks2.call_Function(); // calling call_Function
                                    // for GFG2 object
    return 0;
}
```

## Output                                                                [Move Up](#table-of-contents)
``` 
Printing the Base class Content
Printing the Base class Content
```


As we can see, the print() function of the parent class is called even from the derived class object. To resolve this we use virtual functions.




**Above Example with virtual Function:**

```cpp
#include<bits/stdc++.h>
using namespace std;

class GFG {
public:
    void call_Function() // function that call print
    {
        print();
    }
    virtual void print() // using "virtual" for the display function 
    {
        cout << "Printing the Base class Content" << endl;
    }
};
class GFG2 : public GFG // GFG2 inherit a publicly
{
public:
    void print() // GFG2's display
    {
        cout << "Printing the Derived class Content"
            << endl;
    }
};
int main()
{
    GFG geeksforgeeks; // Creating GFG's object
    geeksforgeeks.call_Function(); // Calling call_Function
    GFG2 geeksforgeeks2; // creating GFG2 object
    geeksforgeeks2.call_Function(); // calling call_Function
                                    // for GFG2 object
    return 0;
}

//this code is contributed by Md Nizamuddin
```

## Output                                                            [Move Up](#table-of-contents)
```
Printing the Base class Content
Printing the Derived class Content
```


## Message Passing                                                     [Move Up](#table-of-contents)
Objects communicate with one another by sending and receiving information. A message for an object is a request for the execution of a procedure and therefore will invoke a function in the receiving object that generates the desired results. Message passing involves specifying the name of the object, the name of the function, and the information to be sent.

**Example:**

```cpp
#include <iostream>
using namespace std;

// Define a Car class with a method to display its speed
class Car {
public:
    void displaySpeed(int speed) {
        cout << "The car is moving at " << speed << " km/h." << endl;
    }
};

int main() {
    // Create a Car object named myCar
    Car myCar;

    // Send a message to myCar to execute the displaySpeed method
    int currentSpeed = 100;
    myCar.displaySpeed(currentSpeed);

    return 0;
}



```
