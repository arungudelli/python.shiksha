---
title: "python globals() function syntax,usage and examples "
description: "The 'globals()' function is a one of the built-in functions in python"
date: "2022-08-18T02:00:05+09:00"
draft: false
link: "python `globals()` Built-in functions"
author: "harika"
---

## `globals()` function in python

1. The `globals()` function is a one of the built-in functions in python.
2. The `globals()` is used for `Returns the current global symbol table as a dictionary`.

## Symbol table: A symbol table is a type of data structure that houses all of the program's necessary data.
These include class names, methods, and variable names.

Python's `globals()` method provides access to the global symbol table, which contains all data pertaining to the program's global scope. 


## `globals()` function syntax

```python
Syntax: globals()
```
## `globals()` function Parameters 

No parameters required for `globals()` function.

### `globals()` function Examples:

let's go through couple of examples to understand `globals()` function in python


###  `globals()` Example 1: 

```python
name = 'arjun'
print('Before modification:', name)
  
# Calling global()
globals()['name'] = 'arjun reddy'
print('After modification:', name)
```
output:

```python
Before modification: arjun
After modification: arjun reddy
```

###  `globals()` Example 2: 

```python
num = 20
globals()['num'] = 55
print('The number is:', num)
```
output:

```python
The number is:
```
we can also modify the number with this global function in python

## Summary
In this tutorial we learnt about Python `globals()` function with simple examples.