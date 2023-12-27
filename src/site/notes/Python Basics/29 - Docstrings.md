---
{"dg-publish":true,"permalink":"/python-basics/29-docstrings/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-27T22:21:33.715+05:30","updated":"2023-12-27T22:30:39.402+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Python Basics/28 - F Strings\|28 - F Strings]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-27 - 22:21==

## Docstrings
Python docstrings are the string literals that appear right after the definition of a function, method, class, or module.

#### Example
```python
def square(n):
	'''Takes in a number n, returns the square of n'''
	print(n**2)
square(5)
```

Here,

'''Takes in a number n, returns the square of n''' is a docstring which will not appear in output

#### Output:
```python
25
```

Here is another example:
```python
def add(num1, num2):
	"""
	Add up two integer numbers.
	This function simply wraps the ``+`` operator, and does not      do anything interesting, except for illustrating what      the docstring of a very simple function looks like.
	Parameters
	----------
	num1 : int
		First number to add.
	num2 : int
		Second number to add.
		
		Returns
		-------
		int
			The sum of ``num1`` and ``num2``.
			
		See Also
		--------
		subtract : Subtract one integer from another.
		
		Examples
		--------
		>>> add(2, 2)
		4
		>>> add(25, 0)
		25
		>>> add(10, -10)
		0
		"""
		return num1 + num2
```

### Python Comments vs Docstrings

#### Python Comments
Comments are descriptions that help programmers better understand the intent and functionality of the program. They are completely ignored by the Python interpreter.

#### Python docstrings
As mentioned above, Python docstrings are strings used right after the definition of a function, method, class, or module (like in Example 1). They are used to document our code.

We can access these docstrings using the **doc** attribute.

### Python **doc** attribute
Whenever string literals are present just after the definition of a function, module, class or method, they are associated with the object as their **doc** attribute. We can later use this attribute to retrieve this docstring.

#### Example
```python
def square(n):
'''Takes in a number n, returns the square of n'''
	return n**2
print(square.__doc__)
```

#### Output:
```python
Takes in a number n, returns the square of n
```

## PEP 8
PEP 8 is a document that provides guidelines and best practices on how to write Python code. It was written in 2001 by Guido van Rossum, Barry Warsaw, and Nick Coghlan. The primary focus of PEP 8 is to improve the readability and consistency of Python code.

PEP stands for Python Enhancement Proposal, and there are several of them. A PEP is a document that describes new features proposed for Python and documents aspects of Python, like design and style, for the community.

### The Zen of Python
Long time Pythoneer Tim Peters succinctly channels the BDFL’s guiding principles for Python’s design into 20 aphorisms, only 19 of which have been written down.

```python
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.  Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

### Easter egg
```python
import this
```