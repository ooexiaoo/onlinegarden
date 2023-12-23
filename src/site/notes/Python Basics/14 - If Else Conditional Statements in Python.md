---
{"dg-publish":true,"permalink":"/python-basics/14-if-else-conditional-statements-in-python/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-13T22:59:30.967+05:30","updated":"2023-12-23T13:37:18.676+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/15 - Exercise 2\|15 - Exercise 2]]
Down:: [[Python Basics/13 - String Method\|13 - String Method]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-13 - 22:59==
## if-else Statements
Sometimes the programmer needs to check the evaluation of certain expression(s), whether the expression(s) evaluate to True or False. If the expression evaluates to False, then the program execution follows a different path than it would have if the expression had evaluated to True.

Based on this, the conditional statements are further classified into following types:
- if
- if-else
- if-else-elif
- nested if-else-elif.
### An if……else statement evaluates like this:
#### if the expression evaluates True:
Execute the block of code inside if statement. After execution return to the code out of the if……else block.
#### if the expression evaluates False:
Execute the block of code inside else statement. After execution return to the code out of the if……else block.
### Example:
```python
applePrice = 210
budget = 200  if (applePrice <= budget):
print("Alexa, add 1 kg Apples to the cart.")  else:
print("Alexa, do not add Apples to the cart.")
```

### Output:
```python
Alexa, do not add Apples to the cart.
```

### Main Example - myif.py
```python
a = int(input("Enter your age: "))
print("Your age is:", a)
# Conditional operators 
# >, <, >=, <=, ==, !=
# print(a>18)
# print(a<=18)
# print(a==18)
# print(a!=18)
if(a>18):
  print("You can drive")
  print("Yes")
else:
  print("You cannot drive")
  print("No")
  print("Yay!")
```
## elif Statements
Sometimes, the programmer may want to evaluate more than one condition, this can be done using an elif statement.
### Working of an elif statement
Execute the block of code inside if statement if the initial expression evaluates to True. After execution return to the code out of the if block.

Execute the block of code inside the first elif statement if the expression inside it evaluates True. After execution return to the code out of the if block.

Execute the block of code inside the second elif statement if the expression inside it evaluates True. After execution return to the code out of the if block.  
.  
.  
.  
Execute the block of code inside the nth elif statement if the expression inside it evaluates True. After execution return to the code out of the if block.

Execute the block of code inside else statement if none of the expression evaluates to True. After execution return to the code out of the if block.
### Example:
```python
num = 0
if (num < 0):
	print("Number is negative.")
elif (num == 0):
	print("Number is Zero.")
else:
	print("Number is positive.")
```
### Output:
```python
Number is Zero.
```
### Main Example - if-else.py
```python
applePrice = 10
budget = 200
if (budget - applePrice > 50):
    print("Alexa, add 1 kg Apples to the cart.")
else:
    print("Alexa, do not add Apples to the cart.")
```

### Main Example - elif.py
```python
num = int(input("Enter the value of num: "))
if (num < 0):
  print("Number is negative.")
elif (num == 0):
  print("Number is Zero.")
elif (num == 999):
  print("Number is Special.")
else:
  print("Number is positive.")

print("I am happy now")
```
# Nested if statements
We can use if, if-else, elif statements inside other if statements as well.  
### Example:
```python
num = 18
if (num < 0):
	print("Number is negative.")
elif (num > 0):
	if (num <= 10):
		print("Number is between 1-10")
	elif (num > 10 and num <= 20):
		print("Number is between 11-20")
	else:
		print("Number is greater than 20")
else:
	print("Number is zero")
```
### Output:
```python
Number is between 11-20
```

## Here's What I Wrote:
```python
a = (input("what do you like to watch: "))
print("You like to watch:", a)
if a in ["anime", "manga", "manhwa"]:
    print("There's a high chance that you're an Otaku\nGod bless your soul!")
elif a in ["movies", "bollywood", "hollywood"]:
    print("You might be a normie, I personally don't like people like you!\nGet out of my site this instant!")
else:
    print("😵‍💫")
```