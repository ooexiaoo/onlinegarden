---
{"dg-publish":true,"permalink":"/python-basics/10-taking-user-input/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-09T20:48:32.218+05:30","updated":"2023-12-23T13:36:52.776+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/11 - Strings\|11 - Strings]]
Down:: [[Python Basics/09 - Typecasting in Python\|09 - Typecasting in Python]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-09 - 20:48==

In python, we can take user input directly by using input() function.This input function gives a return value as string/character hence we have to pass that into a variable
## Syntax:
```python
variable=input()
```
But input function returns the value as string. Hence we have to typecast them whenever required to another datatype.
## Example:
```python
variable=int(input())
variable=float(input())
```
We can also display a text using input function. This will make input() function take user input and display a message as well
## Example:
```python
a=input("Enter the name: ")
print(a)
```
## Output:
```python
Enter the name: Harry
Harry
```