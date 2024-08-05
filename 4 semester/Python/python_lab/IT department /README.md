# WAP to show  implementation of Variables and Literals, Comments,Single-line Comment,Multiline Comments




```py
# This is an example of a multiline comment
# created using multiple single-line commenced
# The code prints the text Hello World
print("Hello, World!")

a, b, c = 5, 3.2, 'Hello'

print (a)  # prints 5
print (b)  # prints 3.2
print (c)  # prints Hello

x = y =site1 = site2  = 'programiz.com'

print(x)  # prints programiz.com
print(y)  # prints programiz.com

```


## Output
```
Hello, World!
5
3.2
Hello
programiz.com
programiz.com
```





#  WAP to show  implementation of Type Conversion
- **1: Converting integer to float**
- **2: Addition of string and integer Using Explicit Conversion**
- ****





```py
  

i=int(input("Enter integer number  :"))

f=eval(input("Enter flot number  :"))
print("\n\nImplicit Type Conversion")
n=i+f
print("successfully Converting datatype : ",n)
print(type(n))




 
print(" \n\n\n\nExplicit Type Conversion") 
num_string = '12'
 
print("Data type of num_string before Type Casting:",type(num_string))

# explicit type conversion
num_string = int(num_string)

print("Data type of num_string after Type Casting:",type(num_string))

num_sum = i + num_string

print("Sum:",num_sum)
print("Data type of num_sum:",type(num_sum))


```

# Output
```
Enter integer number  :556
Enter flot number  :5.6


Implicit Type Conversion
successfully Converting datatype :  561.6
<class 'float'>
 



Explicit Type Conversion
Data type of num_string before Type Casting: <class 'str'>
Data type of num_string after Type Casting: <class 'int'>
Sum: 568
Data type of num_sum: <class 'int'>
```






#  WAP to show  implementation of Python Operators
- 1. Arithmetic Operators
- 2. Assignment Operators
- 3. Comparison Operators
- 4. Logical Operators
- 5. Bitwise Operators
- 6. Special Operators


```py
a = int(input("Enter first number \t "))
b = int(input("Enter Second number "))


print ('Sum: ', a + b)  
 
print ('Subtraction: ', a - b)   

 
print ('Multiplication: ', a * b)  

 
print ('Division: ', a / b) 

 
print ('Floor Division: ', a // b)

 
print ('Modulo: ', a % b)  

 
print ('Power: ', a ** b)


```

## output

```
Enter first number 	 7
Enter Second number 8
Sum:  15
Subtraction:  -1
Multiplication:  56
Division:  0.875
Floor Division:  0
Modulo:  7
Power:  5764801
````




#  WAP to show  implementation of  Assignment Operators
- Addition Assignment	
- Subtraction Assignment	
- Multiplication Assignment
- Division Assignment	
- Remainder Assignment
- Exponent Assignment

```py
 
a = int(input("assign first  value  \t "))
b = int(input("assign second  value "))



print("Assignment Operators")
print ( a )  
print (b)   

print("\nAddition Assignment && Subtraction Assignment ")

a +=1  # a = a + 1
b -=1
print( "Addition is :", a)
print ("Subtraction is :",b)


print("\nMultiplication Assignment")
a *= b  # a = a * b
print(a)
 
print("\nDivision Assignment ")

a  /=b # a =  a/b
print(a) 



print("\nRemainder Assignment ") 
a %=b
print (a)


print("\n Exponent Assignment ")
a **= b
print (a)
  

```

## Output

```
assign first  value  	 6
assign second  value 6
Assignment Operators
6
6

Addition Assignment && Subtraction Assignment 
Addition is : 7
Subtraction is : 5

Multiplication Assignment
35

Division Assignment 
7.0

Remainder Assignment 
2.0

 Exponent Assignment 
32.0
```




#  WAP to show  implementation of Comparison Operators

```py

a = 5

b = 2

# equal to operator
print('a == b =', a == b)

# not equal to operator
print('a != b =', a != b)

# greater than operator
print('a > b =', a > b)

# less than operator
print('a < b =', a < b)

# greater than or equal to operator
print('a >= b =', a >= b)

# less than or equal to operator
print('a <= b =', a <= b)

```

# output 
```
a == b = False
a != b = True
a > b = True
a < b = False
a >= b = True
a <= b = False
```



#  WAP to show  implementation of Logical Operators
```py

print("\n Logical Operators")
a = 5
b = 6

print((a > 2) and (b >= 6))   

print((a > 2) or (b >= 6)) 

print("\n Special operators :")
x1 = 5
y1 = 5
x2 = 'Hello'
y2 = 'Hello'
x3 = [1,2,3]
y3 = [1,2,3]
print(x1 is not y1)   
print(x2 is y2)   
print(x3 is y3)   

print("\nMembership operators :")
message = 'Hello world'
dict1 = {1:'a', 2:'b'}
print('H' in message)   
print('hello' not in message)  
print(1 in dict1)   
print('a' in dict1)  

```

## output
```
Logical Operators
True
True

 Special operators :
False
True
False

Membership operators :
True
True
True
False
```




