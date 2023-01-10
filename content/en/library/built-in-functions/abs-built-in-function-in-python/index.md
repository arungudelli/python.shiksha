---
title: "Python abs() function syntax, usage & example"
description: "The 'abs()' function is a one of the built-in functions in python"
date: "2022-07-07T03:40:05+09:00"
draft: false
link: "abs() Built-in functions"
author: "harika"
---

## `abs()` function in python

1. The `abs()` function is a one of the built-in functions in python.
2. The `abs()` is used to Returns the absolute value of a number.

## `abs()` function Syntax 

The syntax `abs()` function is 

```python
abs(number)
```
## `abs()` function parameters

The `abs()` function takes only one parameter

1. number

number can be an integer, a floating-point number or a complex number

If the argument is an integer or floating-point number, `abs()` returns the absolute value in integer or float.

In the case of a complex number, `abs()` returns only the magnitude part and that can also be a floating-point number.


## Python `abs()` Examples

let's go through couple of examples to understand `abs()` function in python

### Example 1: `abs()` function with float

If the number is float number with negative, it will returns positive number like this

```python
# welcome to Pythonshiksha
float = -36.75
print('Absolute value of float is:', abs(float))
```
output:

```python
Absolute value of float is: 36.75
```

### Example 2: `abs()` function with integers

If the number is integer  with negative it will returns positive number like this

```python
# welcome to Pythonshiksha
int = -29
print('Absolute value of integer is:', abs(int))
```
output:

```python
Absolute value of integer is:29
```
### Example 3: `abs()` function with complex numbers

If the number is complex number `abs()` returns only the magnitude part and that can also be a floating-point number.

```python
# welcome to Pythonshiksha
complex = (4 - 8j)
print('Absolute value or Magnitude of complex is:', abs(complex))
```

output:

```python
Absolute value or Magnitude of complex is: 8.94427190999916
```

## Summary

In this tutorial we learnt about Python `abs()` function with simple examples.


