---
{"dg-publish":true,"permalink":"/coding/python-basics/58-constructors/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-02-08T00:14:39.548+05:30","updated":"2024-02-08T00:17:42.734+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Coding/Python Basics/57 - Classes and Objects\|57 - Classes and Objects]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-02-08 - 00:14==

A constructor is a special method in a class used to create and initialize an object of a class. There are different types of constructors. Constructor is invoked automatically when an object of a class is created.

A constructor is a unique function that gets called automatically when an object is created of a class. The main purpose of a constructor is to initialize or assign values to the data members of that class. It cannot return any value other than None.

## Syntax of Python Constructor
```python
def __init__(self):
	# initializations
```

init is one of the reserved functions in Python. In Object Oriented Programming, it is known as a constructor.

## Types of Constructors in Python
1. Parameterized Constructor
2. Default Constructor

### Parameterized Constructor in Python
When the constructor accepts arguments along with self, it is known as parameterized constructor.

These arguments can be used inside the class to assign the values to the data members.

#### Example:
```python
class Details:
	def __init__(self, animal, group):
	self.animal = animal
	self.group = group

obj1 = Details("Crab", "Crustaceans")
print(obj1.animal, "belongs to the", obj1.group, "group.")
```

#### Output:
```python
Crab belongs to the Crustaceans group.
```

### Default Constructor in Python
When the constructor doesn't accept any arguments from the object and has only one argument, self, in the constructor, it is known as a Default constructor.

#### Example:
```python
class Details:
	def __init__(self):
	print("animal Crab belongs to Crustaceans group")
obj1=Details()
```

#### Output:
```python
animal Crab belongs to Crustaceans group
```

## Main Example
```python
class Person:

  def __init__(self, name, occ):
    print("Hey I am a person")
    self.name = name
    self.occ = occ

  def info(self):
    print(f"{self.name} is a {self.occ}")


a = Person("Harry", "Developer")
b = Person("Divya", "HR") 
a.info()
b.info()
# print(a.name)
# a.name = "Divya"
# a.occ = "HR"
# a.info()
```