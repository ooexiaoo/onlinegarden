---
{"dg-publish":true,"permalink":"/python-basics/40-exercise-4/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-07T22:28:32.909+05:30","updated":"2024-01-09T13:25:31.292+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/41 - Short Hand if else\|41 - Short Hand if else]]
Down:: [[Python Basics/38 - Custom Errors\|38 - Custom Errors]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-07 - 22:28==

Write a python program to translate a message into secret code language. Use the rules below to translate normal English into secret code language

## Coding:
if the word contains at least 3 characters, remove the first letter and append it at the end now append three random characters at the starting and the end else: simply reverse the string

## Decoding:
if the word contains less than 3 characters, reverse it else: remove 3 random characters from start and end. Now remove the last letter and append it to the beginning

### Your program should ask whether you want to code or decode

## I can't do it :(
Here's what I saw others do. I'll work on this
```python
x=int(input("press 1 for ENCODE or any other number for DECODE :"))
if x == 1:  #Coding
    str = input("\nEnter the word to Code :")
    l = list(str)
    if len(str) >= 3:
        l2 = l[0]
        l = l[1:]
        l += l2
        rand = ['a', 'c', 'z']
        l += rand
        l[:0] = rand
        print("Output :",''.join(l),)
    else:
        l.reverse()
        print("Output :",''.join(l),)

#Decoding
else:
    str = input("\nEnter the word to Decode :")
    l = list(str)
    if len(str) <= 3:
        l.reverse()
        print("Output :",''.join(l),)
    else:
        l = l[3:-3]
        l2 = l.pop()
        l[:0] += l2
        print("Output :",''.join(l),)
```