---
{"dg-publish":true,"permalink":"/coding/python-basics/50-read-readlines-and-other-methods/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-28T23:25:58.348+05:30","updated":"2024-01-29T16:53:03.249+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[💻 Coding/Python Basics/51 - seek() and tell() functions\|51 - seek() and tell() functions]]
Down:: [[💻 Coding/Python Basics/49 - File IO\|49 - File IO]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-28 - 23:26==

## readlines() method
The readline() method reads a single line from the file. If we want to read multiple lines, we can use a loop.
```python
f = open('myfile.txt', 'r')
while True:
	line = f.readline()
	if not line:
		break
	print(line)
```

The readlines() method reads all the lines of the file and returns them as a list of strings.

## writelines() method
The writelines() method in Python writes a sequence of strings to a file. The sequence can be any iterable object, such as a list or a tuple.

Here's an example of how to use the writelines() method:

```python
f = open('myfile.txt', 'w')
lines = ['line 1\n', 'line 2\n', 'line 3\n']
f.writelines(lines)
f.close()
```

This will write the strings in the lines list to the file myfile.txt. The \n characters are used to add newline characters to the end of each string.

Keep in mind that the writelines() method does not add newline characters between the strings in the sequence. If you want to add newlines between the strings, you can use a loop to write each string separately:
```python
f = open('myfile.txt', 'w')
lines = ['line 1', 'line 2', 'line 3']
for line in lines:
	f.write(line + '\n')
f.close()
```

It is also a good practice to close the file after you are done with it.