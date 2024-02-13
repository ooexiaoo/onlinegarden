---
{"dg-publish":true,"permalink":"/coding/python-basics/60-getters-and-setters/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-02-12T11:38:50.444+05:30","updated":"2024-02-13T17:59:12.575+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Coding/Python Basics/61 - Inheritance in Python\|61 - Inheritance in Python]]
Down:: [[Coding/Python Basics/59 - Decorators in Python\|59 - Decorators in Python]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-02-12 - 11:38==

## Getters
Getters in Python are methods that are used to access the values of an object's properties. They are used to return the value of a specific property, and are typically defined using the @property decorator. Here is an example of a simple class with a getter method:
```python
class MyClass:
	def __init__(self, value):
		self._value = value

	@property
	def value(self):
		return self._value
```

In this example, the MyClass class has a single property, _value, which is initialized in the **init** method. The value method is defined as a getter using the @property decorator, and is used to return the value of the _value property.

To use the getter, we can create an instance of the MyClass class, and then access the value property as if it were an attribute:
```python
>>> obj = MyClass(10)
>>> obj.value
10
```

## Setters
It is important to note that the getters do not take any parameters and we cannot set the value through getter method.For that we need setter method which can be added by decorating method with @property_name.setter

Here is an example of a class with both getter and setter:
```python
class MyClass:
	def __init__(self, value):
		self._value = value

    @property
    def value(self):
	    return self._value

    @value.setter
    def value(self, new_value):
	    self._value = new_value
```

We can use setter method like this:
```python
>>> obj = MyClass(10)
>>> obj.value = 20
>>> obj.value
20
```

In conclusion, getters are a convenient way to access the values of an object's properties, while keeping the internal representation of the property hidden. This can be useful for encapsulation and data validation.

## Main Example
```python
class MyClass:
  def __init__(self, value):
      self._value = value
    
  def show(self):
    print(f"Value is {self._value}")
    
  @property
  def ten_value(self):
      return 10* self._value
    
  @ten_value.setter
  def ten_value(self, new_value):
      self._value = new_value/10

obj = MyClass(10)
obj.ten_value = 67
print(obj.ten_value)
obj.show()
```