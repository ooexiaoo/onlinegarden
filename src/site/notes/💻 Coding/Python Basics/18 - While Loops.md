---
{"dg-publish":true,"permalink":"/coding/python-basics/18-while-loops/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-18T17:42:47.107+05:30","updated":"2023-12-23T13:37:43.395+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[💻 Coding/Python Basics/19 - Break and Continue\|19 - Break and Continue]]
Down:: [[💻 Coding/Python Basics/17 - For Loops\|17 - For Loops]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-18 - 17:42==

As the name suggests, while loops execute statements while the condition is True. As soon as the condition becomes False, the interpreter comes out of the while loop.
## Example:
```python
count = 5
while (count > 0):
print(count)
count = count - 1
```
### Output:
```python
5
4
3
2
1
```
Here, the count variable is set to 5 which decrements after each iteration. Depending upon the while loop condition, we need to either increment or decrement the counter variable (the variable count, in our case) or the loop will continue forever.

## Else with While Loop
We can even use the else statement with the while loop. Essentially, what the else statement does is that as soon as the while loop condition becomes False, the interpreter comes out of the while loop and the else statement is executed.

### Example:
```python
x = 5
while (x > 0):
	print(x)
	x = x - 1
else:
	print('counter is 0')
```

### Output:
```python
5
4
3
2
1
counter is 0
```
## Do-While Loop
do..while is a loop in which a set of instructions will execute at least once (irrespective of the condition) and then the repetition of the loop's body will depend on the condition passed at the end of the while loop. It is also known as an exit-controlled loop.

## How to emulate do while loop in python?
To create a do while loop in Python, you need to modify the while loop a bit in order to get similar behavior to a do while loop.

The most common technique to emulate a do-while loop in Python is to use an infinite while loop with a break statement wrapped in an if statement that checks a given condition and breaks the iteration if that condition becomes true:

### Example
```python
while True:
	number = int(input("Enter a positive number: "))
	print(number)
	if not number > 0:
		break
```

### Output
```python
Enter a positive number: 1 
1
Enter a positive number: 4
4
Enter a positive number: -1
-1
```

## Explanation
This loop uses True as its formal condition. This trick turns the loop into an infinite loop. Before the conditional statement, the loop runs all the required processing and updates the breaking condition. If this condition evaluates to true, then the break statement breaks out of the loop, and the program execution continues its normal path.