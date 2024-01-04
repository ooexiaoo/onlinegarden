---
{"dg-publish":true,"permalink":"/python-basics/35-for-loop-with-else/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-03T18:49:22.307+05:30","updated":"2024-01-04T17:02:04.568+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/36 - Exception Handling\|36 - Exception Handling]]
Down:: [[Python Basics/34 - Dictionary Methods\|34 - Dictionary Methods]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-03 - 18:49==

As you have learned before, the else clause is used along with the if statement.

Python allows the else keyword to be used with the for and while loops too. The else block appears after the body of the loop. The statements in the else block will be executed after all iterations are completed. The program exits the loop only after the else block is executed.

### Syntax
`   for counter in sequence:      #Statements inside for loop block  else:      #Statements inside else block   `

#### Example:
```python
for x in range(5):
	print ("iteration no {} in for loop".format(x+1))
else:
	print ("else block in loop")
print ("Out of loop")
```

#### Output:
```python
iteration no 1 in for loop
iteration no 2 in for loop
iteration no 3 in for loop
iteration no 4 in for loop
iteration no 5 in for loop
else block in loop
Out of loop
```

## Main Example
```python
i = 0
while i<7:
  print(i)
  i = i + 1
  # if i == 4:
  #   break

else:
  print("Sorry no i")

for x in range(5):
    print ("iteration no {} in for loop".format(x+1))
else:
    print ("else block in loop")
print ("Out of loop")
```