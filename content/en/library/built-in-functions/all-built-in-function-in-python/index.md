---
title: "Python all() function syntax, usage & example"
description: "The 'all()' function is one of the built-in functions in Python"
date: "2022-07-20T03:58:00+00:00"
draft: false
link: "all() built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `all()` function in Python

1. The `all()` function is one of the built-in functions in Python.
2. The `all()` is used for `Returns True if all items in an iterable object 
   are true` otherwise it returns False.

## `all()` function Syntax

```Python
all(iterable)
```

## `all()` function parameter

The `all()` function can take only one parameter.
iterable -An iterable object (list, tuple, dictionary)

## `all()` Return type

If the iterable object is empty, the all() function also returns True.

### Python `all()` Examples

Here we have some examples to understand `all()` function in detail.

### Python `all` Example 1: `all()` for False 

```Python
# welcome to Pythonshiksha
list = [0, 1, 1]
x = all(list)
print(x)
```
output:

```Python
False
```
output is False because 0 is have in list.

### Example2: `all()` for True

```Python
# welcome to Pythonshiksha
list = [1, 1, 1]
x = all(list)
print(x)
```
output:

```Python
True
```
output is True because,list have all 1.

## Summary

In this tutorial we learnt about Python `all()` function with simple examples.





