---
{"dg-publish":true,"permalink":"/python-basics/42-enumerate/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-12T16:00:15.896+05:30","updated":"2024-01-12T16:10:20.570+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Python Basics/41 - Short Hand if else\|41 - Short Hand if else]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-12 - 16:00==

The enumerate function is a built-in function in Python that allows you to loop over a sequence (such as a list, tuple, or string) and get the index and value of each element in the sequence at the same time. Here's a basic example of how it works:
```python
# Loop over a list and print the index and value of each element
fruits = ['apple', 'banana', 'mango']
for index, fruit in enumerate(fruits):
	print(index, fruit)
```

The output of this code will be:
```python
0 apple
1 banana
2 mango
```

As you can see, the enumerate function returns a tuple containing the index and value of each element in the sequence. You can use the for loop to unpack these tuples and assign them to variables, as shown in the example above.

## Changing the start index
By default, the enumerate function starts the index at 0, but you can specify a different starting index by passing it as an argument to the enumerate function:
```python
# Loop over a list and print the index (starting at 1) and value of each element
fruits = ['apple', 'banana', 'mango']
for index, fruit in enumerate(fruits, start=1):
	print(index, fruit)
```

This will output:
```python
1 apple
2 banana
3 mango
```

The enumerate function is often used when you need to loop over a sequence and perform some action with both the index and value of each element. For example, you might use it to loop over a list of strings and print the index and value of each string in a formatted way:
```python
fruits = ['apple', 'banana', 'mango']
for index, fruit in enumerate(fruits):
	print(f'{index+1}: {fruit}')
```

This will output:
```python
1: apple
2: banana
3: mango
```

In addition to lists, you can use the enumerate function with any other sequence type in Python, such as tuples and strings. Here's an example with a tuple:
```python
# Loop over a tuple and print the index and value of each element
colors = ('red', 'green', 'blue')
for index, color in enumerate(colors):
	print(index, color)
```

And here's an example with a string:
```python
# Loop over a string and print the index and value of each character
s = 'hello'  for index, c in enumerate(s):
print(index, c)
```

## Main Example
```python
marks = [12, 56, 32, 98, 12,  45, 1, 4]

# index = 0
# for mark in marks:
#   print(mark)
#   if(index == 3):
#     print("Harry, awesome!")
#   index +=1

for index, mark in enumerate(marks, start=1):
  print(mark)
  if(index == 3):
    print("Harry, awesome!")
```