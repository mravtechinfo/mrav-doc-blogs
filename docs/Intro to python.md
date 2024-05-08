# My Python Journey

## Introduction

In this blog post, I'll share my journey of learning Python and some interesting concepts I've come across.

```python
# Printing
print('hello')

# Input
name = input('Enter your name here: ')
print('Hello ' + name)

# Blank Lines
print('Hello world')
print()

print('Did you see that blank line?')

print('Blank line \nin the middle of a string is like this.')

# Mathematics
print('Adding numbers')
x = 56 + 546
print(x)

print('Dividing numbers')
y = 567 / 0
print(y)
```

```
# Virtual Environments
# Installation
# pip install virtualenv
# Creating a virtual environment
# virtualenv <folder_name>
# Activating a virtual environment
# source <folder_name>/bin/activate
# Installing packages
# pip install <package_name>
```
## Decorators
```
import functools
from colorama import init, Fore
init()

def color(color):
    def wrapper(func):
        @functools.wraps(func)
        def runner(*args, **kwargs):
            print(color + 'changing to blue')
            func(*args, **kwargs)
        return runner
    return wrapper

@color(color=Fore.BLUE)
def greeter():
    print('Hello, world!!')
    print('Just saying hi again')

greeter()
```