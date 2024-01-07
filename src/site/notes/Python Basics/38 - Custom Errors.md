---
{"dg-publish":true,"permalink":"/python-basics/38-custom-errors/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-06T03:26:25.687+05:30","updated":"2024-01-07T22:29:26.848+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/40 - Exercise 4\|40 - Exercise 4]]
Down:: [[Python Basics/37 - Finally Clause\|37 - Finally Clause]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-06 - 03:26==

In python, we can raise custom errors by using the `raise` keyword.

```python
salary = int(input("Enter salary amount: "))
if not 2000 < salary < 5000:
	raise ValueError("Not a valid salary")
```

In the previous tutorial, we learned about different built-in exceptions in Python and why it is important to handle exceptions. However, sometimes we may need to create our own custom exceptions that serve our purpose.

### Defining Custom Exceptions
In Python, we can define custom exceptions by creating a new class that is derived from the built-in Exception class.

Here's the syntax to define custom exceptions:

```python
class CustomError(Exception):
	# code ...
	pass
	
try:
	# code ...
	
except CustomError:
	# code...
```

This is useful because sometimes we might want to do something when a particular exception is raised. For example, sending an error report to the admin, calling an api, etc.

## Main Example
```python
a = int(input("Enter any value between 5 and 9"))

if(a<5  or a>9):
  raise  ValueError("Value should be between 5 and 9")
```