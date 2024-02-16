---
{"dg-publish":true,"permalink":"/coding/python-basics/67-exercise-6-solution/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-02-16T20:18:26.299+05:30","updated":"2024-02-16T20:19:56.023+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[]]
Down:: [[Coding/Python Basics/66 - Instance vs Class variables\|66 - Instance vs Class variables]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-02-16 - 20:18==

Write a Library class with no_of_books and books as two instance variables. Write a program to create a library from this Library class and show how you can print all books, add a book and get the number of books using different methods. Show that your program doesn't persist the books after the program is stopped!

## Solution
```python
class Library:
  def __init__(self):
    self.noBooks = 0
    self.books = []
    
  def addBook(self, book):
    self.books.append(book)
    self.noBooks = len(self.books)

  def showInfo(self):
    print(f"The library has {self.noBooks} books. The books are")
    for book in self.books:
      print(book)


l1 = Library()
l1.addBook("Harry Potter1")
l1.addBook("Harry Potter2")
l1.addBook("Harry Potter3")
l1.showInfo()
```