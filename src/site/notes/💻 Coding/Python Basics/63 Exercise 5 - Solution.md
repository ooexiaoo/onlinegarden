---
{"dg-publish":true,"permalink":"/coding/python-basics/63-exercise-5-solution/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-02-15T18:29:02.591+05:30","updated":"2024-02-15T18:33:19.751+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[💻 Coding/Python Basics/64 - Exercise 6\|64 - Exercise 6]]
Down:: [[💻 Coding/Python Basics/62 - Access Specifiers\|62 - Access Specifiers]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-02-15 - 18:29==

Snake, Water and Gun is a variation of the children's game "rock-paper-scissors" where players use hand gestures to represent a snake, water, or a gun. The gun beats the snake, the water beats the gun, and the snake beats the water. Write a python program to create a Snake Water Gun game in Python using if-else statements. Do not create any fancy GUI. Use proper functions to check for win.

```python
import random

def check(comp, user):
  if comp ==user:
    return 0
    
  if(comp == 0 and user ==1):
    return -1
    
  if(comp == 1 and user ==2):
    return -1
    
  if(comp == 2 and user == 0):
    return -1

  return 1
    
  
comp = random.randint(0, 2)
user = int(input("0 for Snake, 1 for water and 2 for Gun:\n"))

score = check(comp, user)

print("You: ", user)
print("Computer: ", comp)

if(score == 0):
  print("Its a draw")
elif (score == -1):
  print("You Lose")
else:
  print("You Won")
```