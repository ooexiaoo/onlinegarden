---
{"dg-publish":true,"permalink":"/python-basics/41-short-hand-if-else/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-09T13:24:54.787+05:30","updated":"2024-01-09T13:27:52.200+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Python Basics/40 - Exercise 4\|40 - Exercise 4]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-09 - 13:25==

There is also a shorthand syntax for the if-else statement that can be used when the condition being tested is simple and the code blocks to be executed are short. Here's an example:
```python
a = 2
b = 330
print("A") if a > b else print("B")
```

You can also have multiple else statements on the same line:

### Example
One line if else statement, with 3 conditions:

```python
a = 330
b = 330
print("A") if a > b else print("=") if a == b else print("B")
```

### Another Example
```python
result = value_if_true if condition else value_if_false
```

This syntax is equivalent to the following if-else statement:
```python
if condition:
	result = value_if_true
else:
	result = value_if_false
```

### Conclusion
The shorthand syntax can be a convenient way to write simple if-else statements, especially when you want to assign a value to a variable based on a condition.  
However, it's not suitable for more complex situations where you need to execute multiple statements or perform more complex logic. In those cases, it's best to use the full if-else syntax.

## Main Example
```python
a = 330000
b = 3303
print("A") if a > b else print("=") if a == b else print("B")

c = 9 if a>b else 0
print(c)
```