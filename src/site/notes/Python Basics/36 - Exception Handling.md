---
{"dg-publish":true,"permalink":"/python-basics/36-exception-handling/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-04T17:01:37.301+05:30","updated":"2024-01-04T17:04:35.720+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Python Basics/35 - For loop with else\|35 - For loop with else]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-04 - 17:01==

## Exception Handling
Exception handling is the process of responding to unwanted or unexpected events when a computer program runs. Exception handling deals with these events to avoid the program or system crashing, and without this process, exceptions would disrupt the normal operation of a program.

## Exceptions in Python
Python has many built-in exceptions that are raised when your program encounters an error (something in the program goes wrong).

When these exceptions occur, the Python interpreter stops the current process and passes it to the calling process until it is handled. If not handled, the program will crash.

## Python try...except
try….. except blocks are used in python to handle errors and exceptions. The code in try block runs when there is no error. If the try block catches the error, then the except block is executed.

### Syntax:
```python
try:
	#statements which could generate
	#exception
except:
	#Soloution of generated exception
```

### Example:
```python
try:
	num = int(input("Enter an integer: "))
except ValueError:
	print("Number entered is not an integer.")
```

### Output:
```python
Enter an integer: 6.022
Number entered is not an integer.
```

## Main Example
```python
# a = input("Enter the number: ")
# print(f"Multiplication table of {a} is: ")
# try:
#   for i in range(1, 11):
#     print(f"{int(a)} X {i} = {int(a)*i}")
# except:
#   print("Invalid  Input!")

# print("Some imp lines of code")
# print("End of program")

try:
    num = int(input("Enter an integer: "))
    a = [6, 3]
    print(a[num])
except ValueError:
    print("Number entered is not an integer.")
    
except IndexError:
  print("Index Error")
```