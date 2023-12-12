---
{"dg-publish":true,"permalink":"/python-basics/basics-chapter-12-string-slicing-and-operations-on-string/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-12T00:05:46.253+05:30","updated":"2023-12-13T02:44:17.046+05:30"}
---

🧶 Tags - #Python_Basics 
Up - [[Python Basics/Basics Chapter 13 - String Method\|Basics Chapter 13 - String Method]]
Down - [[Python Basics/Basics Chapter 11 - Strings\|Basics Chapter 11 - Strings]]
🗃 Resources - [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
# [[Python Basics/Basics Chapter 12 - String Slicing & Operations on String\|Basics Chapter 12 - String Slicing & Operations on String]]
==2023-12-12 - 00:05==
## Length of a String
We can find the length of a string using len() function.
### Example:

```python
fruit = "Mango"
len1 = len(fruit)
print("Mango is a", len1, "letter word.")
```
### Output:
Mango is a 5 letter word.
## String as an array
A string is essentially a sequence of characters also called an array. Thus we can access the elements of this array.
### Example:
```python
pie = "ApplePie"
print(pie[:5])
print(pie[6])	#returns character at specified index
```
### Output:
```python
Apple
i
```
Note: This method of specifying the start and end index to specify a part of a string is called slicing.
## Slicing Example:
```python
pie = "ApplePie"
print(pie[:5]) #Slicing from Start
print(pie[5:]) #Slicing till End
print(pie[2:6]) #Slicing in between
print(pie[-8:]) #Slicing using negative index
```
### Output:
```python
Apple
Pie
pleP
ApplePie
```
# Loop through a String:
Strings are arrays and arrays are iterable. Thus we can loop through strings.
### Example:
```python
alphabets = "ABCDE"
for i in alphabets:
print(i)
```
### Output:
```python
A 
B
C
D
E
```
## Main Example
```python
fruit = "Mango"
mangoLen = len(fruit)
print(mangoLen)
print(fruit[0:4]) # including 0 but not 4
print(fruit[1:4]) # including 1 but not 4
print(fruit[:5])
print(fruit[0:-3])
print(fruit[:len(fruit)-3])
print(fruit[-1:len(fruit) - 3])
print(fruit[-3:-1])

# Quick Quiz:
nm = "Harry"
print(nm[-4:-2])

# Output
5
Mang
ang
Mango
Ma
Ma

ng
ar
```