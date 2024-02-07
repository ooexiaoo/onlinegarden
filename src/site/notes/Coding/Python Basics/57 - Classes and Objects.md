---
{"dg-publish":true,"permalink":"/coding/python-basics/57-classes-and-objects/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-02-06T23:27:48.242+05:30","updated":"2024-02-08T00:15:03.462+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Coding/Python Basics/58 - Constructors\|58 - Constructors]]
Down:: [[Coding/Python Basics/56 - Intro to oops\|56 - Intro to oops]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-02-06 - 23:27==

## Python Class and Objects
A class is a blueprint or a template for creating objects, providing initial values for state (member variables or attributes), and implementations of behavior (member functions or methods). The user-defined objects are created using the class keyword.

### Creating a Class:
Let us now create a class using the class keyword.
```python
class Details:
	name = "Rohan"
	age = 20
```

### Creating an Object:
Object is the instance of the class used to access the properties of the class Now lets create an object of the class.

#### Example:
```python
obj1 = Details()
```

Now we can print values:

#### Example:
```python
class Details:
	name = "Rohan"
	age = 20

obj1 = Details()
print(obj1.name)
print(obj1.age)
```

#### Output:
```python
Rohan
20
```

## self parameter
The self parameter is a reference to the current instance of the class, and is used to access variables that belongs to the class.

It must be provided as the extra parameter inside the method definition.

### Example:
```python
class Details:
	name = "Rohan"
	age = 20
	
	def desc(self):
	print("My name is", self.name, "and I'm", self.age, "years old.")

obj1 = Details()
obj1.desc()
```

### Output:
```python
My name is Rohan and I'm 20 years old.
```

## Main Example
```python
class Person:
  name = "Harry"
  occupation = "Software Developer"
  networth = 10
  def info(self):
    print(f"{self.name} is a {self.occupation}")


a = Person()
b = Person()
c = Person()

a.name = "Shubham"
a.occupation = "Accountant"

b.name = "Nitika"
b.occupation = "HR"

# print(a.name, a.occupation)
a.info()
b.info()
c.info()
```