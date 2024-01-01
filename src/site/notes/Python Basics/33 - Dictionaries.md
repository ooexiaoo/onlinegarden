---
{"dg-publish":true,"permalink":"/python-basics/33-dictionaries/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-31T00:01:59.793+05:30","updated":"2024-01-01T17:00:27.359+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/34 - Dictionary Methods\|34 - Dictionary Methods]]
Down:: [[Python Basics/32 -  Set Methods\|32 -  Set Methods]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-31 - 00:02==

Dictionaries are an ordered collection of data items. They store multiple items in a single variable. Dictionary items are key-value pairs that are separated by commas and enclosed within curly brackets {}.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True}
print(info)
```

#### Output:
```python
{'name': 'Karan', 'age': 19, 'eligible': True}
```

## Accessing Dictionary items:
### I. Accessing single values:
Values in a dictionary can be accessed using keys. We can access dictionary values by mentioning keys either in square brackets or by using get method.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True}
print(info['name'])
print(info.get('eligible'))
```

#### Output:
```python
Karan
True
```

### II. Accessing multiple values:
We can print all the values in the dictionary using values() method.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True}
print(info.values())
```

#### Output:
```python
dict_values(['Karan', 19, True])
```

### III. Accessing keys:
We can print all the keys in the dictionary using keys() method.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True}
print(info.keys())
```

#### Output:
```python
dict_keys(['name', 'age', 'eligible'])
```

### IV. Accessing key-value pairs:
We can print all the key-value pairs in the dictionary using items() method.

#### Example:
```python
info = {'name':'Karan', 'age':19, 'eligible':True}
print(info.items())
```

#### Output:
```python
dict_items([('name', 'Karan'), ('age', 19), ('eligible', True)])
```

## Main Example
```python
info = {'name':'Karan', 'age':19, 'eligible':True}
# print(info) 
# print(info.keys())
# print(info.values())

# for key in info.keys():
#   print(f"The value corresponding to the key {key} is {info[key]}")

print(info.items())
for key, value in info.items():
  print(f"The value corresponding to the key {key} is {value}") 
```