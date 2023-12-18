---
{"dg-publish":true,"permalink":"/python-basics/basics-chapter-16-match-case-statements/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-16T11:40:24.432+05:30","updated":"2023-12-18T20:44:53.049+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/Basics Chapter 17 - For Loops\|Basics Chapter 17 - For Loops]]
Down:: [[Python Basics/Basics Chapter 15 - Exercise 2\|Basics Chapter 15 - Exercise 2]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-16 - 11:40==

To implement switch-case like characteristics very similar to if-else functionality, we use a match case in python. If you are coming from a C, C++ or Java like language, you must have heard of switch-case statements. If this is your first language, don't worry, as I will tell you everything you need to know about match case statements in this video!

A match statement will compare a given variable’s value to different shapes, also referred to as the pattern. The main idea is to keep on comparing the variable with all the present patterns until it fits into one.

The match case consists of three main entities :
1. The match keyword
2. One or more case clauses
3. Expression for each case

The case clause consists of a pattern to be matched to the variable, a condition to be evaluated if the pattern matches, and a set of statements to be executed if the pattern matches.

## Syntax:
```python
match variable_name:
	case ‘pattern1’ : //statement1
	case ‘pattern2’ : //statement2
	…
	case ‘pattern n’ : //statement n
```

### Example:
```python
x = 4
# x is the variable to match
match x:
	# if x is 0
	case 0:
		print("x is zero")
	# case with if-condition
	case 4 if x % 2 == 0:
		print("x % 2 == 0 and case is 4")
		# Empty case with if-condition
		case _ if x < 10:
			print("x is < 10")
		# default case(will only be matched if the above cases were not matched)
		# so it is basically just an else:
		case _:
			print(x)
```
### Output:

```python
x % 2 == 0 and case is 4
```

### Main Example
```python
x = int(input("Enter the value of x: "))
# x is the variable to match
match x:
    # if x is 0
    case 0:
        print("x is zero")
    # case with if-condition
    case 4:
        print("case is 4")

    case _ if x!=90:
        print(x, "is not 90")
    case _ if x!=80:
        print(x, "is not 80")
    case _:
        print(x)
```

#### Here's an example to illustrate the difference between `if-else` and `match`:
##### Using `if-else`:
```python
# Using if-else
def check_value(value):
    if value == 1:
        print("Value is 1")
    elif value == 2:
        print("Value is 2")
    else:
        print("Value is something else")

check_value(2)
```

##### Using `match` (Python 3.10 and later):
```python
# Using match
def check_value(value):
    match value:
        case 1:
            print("Value is 1")
        case 2:
            print("Value is 2")
        case _:
            print("Value is something else")

check_value(2)
```