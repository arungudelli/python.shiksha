---
title: "python dir() function syntax,usage and examples"
description: "The 'dir()' function is a one of the built-in functions in python"
date: "2022-08-18T11:10:05+09:00"
draft: false
link: "python dir() function"
author: "harika"
---

## `dir()` function in python

1. The `dir()` function is a one of the built-in functions in python.
2. The `dir()` is used for `Returns a list of the specified object's properties and methods`.

## `dir()` function Syntax

```python
dir(object) 
```
## `dir()` function parameter

The `dir()` can take only one parameter.
object is The object you want to see the valid attributes of properties.


The list of names in the current local scope is returned by the `dir()` function in Python.
If a method called __dir__()  exists on the object being invoked, it will be called and required to produce a list of attributes. 

### `dir()` function Examples:

let's go through couple of examples to understand `dir()` function in python

### Example 1:

```python
class employee:
  name = "aaaa"
  age = 48
  country = "India"
  gender = "male"
  
print(dir(employee))
```
output:

```python
['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'age', 'country', 'gender', 'name']
```

### Example 2:

```python
my_number = [31]

# returns valid attributes of the number list 
print(dir(my_number))
```
output:

```python
['__add__', '__class__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
```
The output will remain the same even if you modify the my number in this case because it can show any number of valid attributes. 

## Summary
In this tutorial we learnt about Python `dir()` function with simple examples.
