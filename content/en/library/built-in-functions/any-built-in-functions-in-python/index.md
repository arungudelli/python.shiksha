---
title: "any() function syntax,usage and examples in Python"
description: "The 'any()' function is one of the built-in functions in python"
date: "2022-07-21T10:00:00+00:00"
draft: false
link: "any() built-in functions"
author: "harika"
---

## `any()` function in python

1. The `any()` function is one of the built-in functions in python.
2. Python any() function returns True if any of the elements of a given       iterable( List, Dictionary, Tuple, set, etc) are True else it returns False. 

## `any()` function Syntax

```python
any(iterable)
```

## `any()` function parameter

The `any()` function can take only one parameter.

Iterable: 
It is an iterable object such as a dictionary, tuple, list, set, etc.                 

## `any()` function Return type

Returns: 
Python any() function returns true if any of the items is True.

### python `any()`Examples:
let's go through some  examples to understand `any()` function in python

### Example 1: `any()` function with list

```python
# welcome to Pythonshiksha
# All elements of list are false
l = [ 0, 0, False]
print(any( l ))
 
# Some elements of list are
# true while others are false
l = [ 0, 0, 9, 12, False]
print(any( l ))
 
# Empty List
l = []
print(any( l ))
```

output:

```python
True
False
True
False
```

like this, In this list place we can use dictionaries,strings,tuples,sets for all these methods `any()` function can give output either true or false.


### Example 2: `any()` function with strings

```python
# welcome to Pythonshiksha
# Non-Empty String
s = "python!"
print(any(s))
 
# Non-Empty String
s = "111"
print(any(s))
 
# Empty string
s = ""
print(any(s))
```
output
```python
True
True
False
```
### `any()`Example 3: any() function to Check if any element in list satisfies a condition

```python
# welcome to Pythonshiksha
# initializing list
my_list = [33,21,29,8,39.80]
 
# printing list
print("The original list : " + str(my_list))
 
# Check if any element in list satisfies a condition
# Using any()
res1 = any(ele > 80 for ele in my_list)
res2 = any(ele < 10 for ele in my_list)
 
# Printing result
print("Does any element satisfy specified condition ? : " + str(res1))
print("Does any element satisfy specified condition ? : " + str(res2))
```
output:

```python
The original list : [33, 21, 29, 8, 39.8]
Does any element satisfy specified condition ? : False
Does any element satisfy specified condition ? : True
```
## Note for any() function

1. If the particular element is in that list or dictionary `any()` will give  TRUE.
2. If there is no element in that `any()` will give FALSE.

## Summary
In this tutorial we learnt about Python `any()` function with simple examples.




