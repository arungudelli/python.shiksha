---
title: "python issubclass() function syntax,usage and examples"
description: "The 'issubclass()' function is a one of the built-in functions in python"
date: "2022-08-22T01:30:05+09:00"
draft: false
link: "issubclass()Built-in functions"
author: "harika"
---

## `issubclass()` function in python

1. The `issubclass()` function is a one of the built-in functions in python.
2. The `issubclass()` is used for `Returns True if a specified class is a subclass of a specified object`.

## `issubclass()` function Syntax

```python
issubclass(object, subclass)
```
## `issubclass()` function parameters
object is Required. An object.
subclass is A class object, or a tuple of class  object.

### `issubclass()` function Example:

let's go through couple of examples to understand `issubclass()` function in python

## Example 1:

```python
class student:
  age = 15

class myObj(student):
  name = "John"
  age = student

x = issubclass(myObj, student)
print(x)
```
output:

```python
True
```
## Example 2:

```python
class Square:
  def __init__(SquareType):
    print('Square is a ', SquareType)

class circle(Square):
  def __init__(self):
    Square.__init__('circle')
    
print(issubclass(circle, Square))
print(issubclass(circle, list))
print(issubclass(circle, (list, Square)))
print(issubclass(Square, (list, Square)))
```
output:

```python
True
False
True
True
```
## Summary
In this tutorial we learnt about Python `issubclass()` function with simple examples
