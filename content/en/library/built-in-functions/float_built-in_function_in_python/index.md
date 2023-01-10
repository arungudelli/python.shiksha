---
title: " Python float() function syntax, usage and examples in Python"
description: "The  'filter()' function is a one of the built-in functions in Python."
date: "2022-07-20T03:30:05+09:00"
draft: false
link: "float() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `float()` function in Python

1. The `filter()` function is a one of the built-in functions in Python.
2. The `float()` function converts the specified value into a floating point number.

## `float()` function Syntax

```Python
float(value)
```
##  `float()` function parameters
 
 `float()` function can take only one parameter
value- A number or a string that can be converted into a floating point number

### `filter()` function Examples:

let's go through some of examples to understand `filter()` function in Python

### `float()` Example 1: Python `float()` function with infinity

```Python
print(float("infinity"))
```
output:

```Python
inf
```

### Example 2: Python `float()` with integer

```Python
print(float("29"))
```
output:

```Python
29.0
```

### Example 3: Python `float()` with string

```Python
print(float("Python"))
```
output:

```Python
print(float("Python"))
ValueError: could not convert string to float: 'Python'
```
it gives error because 'Python' is a string not an integer or decimal.

## Summary
In this tutorial we learnt about Python `float()` function with simple examples.
