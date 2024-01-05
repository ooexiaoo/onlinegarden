---
{"dg-publish":true,"permalink":"/python-basics/37-finally-clause/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-04T22:16:00.641+05:30","updated":"2024-01-06T03:27:02.304+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/38 - Custom Errors\|38 - Custom Errors]]
Down:: [[Python Basics/36 - Exception Handling\|36 - Exception Handling]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-04 - 22:16==

The finally code block is also a part of exception handling. When we handle exception using the try and except block, we can include a finally block at the end. The finally block is always executed, so it is generally used for doing the concluding tasks like closing file resources or closing database connection or may be ending the program execution with a delightful message.

## Syntax:
```python
try:
	#statements which could generate
	#exception
except:
	#solution of generated exception
finally:
	#block of code which is going to
	#execute in any situation
```

The finally block is executed irrespective of the outcome of try……except…..else blocks  
One of the important use cases of finally block is in a function which returns a value.

## Example:
```python
try:
	num = int(input("Enter an integer: "))
except ValueError:
	print("Number entered is not an integer.")
else:
	print("Integer Accepted.")
finally:
	print("This block is always executed.")
```

### Output 1:
```python
Enter an integer: 19
Integer Accepted.
This block is always executed.
```

### Output 2:
```python
Enter an integer: 3.142
Number entered is not an integer.
This block is always executed.
```

## Main Example
```python
def func1():
  try:
    l = [1, 5, 6, 7]
    i = int(input("Enter the index: "))
    print(l[i])
    return 1
  except:
    print("Some error occurred")
    return 0

  finally:
    print("I am always executed")
  # print("I am always executed")


x = func1()
print(x)
```