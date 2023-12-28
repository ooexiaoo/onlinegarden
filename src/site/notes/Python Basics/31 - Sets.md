---
{"dg-publish":true,"permalink":"/python-basics/31-sets/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-28T19:58:16.260+05:30","updated":"2023-12-28T20:01:46.233+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Python Basics/30 - Recursion\|30 - Recursion]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-28 - 19:58==

Sets are an unordered collection of data items. They store multiple items in a single variable. Set items are separated by commas and enclosed within curly brackets {}. Sets are unchangeable, meaning you cannot change items of the set once created. Sets do not contain duplicate items.

#### Example:
```python
info = {"Carla", 19, False, 5.9, 19}
print(info)
```

#### Output:
```python
{False, 19, 5.9, 'Carla'}
```

Here we see that the items of set occur in random order, and hence they cannot be accessed using index numbers. Also, sets do not allow duplicate values.

**Quick Quiz:** Try to create an empty set. Check using the type() function whether the type of your variable is a set

## Accessing set items:
### Using a For loop
You can access items of set using a for loop.

#### Example:
```python
info = {"Carla", 19, False, 5.9}
for item in info:
	print(item)
```

#### Output:
```python
False
Carla
19
5.9
```

## Main Example
```python
s = {2, 4, 2, 6}
print(s)

info = {"Carla", 19, False, 5.9, 19}
print(info)

harry = set()
print(type(harry))

for value in info:
  print(value)
```