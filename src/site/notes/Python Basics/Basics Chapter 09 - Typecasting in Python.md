---
{"dg-publish":true,"permalink":"/python-basics/basics-chapter-09-typecasting-in-python/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-09T00:57:52.121+05:30","updated":"2023-12-18T20:43:41.293+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/Basics Chapter 10 - Taking User Input\|Basics Chapter 10 - Taking User Input]]
Down:: [[Python Basics/Basics Chapter 07 - Operators\|Basics Chapter 07 - Operators]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-09 - 00:57==
The conversion of one data type into the other data type is known as type casting in python or type conversion in python.

Python supports a wide variety of functions or methods like: int(), float(), str(), ord(), hex(), oct(), tuple(), set(), list(), dict(), etc. for the type casting in python.

## Two Types of Typecasting:
1. Explicit Conversion (Explicit type casting in python)
2. Implicit Conversion (Implicit type casting in python)
### Explicit typecasting:
The conversion of one data type into another data type, done via developer or programmer's intervention or manually as per the requirement, is known as explicit type conversion.

It can be achieved with the help of Python’s built-in type conversion functions such as int(), float(), hex(), oct(), str(), etc .
#### Example of explicit typecasting:
```python
string = "15"
number = 7
string_number = int(string) #throws an error if the string is not a valid integer
sum= number + string_number
print("The Sum of both the numbers is: ", sum)
```
##### Output:
```python
The Sum of both the numbers is 22
```
### Implicit type casting:
Data types in Python do not have the same level i.e. ordering of data types is not the same in Python. Some of the data types have higher-order, and some have lower order.
While performing any operations on variables with different data types in Python, one of the variable's data types will be changed to the higher data type.
According to the level, one data type is converted into other by the Python interpreter itself (automatically).
This is called, implicit typecasting in python.

Python converts a smaller data type to a higher data type to prevent data loss.
#### Example of implicit type casting:
```python
# Python automatically converts
# a to int
a = 7
print(type(a))

# Python automatically converts b to float
b = 3.0
print(type(b))

# Python automatically converts c to float as it is a float addition
c = a + b
print(c)
print(type(c))
```
##### Output:
```python
<class 'int'>
<class 'float'>
10.0
<class 'float'>
```