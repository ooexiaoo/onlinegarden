---
{"dg-publish":true,"permalink":"/python-basics/28-f-strings/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-26T13:42:24.862+05:30","updated":"2023-12-26T13:47:07.652+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Python Basics/27 - Exercise 3\|27 - Exercise 3]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-26 - 13:42==

## String formatting in python
String formatting can be done in python using the format method.

```python
txt = "For only {price:.2f} dollars!"  print(txt.format(price = 49))
```

### f-strings in python
It is a new string formatting mechanism introduced by the PEP 498. It is also known as Literal String Interpolation, or more commonly as F-strings (f character preceding the string literal). The primary focus of this mechanism is to make the interpolation easier.

When we prefix the string with the letter 'f', the string becomes the f-string itself. The f-string can be formatted in much the same as the str.format() method. The f-string offers a convenient way to embed a Python expression inside string literals for formatting.

#### Example
```python
val = 'Geeks'
print(f"{val}for{val} is a portal for {val}.")
name = 'Tushar'
age = 23
print(f"Hello, My name is {name} and I'm {age} years old.")
```

#### Output:
```python
Hello, My name is Tushar and I'm 23 years old.
```

In the above code, we have used the f-string to format the string. It evaluates at runtime; we can put all valid Python expressions in them.

We can use it in a single statement as well.

#### Example
```python
print(f"{2 * 30})"
```

#### Output:
```python
60
```

## Main Tutorial
```python
letter = "Hey my name is {1} and I am from {0}"
country = "India"
name = "Harry"

print(letter.format(country, name))
print(f"Hey my name is {name} and I am from {country}")
print(f"We use f-strings like this: Hey my name is {{name}} and I am from {{country}}")
price = 49.09999
txt = f"For only {price:.2f} dollars!"
print(txt)
# print(txt.format())
print(type(f"{2 * 30}"))
```