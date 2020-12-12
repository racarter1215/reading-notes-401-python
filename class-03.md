#  Read and Write Files in Python

## Syntax error: Occurs when the parser detects an incorrect statement.

#### Example:
>>> print( 0 / 0 ))
  File "<stdin>", line 1
    print( 0 / 0 ))
                  ^
SyntaxError: invalid syntax
  
#### The arrows mean that a syntax error occured

#### Once you fix the error, this occurs:
>>> print( 0 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero

#### Exception error: Occurs whenever syntactically correct Python code results in an error.

#### Raising Exceptions: Allows you to customize exceptions
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))

Traceback (most recent call last):
  File "<input>", line 4, in <module>
Exception: x should not exceed 5. The value of x was: 10
  
#### Asserts: If a program runs correctly, it runs. If not, throw an exception

import sys
assert ('linux' in sys.platform), "This code runs on Linux only."

Traceback (most recent call last):
  File "<input>", line 2, in <module>
AssertionError: This code runs on Linux only.
  
#### Try and Except examples:

def linux_interaction():
    assert ('linux' in sys.platform), "Function can only run on Linux systems."
    print('Doing something.')

try:
    linux_interaction()
except:
    pass
    

# Reading and Writing Files in Python (Guide)

## File: a contiguous set of bytes used to store data.

### Header: metadata about the contents of the file (file name, size, type, and so on)
### Data: contents of the file as written by the creator or editor
### End of file (EOF): special character that indicates the end of the file

### File Paths:
### Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)
### File Name: the actual name of the file
### Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

#### Example:
/
│
├── path/
|   │
│   ├── to/
│   │   └── cats.gif
│   │
│   └── dog_breeds.txt
|
└── animals.csv

/
│
├── path/
|   │
|   ├── to/  ← Your current working directory (cwd) is here
|   │   └── cats.gif  ← Accessing this file
|   │
|   └── dog_breeds.txt
|
└── animals.csv


