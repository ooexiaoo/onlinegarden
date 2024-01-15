---
{"dg-publish":true,"permalink":"/coding/python-basics/44-how-import-works/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-01-14T14:16:26.254+05:30","updated":"2024-01-15T18:50:04.099+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Coding/Python Basics/45 - if name == main in Python\|45 - if name == main in Python]]
Down:: [[Coding/Python Basics/43 - Virtual Environment\|43 - Virtual Environment]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2024-01-14 - 14:16==

Importing in Python is the process of loading code from a Python module into the current script. This allows you to use the functions and variables defined in the module in your current script, as well as any additional modules that the imported module may depend on.

To import a module in Python, you use the import statement followed by the name of the module. For example, to import the math module, which contains a variety of mathematical functions, you would use the following statement:
```python
import math
```

Once a module is imported, you can use any of the functions and variables defined in the module by using the dot notation. For example, to use the sqrt function from the math module, you would write:
```python
import math
result = math.sqrt(9)print(result) # Output: 3.0
```

## From keyword
You can also import specific functions or variables from a module using the from keyword. For example, to import only the sqrt function from the math module, you would write:
```python
from math import sqrt
result = sqrt(9)print(result) # Output: 3.0
```

You can also import multiple functions or variables at once by separating them with a comma:
```python
from math import sqrt, pi
result = sqrt(9)print(result) # Output: 3.0

print(pi)  # Output: 3.141592653589793
```

## Importing everything
It's also possible to import all functions and variables from a module using the * wildcard. However, this is generally not recommended as it can lead to confusion and make it harder to understand where specific functions and variables are coming from.

```python
from math import *

result = sqrt(9)
print(result)  # Output: 3.0


print(pi)  # Output: 3.141592653589793
```

Python also allows you to rename imported modules using the as keyword. This can be useful if you want to use a shorter or more descriptive name for a module, or if you want to avoid naming conflicts with other modules or variables in your code.

## The "as" keyword
```python
import math as m

result = m.sqrt(9)
print(result)  # Output: 3.0

print(m.pi)  # Output: 3.141592653589793
```

## The dir function
Finally, Python has a built-in function called dir that you can use to view the names of all the functions and variables defined in a module. This can be helpful for exploring and understanding the contents of a new module.
```python
import math

print(dir(math))
```

This will output a list of all the names defined in the math module, including functions like sqrt and pi, as well as other variables and constants.

In summary, the import statement in Python allows you to access the functions and variables defined in a module from within your current script. You can import the entire module, specific functions or variables, or use the * wildcard to import everything. You can also use the as keyword to rename a module, and the dir function to view the contents of a module.

## Main Example
```python
# from math import sqrt, pi
# from math import pi, sqrt as s
# import math as math_builtin_python

# result = math_builtin_python.sqrt(9) * math_builtin_python.pi
# print(result)  # Output: 3.0

# from harry import welcome, harry
import harry as hr
import math

print(dir(math))
print(math.nan, type(math.nan))
hr.welcome()
print(hr.harry)
```