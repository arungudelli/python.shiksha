---
title: "python set() function syntax,usage and examples"
description: "The 'set()' function is a one of the built-in functions in python"
date: "2022-08-15T11:15:05+09:00"
draft: false
link: "set() Built-in functions"
author: "harika"
---

## `set() `function in python:
The `set()` function is a one of the built-in functions in python.
`set()` is used for	`Returns a new set object`.

python `set()` method is used to convert any of the iterable to sequence of iterable elements with distinct elements, commonly called Set. 

## `set()`syntax:
```python
set(iterable)
```
## `set()` parameters

iterable is Required- A sequence, collection or an iterator object

Returns : An empty set if no element is passed. Non-repeating element iterable modified as passed as argument. 
 
### Example:
```python
names =set(('aaa','bbb','ccc','ddd'))
print(names)
```
output:
```python
{'ddd', 'aaa', 'ccc', 'bbb'}
```
always set will be unordered list and this output will change their order in every time.

## Summary
In this tutorial we learnt about Python `set()` function with simple examples

