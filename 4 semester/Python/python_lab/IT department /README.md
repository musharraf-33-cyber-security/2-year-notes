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

