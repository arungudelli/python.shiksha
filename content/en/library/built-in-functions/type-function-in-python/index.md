---
title: "Python type() function syntax, usage & example"
description: "The `type()` function is one of the Built in functions in python"
date: "2022-06-29T11:25:05+09:00"
draft: false
link: "type() built-in function"
author: "harika"
---

## `type()` in python:

1. The `type()` function is one of the Built in functions in python"
2. Depending on the inputs supplied, the `type()` function either returns the type of the object or returns a new type object. 

## `type()` syntax:
```python

1. type(name, bases, dict)
```
## `type()` parameters
name - a class name; 
bases - Optional. Specifies the base classes
dict - Optional. Specifies the namespace with the definition for the class (dictionry).

2. type()

single parameter can return a specified type of data.
type of the object, if only one object parameter is passed

### Example:
```python
a = ('TIGER', 'PYTHON', 'BANANA','HYDERABAD')
b = "good morning"
c = 55.8
d = 100

x = type(a)
y = type(b)
z = type(c) 
p = type(d)

print(x,y,z,p)
```
Output:
```python
<class 'tuple'> <class 'str'> <class 'float'> <class 'int'>
```
In Python, the `type()` function is used to quickly determine what kind of data the user can include in the programme. 

## Summary
In this tutorial we learnt about Python `type()` function with simple examples