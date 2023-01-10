---
title: "python staticmethod() function syntax,usage and examples"
description: "The 'staticmethod()' function is a one of the built-in functions in python"
date: "2022-08-23T03:30:05+09:00"
draft: false
link: "staticmethod()Built-in functions"
author: "harika"
---

## `staticmethod()` function in python:
The `staticmethod()` function is a one of the built-in functions in python.
`staticmethod()` is used for `Converts a method into a static method`.

Static methods, like class methods, are methods that are connected to a class rather than its object.

They do not necessitate the construction of a class instance.
As a result, they are not affected by the state of the object. 

The difference between a static method and a class method is:

Static method knows nothing about the class and just deals with the parameters.
    
Class method works with the class since its parameter is always the class itsel

## `staticmethodd()` Syntax:

```python
@staticmethod
def func(args, ...)
```
## `staticmethod()` parameters

function - function that needs to be converted to a static method

The staticmethod() method takes a single parameter

The staticmethod() returns a static method for a function passed as the parameter.

Note: staticmethod() is considered a un-Pythonic way of creating a static function. Hence, in newer versions of Python, you can use the @staticmethod decorator.

### Example:
```python
class homework:
    def mulNumbers(x, y):
    return x * y

homework.mulNumbers = staticmethod(homework.mulNumbers)
print('The mul is:', homework.mulNumbers(5, 10)
```
output:
```python
The mul is:50
```
## Summary
In this tutorial we learnt about Python `staticmethod()` function with simple examples