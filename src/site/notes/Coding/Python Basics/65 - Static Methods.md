---
{"dg-publish":true,"permalink":"/coding/python-basics/65-static-methods/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-02-15T18:33:29.546+05:30","updated":"2024-02-15T18:43:16.460+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Coding/Python Basics/64 - Exercise 6\|64 - Exercise 6]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-02-15 - 18:33==

Static methods in Python are methods that belong to a class rather than an instance of the class. They are defined using the **@staticmethod** decorator and do not have access to the instance of the class (i.e. self). They are called on the class itself, not on an instance of the class. Static methods are often used to create utility functions that don't need access to instance data.

```python
class Math:
	@staticmethod
	def add(a, b):
		return a + b

result = Math.add(1, 2)
print(result) # Output: 3
```

In this example, the add method is a static method of the Math class. It takes two parameters a and b and returns their sum. The method can be called on the class itself, without the need to create an instance of the class.

## Main Example
```python
class Math:
  def __init__(self, num):
    self.num = num

  def addtonum(self, n):
    self.num = self.num +n
    
  @staticmethod
  def add(a, b):
      return a + b

# result = Math.add(1, 2)
# print(result) # Output: 3
a = Math(5)
print(a.num)
a.addtonum(6)
print(a.num)

print(Math.add(7, 2)) 
```