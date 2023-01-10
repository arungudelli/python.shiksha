---
title: "Python hex() function syntax,usage and examples"
description: "The 'hex()' function is one of the built-in functions in python"
date: "2022-07-19T11:30:00+09:00"
draft: false
link: "python `hex()` built-in functions"
author: "harika"
---

## `hex()`function in python

1. The `hex()` function is one of the built-in functions in python.
2. The`hex()` is used for	`Converts a number into a hexadecimal value`.
The returned string always starts with the prefix 0x.

## `hex()`function Syntax

```python
hex(number)
```
## `hex()`function parameter

number is `An Integer`

## `hex()` function Examples:

let's go through couple of examples to understand `hex()` function in python

### `hex()`function Example 1:

```python
number = 2022
print(number, 'in hex =', hex(number))

number = 0
print(number, 'in hex =', hex(number))

number = -29
print(number, 'in hex =', hex(number))

returnType = type(hex(number))
print('Return type from hex() is', returnType)
```
output:

```python
2022 in hex = 0x7e6
0 in hex = 0x0
-29 in hex = -0x1d
Return type from hex() is <class 'str'>
```
If you need to find a hexadecimal representation of a float, you need to use `float.hex()` method.

# `hex()`function Example 2:

```python
number = 2.5
print(number, 'in hex =', float.hex(number))
```
output:

```python
2.5 in hex = 0x1.4000000000000p+1
```
2.5 hexadecimal value is 0x1.4000000000000p+1
-2.5 hexadecimal value is -0x1.4000000000000p+1 difference is only `-` value will be same 

## Summary
In this tutorial we learnt about Python `hex()` function with simple examples

