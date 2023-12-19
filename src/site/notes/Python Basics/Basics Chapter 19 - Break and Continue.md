---
{"dg-publish":true,"permalink":"/python-basics/basics-chapter-19-break-and-continue/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-19T11:27:18.786+05:30","updated":"2023-12-19T11:33:34.100+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Python Basics/Basics Chapter 18 - While Loops\|Basics Chapter 18 - While Loops]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-19 - 11:27==

## Break Statement
The break statement enables a program to skip over a part of the code. A break statement terminates the very loop it lies within.
### Example
```python
for i in range(1,101,1):
	print(i ,end=" ")
	if(i==50):
		break
	else:
		print("Mississippi")
print("Thank you")
```
### output
```python
1 Mississippi
2 Mississippi
3 Mississippi
4 Mississippi
5 Mississippi
.
.
.
50 Mississippi
```

## Continue Statement
The continue statement skips the rest of the loop statements and causes the next iteration to occur.

### Example
```python
for i in [2,3,4,6,8,0]:
	if (i%2!=0):
		continue
	print(i)
```
### output
```python
2
4
6
8
0
```

## Main Example
```python
# for i in range(12):
#   if(i == 10):
#     print("Skip the iteration")
#     continue
#   print("5 X", i, "=", 5 * i)
  
i = 0
while True:
  print(i)
  i = i + 1
  if(i%100 == 0):
    break

```