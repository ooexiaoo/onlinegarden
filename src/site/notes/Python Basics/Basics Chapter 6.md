---
{"dg-publish":true,"permalink":"/python-basics/basics-chapter-6/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-06T18:06:58.259+05:30","updated":"2023-12-15T07:15:51.968+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/Basics Chapter 1\|Basics Chapter 1]]
Down::: [[Python Basics/Basics Chapter 7 - Operators\|Basics Chapter 7 - Operators]]
🗃 Resources - [YouTube Video](https://www.youtube.com/watch?v=ORCuz7s5cCY&list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg&index=6) | [Replit Chapter 06](https://replit.com/@codewithharry/06-Day6-Variables-and-Data-Types#main.py)
# [[Python Basics/Basics Chapter 6\|Basics Chapter 6]]
==2023-12-06 - 18:07==

---
## What is a variable?
Variable is like a container that holds data. Very similar to how our containers in kitchen holds sugar, salt etc. Creating a variable is like creating a placeholder in memory(RAM) and assigning it some value. In Python its as easy as writing:

```python
a = 1  b = True  c = "Varun"  d = None
```

These are four variables of different data types.
## What is a Data Type?

Data type specifies the type of value a variable holds. This is required in programming to do various operations without causing an error. Refer [[💻 JavaScript Course/JavaScript In depth Course Notes/Primitives and Objects\|Primitives and Objects]] to see other data types.
In python, we can print the type of any operator using type function:

```python
a = 1  print(type(a))  b = "1"  print(type(b))
```

By default, python provides the following built-in data types:
## 1. Numeric data: int, float, complex
- int: 3, -8, 0
- float: 7.349, -9.0, 0.0000001
- complex: 6 + 2i
## 2. Text data: str
str: "Hello World!!!", "Python Programming"
## 3. Boolean data:
Boolean data consists of values True or False.
## 4. Sequenced data: list, tuple
**list:** A list is an ordered collection of data with elements separated by a comma and enclosed within square brackets. Lists are mutable and can be modified after creation.

**Example:**
```python
list1 = [8, 2.3, [-4, 5], ["apple", "banana"]]  print(list1)
```

Output:
```python
[8, 2.3, [-4, 5], ['apple', 'banana']]
```

**Tuple:** A tuple is an ordered collection of data with elements separated by a comma and enclosed within parentheses. Tuples are immutable and can not be modified after creation.

**Example:**
```python
tuple1 = (("parrot", "sparrow"), ("Lion", "Tiger"))  print(tuple1)
```

Output:
```python
(('parrot', 'sparrow'), ('Lion', 'Tiger'))
```

## 5. Mapped data: dict
**dict:** A dictionary is an unordered collection of data containing a key:value pair. The key:value pairs are enclosed within curly brackets.

**Example:**
```python
dict1 = {"name":"Sakshi", "age":20, "canVote":True}  print(dict1)
```
Output:
```python
{'name': 'Sakshi', 'age': 20, 'canVote': True}
```