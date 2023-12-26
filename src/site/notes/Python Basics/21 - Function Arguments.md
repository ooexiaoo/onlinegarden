---
{"dg-publish":true,"permalink":"/python-basics/21-function-arguments/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-20T18:13:40.822+05:30","updated":"2023-12-23T13:38:01.556+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/22 - Introduction to Lists\|22 - Introduction to Lists]]
Down:: [[Python Basics/20 - Functions in Python\|20 - Functions in Python]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-20 - 18:13==

There are four types of arguments that we can provide in a function:
- Default Arguments
- Keyword Arguments
- Variable length Arguments
- Required Arguments

### Default arguments:
We can provide a default value while creating a function. This way, the function assumes a default value even if a value is not provided in the function call for that argument.

#### Example:
```python
def name(fname, mname = "Jhon", lname = "Whatson"):
	print("Hello,", fname, mname, lname)
name("Amy")
```

#### Output:
```python
Hello, Amy Jhon Whatson
```

### Keyword arguments:
We can provide arguments with key = value, this way the interpreter recognizes the arguments by the parameter name. Hence, the order in which the arguments are passed does not matter.

#### Example:
```python
def name(fname, mname, lname):
	print("Hello,", fname, mname, lname)
	
name(mname = "Peter", lname = "Wesker", fname = "Jade")
```

### Output:
```python
Hello, Jade Peter Wesker
```

### Required arguments:
In case we don’t pass the arguments with a key = value syntax, then it is necessary to pass the arguments in the correct positional order and the number of arguments passed should match with actual function definition.

#### Example 1: when number of arguments passed does not match to the actual function definition.

```python
def name(fname, mname, lname):
	print("Hello,", fname, mname, lname)
	
name("Peter", "Quill")
```

#### Output:
```python
name("Peter", "Quill")\
TypeError: name() missing 1 required positional argument: 'lname'
```

#### Example 2: when the number of arguments passed matches to the actual function definition.

```python
def name(fname, mname, lname):
	print("Hello,", fname, mname, lname)
	
name("Peter", "Ego", "Quill")
```

#### Output:
```python
Hello, Peter Ego Quill
```

### Variable-length arguments:
Sometimes we may need to pass more arguments than those defined in the actual function. This can be done using variable-length arguments.

There are two ways to achieve this:

#### Arbitrary Arguments:

While creating a function, pass a * before the parameter name while defining the function. The function accesses the arguments by processing them in the form of tuple.

#### Example:

```python
def name(*name):
	print("Hello,", name[0], name[1], name[2])
	
name("James", "Buchanan", "Barnes")
```

#### Output:
```python
Hello, James Buchanan Barnes
```

#### Keyword Arbitrary Arguments:
While creating a function, pass a * before the parameter name while defining the function. The function accesses the arguments by processing them in the form of a dictionary.

#### Example:
```python
def name(**name):
	print("Hello,", name["fname"], name["mname"], name["lname"])
	
name(mname = "Buchanan", lname = "Barnes", fname = "James")
```

#### Output:

```python
Hello, James Buchanan Barnes
```

## Return Statement
The return statement is used to return the value of the expression back to the calling function.

#### Example:

```python
def name(fname, mname, lname):
	return "Hello, " + fname + " " + mname + " " + lname
	
print(name("James", "Buchanan", "Barnes"))
```

#### Output:
```python
Hello, James Buchanan Barnes
```