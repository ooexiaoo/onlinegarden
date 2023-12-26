---
{"dg-publish":true,"permalink":"/python-basics/15-exercise-2/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-15T07:20:14.633+05:30","updated":"2023-12-23T13:37:24.658+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/16 - Match Case Statements\|16 - Match Case Statements]]
Down:: [[Python Basics/14 - If Else Conditional Statements in Python\|14 - If Else Conditional Statements in Python]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg) | [Understand Time Module in Python](https://realpython.com/python-time-module/)
==2023-12-15 - 07:20==
### Exercise 2: Good Morning Sir
Create a python program capable of greeting you with Good Morning, Good Afternoon and Good Evening.

Your program should use time module to get the current hour. Here is a sample program and documentation link for you:


#### Import time and Print HH:MM:SS
```python
import time
timestamp = time.strftime('%H:%M:%S')
print(timestamp)
timestamp = time.strftime('%H')
print(timestamp)
timestamp = time.strftime('%M')
print(timestamp)
timestamp = time.strftime('%S')
print(timestamp)
# https://docs.python.org/3/library/time.html#time.strftime
```

So the challenge was to write a program that will say use the appropriate sentence, **"Good morning", "Good afternoon", "Good evening", or "Good night"**. depending on the time it is.

Harry Bhai challenged the viewers to write our own code with just the hint provided above which is import time code and said you should use **Integer value**. So after some thinking I wrote this

```python
import time
# timestamp = time.strftime('%H:%M:%S')
# print(timestamp)
# timestamp = time.strftime('%H')
# print(timestamp)
# timestamp = time.strftime('%M')
# print(timestamp)
# timestamp = time.strftime('%S')
# print(timestamp)

hour = (int(time.strftime('%H%M%S')))
	if (hour > 040000 and hour < 115959):
	print("Good morning Exia")
elif (hour >= 120000 and hour <= 155959):
	print("Good afternoon Exia")
elif (hour >= 160000 and hour > 185959):
	print("Good evening Exia")
else:
	print("Good night Exia")

# print(time.strftime('%H%M%S'))
```

As you can see I used the **print(time.strftime('%H%M%S'))** to see if we can print the time as an **integer** without using **":"** as separators. Once I could see that we can do it, everything else was not that hard to do I did have to refer to [[Python Basics/14 - If Else Conditional Statements in Python\|yesterday's tutorial]] about **elif and else**.

Other than that, it was fun to do it.

## The Right Answer
```python
import time

hour = int(time.strftime('%H'))

if 4 <= hour < 12:
    print("Good morning")
elif 12 <= hour < 17:
    print("Good afternoon")
elif 17 <= hour < 20:
    print("Good evening")
else:
    print("Good night")

```

Well, this is just better code. I didn't think about this.