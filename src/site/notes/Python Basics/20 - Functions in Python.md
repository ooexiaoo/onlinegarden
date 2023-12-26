---
{"dg-publish":true,"permalink":"/python-basics/20-functions-in-python/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-20T12:00:20.747+05:30","updated":"2023-12-23T13:37:55.440+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/21 - Function Arguments\|21 - Function Arguments]]
Down:: [[Python Basics/19 - Break and Continue\|19 - Break and Continue]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-20 - 12:00==

A function is a block of code that performs a specific task whenever it is called. In bigger programs, where we have large amounts of code, it is advisable to create or use existing functions that make the program flow organized and neat.

There are two types of functions:
1. Built-in functions
2. User-defined functions

## Built-in functions:
These functions are defined and pre-coded in python. Some examples of built-in functions are as follows:
*min(), max(), len(), sum(), type(), range(), dict(), list(), tuple(), set(), print(), etc.*

## User-defined functions:
We can create functions to perform specific tasks as per our needs. Such functions are called user-defined functions.
### Syntax:
```python
def function_name(parameters):
	pass
	# Code and Statements
```

- Create a function using the def keyword, followed by a function name, followed by a parenthesis (()) and a colon(:).
- Any parameters and arguments should be placed within the parentheses.
- Rules to naming function are similar to that of naming variables.
- Any statements and other code within the function should be indented.

### Calling a function:
We call a function by giving the function name, followed by parameters (if any) in the parenthesis.

#### Example:
```python
def name(fname, lname):
	print("Hello,", fname, lname)
	
name("Sam", "Wilson")
```

#### Output:
```python
Hello, Sam Wilson
```

## Main Example
```python
def calculateGmean(a, b):
  mean = (a*b)/(a+b)
  print(mean)

def isGreater(a, b):
  if(a>b):
    print("First number is greater")
  else:
    print("Second number is greater or equal")

def isLesser(a, b):
  pass
  

a = 9
b = 8
isGreater(a, b)
calculateGmean(a, b)
# gmean1 = (a*b)/(a+b)
# print(gmean1)
c = 8
d = 74
isGreater(c, d)
calculateGmean(c, d)
# gmean2 = (c*d)/(c+d)
# print(gmean2)
```