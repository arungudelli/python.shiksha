---
title: " python float() function syntax, usage and examples in python"
description: "The  'filter()' function is a one of the built-in functions in python."
date: "2022-07-20T03:30:05+09:00"
draft: false
link: "float() Built-in functions"
author: "harika"
---

## `float()` function in python

1. The `filter()` function is a one of the built-in functions in python.
2. The `float()` function converts the specified value into a floating point number.

## `float()` function Syntax

```python
float(value)
```
##  `float()` function parameters
 
 `float()` function can take only one parameter
value- A number or a string that can be converted into a floating point number

### `filter()` function Examples:

let's go through some of examples to understand `filter()` function in python

### `float()` Example 1: python `float()` function with infinity

```python
print(float("infinity"))
```
output:

```python
inf
```

### Example 2: python `float()` with integer

```python
print(float("29"))
```
output:

```python
29.0
```

### Example 3: python `float()` with string

```python
print(float("python"))
```
output:

```python
print(float("python"))
ValueError: could not convert string to float: 'python'
```
it gives error because 'python' is a string not an integer or decimal.

## Summary
In this tutorial we learnt about Python `float()` function with simple examples.
