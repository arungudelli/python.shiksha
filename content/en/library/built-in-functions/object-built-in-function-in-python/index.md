---
title: "python object() function syntax,usage and examples"
description: "The 'object()'function is a one of the built-in functions in python"
date: "2022-08-05T11:50:05+09:00"
draft: false
link: "object() Built-in functions"
author: "harika"
---

## `object()` function in python

1. The `object()` function is a one of the built-in functions in python.
2. The `object()` is used for	`Returns a new object`. returns an empty object.
3. In python, each variable to which we assign a value/container is treated as an object. Object in itself is a class.

## `object()` function Syntax

```python
object()
```
## `object()` function function parameter

no parameters for this object function.

### `object()` function Examples:

let's go through some of examples to understand `object()` function in python

### Example 1:

```python
obj = object()
 
# printing its type
print("The type of object class object is : ")
print(type(obj))
 
# printing its attributes
print("The attributes of its class are : ")
print(dir(obj))
```
output:

```python
The type of object class object is :
<class 'object'>
The attributes of its class are :
['__class__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__']
```

###  Example 2:

```python
x = object()

print(dir(x))
```
output:

```python
['__class__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__']
```

## Summary
In this tutorial we learnt about Python `object()` function with simple examples


