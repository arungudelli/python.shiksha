---
title: "Python len() function syntax,usage and examples"
description: "The 'len()' function is one of the built-in function in python"
date: "2022-06-26T07:30:00+09:00"
draft: false
link: "len() built-in function"
author: "harika"
---

## `len()` Function in python

1. The `len()` function is one of the built-in function in python
2. Python has an Built-in function `len()` function for calculating the number of elements inside a list.

3. This function takes in the string whose length is to be calculated as the argument and this function returns an integer value as the output i.e., the "length" of the string.

## how the `len()` can work:

1.create a list with any data type
2.find out the `length` of the list with `len()`
 After this if the list `length`  is `0`then the list is empty.
Otherwise list have something in it.

## `len()` function Syntax

```python
len(object)
```
## `len()` function Parameter Values

object is Required - An object. 
Must be a sequence or a collection

### `len()` function Examples:

let's go through couple of examples to understand `len()` function in python

### `len()`example 1:
```python
list1=[]
if len(list1)==0:
    print("list is empty")
```
output:

```python
list is empty
```
### `len()`example 2:
```python
x = len("pythonshiksha")

print(x)
```
output
```python
13
```
we successfully checked the list is empty with `len()` but this is not recommended by PEP8.

## Summary
In this tutorial we learnt about Python `len()` function with simple examples