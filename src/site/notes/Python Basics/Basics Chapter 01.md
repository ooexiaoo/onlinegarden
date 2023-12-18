---
{"dg-publish":true,"permalink":"/python-basics/basics-chapter-01/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-05T16:52:10.639+05:30","updated":"2023-12-18T20:46:54.161+05:30"}
---

🧶 Tags:: #Python_Basics
Down:: [[Python Basics/Basics Chapter 06\|Basics Chapter 06]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-05 | 16:52==

#### 1st code
```python
Print("Hello World")

# Result - Hello World
```
#### Escape Sequence Character and Comment
- To create a new line we use **backslash n**, you don't need to leave spaces around backslash n as well.
- To add a comment, just use a **"#"**. Or to comment out multiple lines, just use **(''')** triple single quotes or triple double quotes.
```python
print("Hey!\nHow are you doing")

# Hey!
#	  How are you doing

'''
Multi
line
comment
'''

"""
Multi
line
comment
"""
```

#### Double Quote Escape Sequence Character
- So to add double quotes inside double quotes all you need to use is a backslash \
- An escape sequence character is a backslash followed by the character you want to insert.
```python
print("Hello, this is \"Varun\"\nand I'm trying to learn Python")

# Hello, this is "Varun
# and I'm trying to learn Python
```

#### Separator
- Separator is used to separate multiple values with what ever you've added, like we added ~ in the example below.
- Similarly end='end' specify what to print at the end. Default is '\n' (line feed).
- File: An object with a write method. Default is sys.stdout.
- Remember that 2 to 4 are optional, You don't really need to use them, but are there if you need them for some reason.
```python
print("Hey", 6, 7, sep="~")

# Hey~6~7

print("Hey", 6, 7, sep="~", end="009\n")
print("Varun")
# Hey~6~7009
# Varun

print("Hey", 6, 7, sep="~", end="009\n")
print("Varun")
# Hey~6~7009
# Varun
```