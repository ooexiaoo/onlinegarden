---
{"dg-publish":true,"permalink":"/python-basics/30-recursion/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-28T15:03:55.076+05:30","updated":"2023-12-28T19:58:51.282+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/31 - Sets\|31 - Sets]]
Down:: [[Python Basics/29 - Docstrings\|29 - Docstrings]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-28 - 15:03==

Recursion is the process of defining something in terms of itself.

## Python Recursive Function
In Python, we know that a function can call other functions. It is even possible for the function to call itself. These types of construct are termed as recursive functions.

### Example:
```python
def factorial(num):
	if (num == 1 or num == 0):
		return 1
	else:
		return (num * factorial(num - 1))
# Driver Code
num = 7;
print("Number: ",num)
print("Factorial: ",factorial(num))
```

### Output:
```python
number:  7
Factorial:  5040
```

## Main Example
```python
# factorial(7) = 7*6*5*4*3*2*1
# factorial(6) = 6*5*4*3*2*1
# factorial(5) = 5*4*3*2*1
# factorial(4) = 4*3*2*1
# factorial(0) = 1


# factorial(n) = n * factorial(n-1)
def factorial(n):
  if (n == 0 or n == 1):
    return 1
  else:
    return n * factorial(n - 1)


print(factorial(5))
# 5 * factorial(4)
# 5 * 4 * factorial(3)
# 5 * 4 * 3 * factorial(2)
# 5 * 4 * 3 * 2 * factorial(1)
# 5 * 4 * 3 * 2 * 1

# Quick Quiz: Write a program to print the Fibonacci sequence
# f(0) = 0
# f(1) = 1
# f(2) = f(1) + f(0)
# f(n) = f(n-1) + f(n-2)

# 0 1 1 2 3 5 8....
```