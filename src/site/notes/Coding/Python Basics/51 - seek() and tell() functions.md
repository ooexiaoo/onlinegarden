---
{"dg-publish":true,"permalink":"/coding/python-basics/51-seek-and-tell-functions/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-29T16:52:44.119+05:30","updated":"2024-01-29T16:55:50.949+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Coding/Python Basics/50 - read, readlines and other methods\|50 - read, readlines and other methods]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-29 - 16:52==

In Python, the seek() and tell() functions are used to work with file objects and their positions within a file. These functions are part of the built-in io module, which provides a consistent interface for reading and writing to various file-like objects, such as files, pipes, and in-memory buffers.

## seek() function
The seek() function allows you to move the current position within a file to a specific point. The position is specified in bytes, and you can move either forward or backward from the current position. For example:

```python
with open('file.txt', 'r') as f:
	# Move to the 10th byte in the file
	f.seek(10)

	# Read the next 5 bytes
	data = f.read(5)
```

## tell() function
The tell() function returns the current position within the file, in bytes. This can be useful for keeping track of your location within the file or for seeking to a specific position relative to the current position. For example:

```python
with open('file.txt', 'r') as f:
	# Read the first 10 bytes
	data = f.read(10)


  # Save the current position
  current_position = f.tell()

  # Seek to the saved position
  f.seek(current_position)
```

## truncate() function
When you open a file in Python using the open function, you can specify the mode in which you want to open the file. If you specify the mode as 'w' or 'a', the file is opened in write mode and you can write to the file. However, if you want to truncate the file to a specific size, you can use the truncate function.

Here is an example of how to use the truncate function:
```python
with open('sample.txt', 'w') as f:
	f.write('Hello World!')
	f.truncate(5)

with open('sample.txt', 'r') as f:
print(f.read())
```