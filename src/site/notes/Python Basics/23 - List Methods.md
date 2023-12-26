---
{"dg-publish":true,"permalink":"/python-basics/23-list-methods/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-22T17:07:07.190+05:30","updated":"2023-12-23T14:11:49.066+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/24 - Introduction to Tuples\|24 - Introduction to Tuples]]
Down:: [[Python Basics/22 - Introduction to Lists\|22 - Introduction to Lists]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-22 - 17:07==

## list.sort()
This method sorts the list in ascending order. The original list is updated

### Example 1:
```python
colors = ["voilet", "indigo", "blue", "green"]
colors.sort()
print(colors)

num = [4,2,5,3,6,1,2,1,2,8,9,7]
num.sort()
print(num)
```

### Output:
```python
['blue', 'green', 'indigo', 'voilet']\
[1, 1, 2, 2, 2, 3, 4, 5, 6, 7, 8, 9]
```

What if you want to print the list in descending order?  
We must give reverse=True as a parameter in the sort method.

### Example:
```python
colors = ["voilet", "indigo", "blue", "green"]
colors.sort(reverse=True)
print(colors)

num = [4,2,5,3,6,1,2,1,2,8,9,7]
num.sort(reverse=True)
print(num)
```

#### Output:
```python
['voilet', 'indigo', 'green', 'blue']
[9, 8, 7, 6, 5, 4, 3, 2, 2, 2, 1, 1]
```

The reverse parameter is set to False by default.

Note: Do not mistake the reverse parameter with the reverse method.

## reverse()
This method reverses the order of the list.

#### Example:
```python
colors = ["voilet", "indigo", "blue", "green"]
colors.reverse()
print(colors)

num = [4,2,5,3,6,1,2,1,2,8,9,7]
num.reverse()
print(num)
```

#### Output:
```python
['green', 'blue', 'indigo', 'voilet']
[7, 9, 8, 2, 1, 2, 1, 6, 3, 5, 2, 4]
```

## index()
This method returns the index of the first occurrence of the list item.

#### Example:
```python
colors = ["voilet", "green", "indigo", "blue", "green"]
print(colors.index("green"))

num = [4,2,5,3,6,1,2,1,3,2,8,9,7]
print(num.index(3))
```

Output:
```python
1
3
```

## count()
Returns the count of the number of items with the given value.

#### Example:
```python
colors = ["voilet", "green", "indigo", "blue", "green"]
print(colors.count("green"))

num = [4,2,5,3,6,1,2,1,3,2,8,9,7]
```

#### Output:
```python
2
3
```

## copy()
Returns copy of the list. This can be done to perform operations on the list without modifying the original list.

#### Example:
```python
colors = ["voilet", "green", "indigo", "blue"]
newlist = colors.copy()
print(colors)
print(newlist)
```

#### Output:
```python
['voilet', 'green', 'indigo', 'blue']
['voilet', 'green', 'indigo', 'blue']
```

## append():
This method appends items to the end of the existing list.

#### Example:
```python
colors = ["voilet", "indigo", "blue"]
colors.append("green")
print(colors)
```

#### Output:
```python
['voilet', 'indigo', 'blue', 'green']
```

## insert():
This method inserts an item at the given index. User has to specify index and the item to be inserted within the insert() method.

#### Example:
```python
colors = ["voilet", "indigo", "blue"]
#           [0]        [1]      [2]
colors.insert(1, "green")
#inserts item at index 1
# updated list: colors = ["voilet", "green", "indigo", "blue"]
#       indexs              [0]       [1]       [2]      [3]
print(colors)
```

#### Output:
```python
['voilet', 'green', 'indigo', 'blue']
```

## extend():
This method adds an entire list or any other collection datatype (set, tuple, dictionary) to the existing list.

#### Example 1:
```python
#add a list to a list
colors = ["voilet", "indigo", "blue"]
rainbow = ["green", "yellow", "orange", "red"]
colors.extend(rainbow)
print(colors)
```

#### Output:
```python
['voilet', 'indigo', 'blue', 'green', 'yellow', 'orange', 'red']
```

## Concatenating two lists:
You can simply concatenate two lists to join two lists.

#### Example:
```python
colors = ["voilet", "indigo", "blue", "green"]
colors2 = ["yellow", "orange", "red"]
print(colors + colors2)
```

#### Output:
```python
['voilet', 'indigo', 'blue', 'green', 'yellow', 'orange', 'red']
```

## Main Example
```python
l = [11, 45, 1, 2, 4, 6, 1, 1]
print(l)
# l.append(7)
# l.sort(reverse=True)
# l.reverse()
# print(l.index(1))
# print(l.count(1))
# m = l.copy()
# m[0] = 0
# l.insert(1, 899)
m = [900, 1000, 1100]
k = l + m
# print(k)
# l.extend(m)
print(l)
```