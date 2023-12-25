---
{"dg-publish":true,"permalink":"/python-basics/25-operations-on-tuples/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-24T21:24:56.198+05:30","updated":"2023-12-25T20:35:15.260+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/27 - Exercise 3\|27 - Exercise 3]]
Down:: [[Python Basics/24 - Introduction to Tuples\|24 - Introduction to Tuples]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-24 - 21:25==

## Manipulating Tuples
Tuples are immutable, hence if you want to add, remove or change tuple items, then first you must convert the tuple to a list. Then perform operation on that list and convert it back to tuple.

#### Example:
```python
countries = ("Spain", "Italy", "India", "England", "Germany")
temp = list(countries)
temp.append("Russia")       #add item
temp.pop(3)                 #remove item
temp[2] = "Finland"         #change item
countries = tuple(temp)  print(countries)   `
```

#### Output:
```python
('Spain', 'Italy', 'Finland', 'Germany', 'Russia')
```

Thus, we convert the tuple to a list, manipulate items of the list using list methods, then convert the list back to a tuple.

However, we can directly concatenate two tuples without converting them to list.

#### Example:
```python
countries = ("Pakistan", "Afghanistan", "Bangladesh", "ShriLanka")
countries2 = ("Vietnam", "India", "China")
southEastAsia = countries + countries2
print(southEastAsia)
```

#### Output:
```python
('Pakistan', 'Afghanistan', 'Bangladesh', 'ShriLanka', 'Vietnam', 'India', 'China')
```

## Tuple methods
As tuple is immutable type of collection of elements, it has limited built in methods. They are explained below

## count() Method
The count() method of Tuple returns the number of times the given element appears in the tuple.

### Syntax:
```python
tuple.count(element)
```

### Example
```python
Tuple1 = (0, 1, 2, 3, 2, 3, 1, 3, 2)
res = Tuple1.count(3)
print('Count of 3 in Tuple1 is:', res)
```

### Output
```python
3
```

## index() method
The Index() method returns the first occurrence of the given element from the tuple.

### Syntax:
```python
tuple.index(element, start, end)
```

Note: This method raises a ValueError if the element is not found in the tuple.

### Example
```python
Tuple = (0, 1, 2, 3, 2, 3, 1, 3, 2)
res = Tuple.index(3)
print('First occurrence of 3 is', res)
```

#### Output
```python
3
```