# Table of Contents

1. [Object Oriented Programming in C++](#object-oriented-programming-in-c)
2. [Key Concepts of OOP](#key-concepts-of-oop)
   - [Class](#class)
   - [Objects](#objects)
   - [Encapsulation](#encapsulation)
   - [Abstraction](#abstraction)
   - [Polymorphism](#polymorphism)
   - [Inheritance](#inheritance)
   - [Dynamic Binding](#dynamic-binding)
   - [Message Passing](#message-passing)
3. [Characteristics of an Object-Oriented Programming Language](#characteristics-of-an-object-oriented-programming-language)
4. [OOPS Concepts in C++](#oops-concepts-in-c)
5. [Differences between Procedural and Object-Oriented Programming](#differences-between-procedural-and-object-oriented-programming)
   - [Procedural Programming](#procedural-programming)
   - [Object-Oriented Programming](#object-oriented-programming)
   - [Comparison](#comparison)
6. [Functional Programming vs Object-Oriented Programming](#functional-programming-vs-object-oriented-programming)
   - [Functional Programming](#functional-programming)
   - [Object-Oriented Programming](#object-oriented-programming-1)
   - [Comparison](#comparison-1)
7. [Namespace in C++](#namespace-in-c)
   - [Introduction](#introduction)
   - [Defining a Namespace](#defining-a-namespace)
   - [Advantages of Namespaces](#advantages-of-namespaces)
   - [Example of Namespace Usage](#example-of-namespace-usage)
   - [Nested Namespaces](#nested-namespaces)
   - [Namespace Scope](#namespace-scope)
8. [Conclusion](#conclusion)
9. [References](#references)
 
[Table of Contents](#Table of Contents) 
## Object-Oriented Programming (OOP) 

OOP stands for Object-Oriented Programming. It breaks a program into objects, which encapsulate data and functions. Key concepts of OOP include Classes, Objects, Polymorphism, Abstraction, Encapsulation, and Inheritance. Some popular OOP languages include Objective C, Perl, Java, Python, Modula, Ada, Simula, C++, Smalltalk, and Common Lisp.

### Advantages of OOP
- **Modular Development**: Programs can be built from standard modules, saving development time and increasing productivity.
- **Manageable Problems**: Programs can be broken into smaller, manageable pieces, making it easier to solve problems one object at a time.
- **Enhanced Productivity**: OOP can lead to greater programmer productivity and better software quality.
- **Scalability**: OOP systems can be upgraded from small to large systems seamlessly.
- **Object Coexistence**: Multiple instances of objects can coexist without interference.
- **Task Partitioning**: Work on a project can be partitioned based on objects, improving organization.
- **Data Hiding**: Data hiding principles help in building secure programs.
- **Code Reusability**: Inheritance helps in reusing and extending existing code, reducing redundancy.
- **Simplified Communication**: Message passing techniques simplify interface descriptions and communication between objects.
- **Detailed Modeling**: Data-centered design allows capturing more details of the model in an implementable form.

### Disadvantages of OOP
- **Increased Size**: OOP programs can be larger than procedural ones, leading to slower execution times.
- **Limited Applicability**: OOP is not suitable for all types of problems and cannot be universally applied.
- **Complex Design**: Effective use of OOP requires strong design and planning skills.
- **Learning Curve**: OOP may be challenging to grasp for some, requiring a shift in thought process.
- **Object Overhead**: Everything is treated as an object, necessitating careful consideration in its application.

## Application of OOP in C++

### Real-Time System Design
OOP simplifies handling complexities inherent in real-time systems.

### Hypertext and Hypermedia
OOP helps in the framework for hypertext and hypermedia, which is essential for web development.

### AI Expert Systems
OOP aids in developing AI expert systems that tackle complex problems beyond human capability.

### Office Automation Systems
OOP facilitates the development of systems for information sharing and communication within organizations.

### Neural Networking and Parallel Programming
OOP assists in approximating and predicting complex systems through neural networks.

### Simulation and Modeling Systems
OOP provides an appropriate approach to model and simulate complex systems with varying specifications.

### Object-Oriented Databases
OOP maintains a direct correspondence between real-world objects and database objects, preserving their identity and integrity.

### Client-Server Systems
OOP supports creating object-oriented client-server applications.

### CIM/CAD/CAM Systems
OOP can be used in manufacturing and design applications, such as blueprint and flowchart generation.

## Namespace in C++

### Introduction
Namespaces in C++ provide a way to group identifiers such as variables, methods, and classes into a logical scope. They help avoid naming conflicts, especially when combining multiple libraries.

#### Defining a Namespace
```cpp
namespace namespace_name {
    // code declarations
    int a;
    void method();
    class MyClass {};
}


```

 


## Namespace in C++ | Set 1 (Introduction)

### What is a Namespace?

In C++, a namespace provides a space to define or declare identifiers, such as variables, methods, and classes. Essentially, a namespace creates a scope within which these identifiers are defined. This helps in organizing code and avoiding naming conflicts.

### Why Use Namespaces?

Namespaces are crucial in avoiding name collisions, especially when working with large codebases or integrating multiple libraries. For example, you might be writing code with a function named `xyz()`, and another library might also define a function with the same name. Without namespaces, the compiler would have no way of distinguishing between these two functions.

### How Namespaces Help

A namespace allows you to encapsulate identifiers, ensuring that similar names used in different contexts do not interfere with each other. This additional layer of information helps differentiate between functions, classes, variables, and other identifiers with the same name but residing in different namespaces.

### Example

Consider the following scenario:

```cpp
// Code in your project
namespace MyProject {
    void xyz() {
        // Implementation of xyz in MyProject
    }
}

// Code from an external library
namespace ExternalLib {
    void xyz() {
        // Implementation of xyz in ExternalLib
    }
}

```


## Defining a Namespace in C++

### How to Define a Namespace

In C++, a namespace is defined using the `namespace` keyword followed by the namespace name. The namespace encapsulates code declarations such as variables, methods, and classes. The syntax is as follows:

```cpp
namespace namespace_name 
{
    // Variable declaration
    int a;

    // Method declaration
    void add();

    // Class definition
    class Student {
        // Class members
    };
}
```


### Advantages of Namespaces

Namespaces are crucial for managing the complexity of large codebases. They provide the following benefits:

- **Avoid Name Collisions:** When multiple libraries or parts of a program use the same name for different functions, variables, or classes, namespaces help to avoid conflicts. For example, if you have a function named `xyz()` in your code and another library also has a function named `xyz()`, namespaces allow you to specify which version of `xyz()` you are referring to.
  
- **Organize Code:** Namespaces help in grouping related code together, making the codebase more organized and manageable.

### Example of Namespace Usage

Consider a scenario where you are using a library that has a function called `xyz()`, and your own code also has a function named `xyz()`. Without namespaces, the compiler would not be able to distinguish between the two functions. Here’s how namespaces can resolve this issue:

```cpp
#include <iostream>

namespace Library {
    void xyz() {
        std::cout << "Library xyz()" << std::endl;
    }
}

namespace MyCode {
    void xyz() {
        std::cout << "MyCode xyz()" << std::endl;
    }
}

int main() {
    Library::xyz();  // Calls the xyz function in the Library namespace
    MyCode::xyz();   // Calls the xyz function in the MyCode namespace
    return 0;
}
```


## Nested Namespaces

Namespaces can be nested, which means you can define one namespace inside another. This allows for a more granular organization of code. The syntax for nested namespaces is as follows:

### Syntax

```cpp
namespace namespace_name1 {
    // Code declarations

    namespace namespace_name2 {
        // Code declarations
    }
}
```

You can access members of nested namespace by using resolution operators as follows:
// to access members of namespace_name2
using namespace namespace_name1::namespace_name2;
// to access members of namespace_name1
using namespace namespace_name1;
 

# In the above statements if you are using namespace_name1, then it will make elements of namespace_name2 available in the scope as follows:

```cpp
#include <iostream>
using namespace std;

// first name space
namespace first_space
{
void func()
{
	cout << "Inside first_space" << endl;
}
// second name space
namespace second_space
{
	void func()
	{
		cout << "Inside second_space" << endl;
	}
}
}
using namespace first_space::second_space;
int main ()
{
	// This calls function from second name space.
	func();

	return 0;
}
```

Output
``` cpp
Inside second_space
```
# Let us see how namespace scope the entities including variable and functions:

```cpp

#include <iostream>
using namespace std;
// first name space
namespace first_space
{
void func()
{
	cout << "Inside first_space" << endl;
}
}
// second name space
namespace second_space
{
void func()
{
	cout << "Inside second_space" << endl;
}
}

int main ()
{
	// Calls function from first name space.
	first_space :: func();
	// Calls function from second name space.
	second_space :: func(); 
	return 0;
}

```

Output
```cpp
Inside first_space
Inside second_space
```

# Consider the following C++ program: 
```cpp
// A program to demonstrate need of namespace
int main()
{
	int value;
	value = 0;
	double value; // Error here
	value = 0.0;
}
```

Output :
```cpp
Compiler Error:
'value' has a previous declaration as 'int value'
```





In each scope, a name can only represent one entity. So, there cannot be two variables with the same name in the same scope. Using namespaces, we can create two variables or member functions having the same name. 


```cpp
// Here we can see that more than one variables
// are being used without reporting any error.
// That is because they are declared in the
// different namespaces and scopes.
#include <iostream>
using namespace std;

// Variable created inside namespace
namespace first {
int val = 500;
}

// Global variable
int val = 100;

int main()
{
	// Local variable
	int val = 200;

	// These variables can be accessed from
	// outside the namespace using the scope
	// operator ::
	cout << first::val << '\n';

	return 0;
}
```



Output
```
500
```

- Definition and Creation: Namespaces allow us to group named entities that otherwise would have global scope into narrower scopes, giving them namespace scope. This allows organizing the elements of programs into different logical scopes referred to by names. Namespaces provide the space where we can define or declare identifiers i.e. names of variables, methods, classes, etc.

- A namespace is a feature added in C++ and is not present in C.
- A namespace is a declarative region that provides a scope to the identifiers (names of functions, variables or other user-defined data types) inside it.
- Multiple namespace blocks with the same name are allowed. All declarations within those blocks are declared in the named scope.
- A namespace definition begins with the keyword namespace followed by the namespace name as follows:

```
namespace namespace_name 
{
   int x, y; // code declarations where 
             // x and y are declared in 
             // namespace_name's scope
}
```




-Namespace declarations appear only at global scope.
-Namespace declarations can be nested within another namespace.
-Namespace declarations don’t have access specifiers (Public or Private).
-No need to give a semicolon after the closing brace of the definition of namespace.
-We can split the definition of namespace over several units.


# Defining a Namespace:
A namespace definition begins with the keyword namespace followed by the namespace name as follows:
```
namespace namespace_name{
	// code declarations i.e. variable (int a;)
	method (void add();)
	classes ( class student{};)
}
```



It is to be noted that there is no semicolon (;) after the closing brace.
To call the namespace-enabled version of either a function or a variable, prepend the namespace name as follows:

namespace_name: :code;  // code could be a variable, function or class.


```cpp
// Let us see how namespace scope the entities including variable and functions:

#include <iostream>
using namespace std;

// first name space
namespace first_space
{
void func()
{
	cout << "Inside first_space" << endl;
}
}

// second name space
namespace second_space
{
void func()
{
	cout << "Inside second_space" << endl;
}
}

int main ()
{
	// Calls function from first name space.
first_space::func();
	// Calls function from second name space.
second_space::func(); 
return 0;
}

// If we compile and run above code, this would produce the following result:
// Inside first_space
// Inside second_space
```



Output
```cpp
Inside first_space
Inside second_space
```


# The using directive:
You can avoid prepending of namespaces with the using namespace directive. This directive tells the compiler that the subsequent code is making use of names in the specified namespace. The namespace is thus implied for the following 
code:
```cpp
#include <iostream>
using namespace std;

// first name space
namespace first_space
{
void func()
{
	cout << "Inside first_space" << endl;
}
}

// second name space
namespace second_space
{
void func()
{
	cout << "Inside second_space" << endl;
}
}

using namespace first_space;

int main ()
{
	// This calls function from first name space.
func();
return 0;
}

// If we compile and run above code, this would produce the following result:
// Inside first_space
```


Output
```
Inside first_space
```



[Table of Contents](#Table of Contents) 

read more 
[namespace](https://www.geeksforgeeks.org/namespace-in-c/)





