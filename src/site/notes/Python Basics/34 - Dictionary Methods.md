---
{"dg-publish":true,"permalink":"/python-basics/34-dictionary-methods/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-01T16:55:51.521+05:30","updated":"2024-01-01T17:02:14.321+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-01 - 16:55==

Dictionary uses several built-in methods for manipulation.They are listed below

## update()
The update() method updates the value of the key provided to it if the item already exists in the dictionary, else it creates a new key-value pair.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True}
print(info)
info.update({'age':20})
info.update({'DOB':2001})
print(info)
```

#### Output:
```python
{'name': 'Karan', 'age': 19, 'eligible': True}
{'name': 'Karan', 'age': 20, 'eligible': True, 'DOB': 2001}
```

## Removing items from dictionary:
There are a few methods that we can use to remove items from dictionary.

### clear():
The clear() method removes all the items from the list.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True}
info.clear()
print(info)
```

#### Output:
```python
{}
```

#### pop():
The pop() method removes the key-value pair whose key is passed as a parameter.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True}
info.pop('eligible')
print(info)
```

#### Output:
```python
{'name': 'Karan', 'age': 19}
```

### popitem():
The popitem() method removes the last key-value pair from the dictionary.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True, 'DOB':2003}  info.popitem()  print(info)
```

#### Output:
```python
{'name': 'Karan', 'age': 19, 'eligible': True}
```

### del:
we can also use the del keyword to remove a dictionary item.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True, 'DOB':2003}
del info['age']
print(info)
```

#### Output:
```python
{'name': 'Karan', 'eligible': True, 'DOB': 2003}
```

If key is not provided, then the del keyword will delete the dictionary entirely.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True, 'DOB':2003}
del info
print(info)
```

#### Output:
```python
NameError: name 'info' is not defined
```

## Main Example
```python
ep1 = {122: 45, 123: 89, 567: 69, 670: 69}
ep2 = {222: 67, 566: 90}

# ep1.update(ep2)
# ep1.clear()
# ep1.pop(122)
ep1.popitem()
del ep1[122]
print(ep1)
```