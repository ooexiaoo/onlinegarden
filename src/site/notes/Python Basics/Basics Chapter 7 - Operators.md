---
{"dg-publish":true,"permalink":"/python-basics/basics-chapter-7-operators/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-07T18:54:01.613+05:30","updated":"2023-12-10T19:50:34.697+05:30"}
---

🧶 Tags - #Python_Basics 
Up - [[Python Basics/Basics Chapter 1\|Basics Chapter 1]]
Down - [[Python Basics/Basics Chapter 9 - Typecasting in Python\|Basics Chapter 9 - Typecasting in Python]]

---
🗃 Resources - [YouTube Video](https://www.youtube.com/watch?v=FLVqcxnJP_E&list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg&index=7) | [My Repel](https://replit.com/@wolfr13/calculator#main.py)

# [[Python Basics/Basics Chapter 7 - Operators\|Basics Chapter 7 - Operators]]
==2023-12-07 - 18:54==

---
# Operators
Python has different types of operators for different operations. To create a calculator we require arithmetic operators.
# Arithmetic operators

|Operator|Operator Name|Example|
|---|---|---|
|+|`Addition`|`15+7`|
|-|`Subtraction`|`15-7`|
|*|`Multiplication`|`5*7`|
| ** | `Exponential` | `5**3` |
| / | `Division` | `5/3` |
| % | `Modulus` | `15%7` |
| // | `Floor Division` | `15//7` |

```python
n = 15
m = 7
ans1 = n+m
print("Addition of",n,"and",m,"is", ans1)
ans2 = n-m
print("Subtraction of",n,"and",m,"is", ans2)
ans3 = n*m
print("Multiplication of",n,"and",m,"is", ans3)
ans4 = n/m
print("Division of",n,"and",m,"is", ans4)
ans5 = n%m
print("Modulus of",n,"and",m,"is", ans5)
ans6 = n//m
print("Floor Division of",n,"and",m,"is", ans6)
```
# Explaination
Here 'n' and 'm' are two variables in which the integer value is being stored. Variables 'ans1' , 'ans2' ,'ans3', 'ans4','ans5' and 'ans6' contains the outputs corresponding to addition, subtraction,multiplication, division, modulus and floor division respectively.