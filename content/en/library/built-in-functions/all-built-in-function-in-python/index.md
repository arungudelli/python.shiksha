---
title: "Python all() function syntax, usage & example"
description: "The 'all()' function is one of the built-in functions in python"
date: "2022-07-20T03:58:00+00:00"
draft: false
link: "all() built-in functions"
author: "harika"
---

## `all()` function in python

1. The `all()` function is one of the built-in functions in python.
2. The `all()` is used for `Returns True if all items in an iterable object 
   are true` otherwise it returns False.

## `all()` function Syntax

```python
all(iterable)
```

## `all()` function parameter

The `all()` function can take only one parameter.
iterable -An iterable object (list, tuple, dictionary)

## `all()` Return type

If the iterable object is empty, the all() function also returns True.

### python `all()` Examples

Here we have some examples to understand `all()` function in detail.

### python `all` Example 1: `all()` for False 

```python
# welcome to Pythonshiksha
list = [0, 1, 1]
x = all(list)
print(x)
```
output:

```python
False
```
output is False because 0 is have in list.

### Example2: `all()` for True

```python
# welcome to Pythonshiksha
list = [1, 1, 1]
x = all(list)
print(x)
```
output:

```python
True
```
output is True because,list have all 1.

## Summary

In this tutorial we learnt about Python `all()` function with simple examples.





