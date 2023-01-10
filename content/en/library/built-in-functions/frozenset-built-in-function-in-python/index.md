---
title: "python frozenset() function syntax,usage and examples"
description: "The 'frozenset()' function is a one of the built-in functions in python "
date: "2022-08-19T08:00:05+09:00"
draft: false
link: "frozenset() Built-in functions"
author: "harika"
---

## `frozenset()` function in python

1. The `frozenset()` function is a one of the built-in functions in python.
2. The `frozenset()` is used for `Returns a frozenset object`.

An immutable form of a Python set object is what a frozen set is.
A set's components can be changed at any moment, but the components of a frozen set don't change after they've been created. 


## `frozenset()` function syntax

```python
frozenset([iterable])
```
## `frozenset()` function parameters

The `frozenset()` function takes a single parameter:

    iterable (Optional) - the iterable which contains elements to initialize the frozenset with.
    Iterable can be set, dictionary, tuple, etc.

## `frozenset()` Return value 

The `frozenset()` function returns an immutable frozenset initialized with elements from the given iterable.

If no parameters are passed, it returns an empty frozenset.

## `frozenset()` function Examples

let's go through couple of examples to understand `frozenset()` function in python

### Example 1:

```python
stu_list = ['aaa', 'bbb', 'ccc']
x = frozenset(stu_list)
print(x)
```
output:

```python
frozenset({'ccc', 'aaa', 'bbb'})
```
this frozenset list is immutable, we can't change it now 

lets see an example to add another student name.

### Example 2:

```python
stu_list = ['aaa', 'bbb', 'ccc']
x = frozenset(stu_list)
x[1] = "ddd"
print(x)
```
output:

```python
Traceback (most recent call last):
  File "./prog.py", line 3, in <module>
TypeError: 'frozenset' object does not support item assignment
```
when we try to add or remove from list it always gives an error why because frozenset is immutable.

## Summary
In this tutorial we learnt about Python `frozenset()` function with simple examples.
