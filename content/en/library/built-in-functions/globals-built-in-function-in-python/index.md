---
title: "Python globals() function syntax,usage and examples "
description: "The 'globals()' function is a one of the built-in functions in Python"
date: "2022-08-18T02:00:05+09:00"
draft: false
link: "Python `globals()` Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `globals()` function in Python

1. The `globals()` function is a one of the built-in functions in Python.
2. The `globals()` is used for `Returns the current global symbol table as a dictionary`.

## Symbol table: A symbol table is a type of data structure that houses all of the program's necessary data.
These include class names, methods, and variable names.

Python's `globals()` method provides access to the global symbol table, which contains all data pertaining to the program's global scope. 


## `globals()` function syntax

```Python
Syntax: globals()
```
## `globals()` function Parameters 

No parameters required for `globals()` function.

### `globals()` function Examples:

let's go through couple of examples to understand `globals()` function in Python


###  `globals()` Example 1: 

```Python
name = 'arjun'
print('Before modification:', name)
  
# Calling global()
globals()['name'] = 'arjun reddy'
print('After modification:', name)
```
output:

```Python
Before modification: arjun
After modification: arjun reddy
```

###  `globals()` Example 2: 

```Python
num = 20
globals()['num'] = 55
print('The number is:', num)
```
output:

```Python
The number is:
```
we can also modify the number with this global function in Python

## Summary
In this tutorial we learnt about Python `globals()` function with simple examples.