---
title: "python setattr() function syntax,usage and examples"
description: "The 'setattr()' function is a one of the built-in functions in python"
date: "2022-08-15T06:49:05+09:00"
draft: false
link: "setattr() Built-in functions"
author: "harika"
---

## `setattr()` function in python:
1. The `setattr()` function is a one of the built-in functions in python.
2. The `setattr()` is used for `Sets an attribute (property/method) of an object`.

when we want to add a new attribute to an object and set a value to it. 
It returns None to the caller function.

## `setattr()`Syntax:
```python
setattr(object, attribute, value)
```
## `setattr` parameters

object is Required-An object.
attribute is Required-The name of the attribute you want to set
value is Required-The value you want to give the specified attribute

### Example:
```python
class student:
    firstName = 'chandu'
    lastName = 'patel'

std = student()
print('First Name: ', std.firstName)
print('Last Name: ', std.lastName)

setattr(std,'firstName','nandini')
setattr(std,'lastName','reddy')

print('After setting attributes')

print('First Name: ', std.firstName)
print('Last Name: ', std.lastName)
```
output:
```python
First Name:  chandu
Last Name:  patel
After setting attributes
First Name:  nandini
Last Name:  reddy
```
here chandu patel is set to nandini reddy.


## Summary
In this tutorial we learnt about Python `setattr()` function with simple examples

