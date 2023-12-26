---
{"dg-publish":true,"permalink":"/python-basics/17-for-loops/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-17T18:21:59.877+05:30","updated":"2023-12-23T13:37:36.603+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/18 - While Loops\|18 - While Loops]]
Down:: [[Python Basics/16 - Match Case Statements\|16 - Match Case Statements]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-17 - 18:22==

Sometimes a programmer wants to execute a group of statements a certain number of times. This can be done using loops. Based on this, loops are further classified into following main types;
- for loop
- while loop

## The for loop
for loops can iterate over a sequence of iterable objects in python. Iterating over a sequence is nothing but iterating over strings, lists, tuples, sets and dictionaries.

### Example: iterating over a string:
```python
name = 'Abhishek'
for i in name:
	print(i, end=", ")
```

### Output:
A, b, h, i, s, h, e, k,

## Example: iterating over a list:
```python
colors = ["Red", "Green", "Blue", "Yellow"]
for x in colors:
	print(x)
```

### Output:
Red  
Green  
Blue  
Yellow

Similarly, we can use loops for lists, sets and dictionaries.

## range():
What if we do not want to iterate over a sequence? What if we want to use for loop for a specific number of times?

Range has 3 parameters: **Start, Stop, and Step.**

#### Start
Is from where the numbers start. If you add *for K in range(0, 5)*. The range will start from **0**.
#### Stop
Is where the number stops. If you add *for K in range(0,5)*. The range will stop at **4**. Yes! 4 not 5. It always stops at a number before what you entered. As the number you entered will not be added to the list.

#### Step
Is the number of steps it skips. If you add *for K in range(0,10,2)*. You will see **0,2,4,6,8** same as stop it will never print 10 as we've told the program to stop at it reaches 10.

Here, we can use the range() function.
## Example:
```python
for k in range(5):
	print(k)
```

### Output:
0 
1 
2 
3 
4 
Here, we can see that the loop starts from 0 by default and increments at each iteration.

But we can also loop over a specific range.

## Example:
```python
for k in range(4,9):
	print(k)
```

### Output:
4  
5  
6  
7  
8

## Quick Quiz
Explore about third parameter of range (ie range(x, y, z))

### Example:
```python
for k in range(1, 12, 3):
	print(k)
```