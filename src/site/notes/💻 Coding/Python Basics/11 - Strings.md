---
{"dg-publish":true,"permalink":"/coding/python-basics/11-strings/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-10T20:14:56.363+05:30","updated":"2023-12-26T12:28:31.110+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[💻 Coding/Python Basics/12 - String Slicing & Operations on String\|12 - String Slicing & Operations on String]]
Down:: [[💻 Coding/Python Basics/10 - Taking User Input\|10 - Taking User Input]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-10 - 20:15==
In python, anything that you enclose between single or double quotation marks is considered a string.

A string is essentially a sequence or array of textual data. Strings are used when working with Unicode characters.
## Example
```python
name = "Exia"
print("Hello, " + name)
```
## Output
Hello, Harry

Note: It does not matter whether you enclose your strings in single or double quotes, the output remains the same.

Sometimes, the user might need to put quotation marks in between the strings. Example, consider the sentence: He said, **“I want to eat an apple”**.

How will you print this statement in python?: `He said, "I want to eat an apple".` We will definitely use single quotes for our convenience

```python
print('He said, "I want to eat an apple".')
```
## Multiline Strings
If our string has multiple lines, we can create them like this:

```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)
```
## Accessing Characters of a String
In Python, string is like an array of characters. We can access parts of string by using its index which starts from 0.  
Square brackets can be used to access elements of the string.

```python
print(name[0])
print(name[1])
```
## Looping through the string
We can loop through strings using a for loop like this:
```python
for character in name:
print(character)
```
Above code prints all the characters in the string name one by one!