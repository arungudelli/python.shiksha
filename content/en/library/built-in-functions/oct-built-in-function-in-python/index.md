---
title: "python oct() functions syntax,usage and examples"
description: "The 'oct()'function is a one of the built-in functions in python"
date: "2022-08-05T11:50:05+09:00"
draft: false
link: "oct() Built-in functions"
author: "harika"
---

## `oct()` function in python

1. The `oct()` function is a one of the built-in functions in python.
2. The `oct()` is used for	`Converts a number into an octal`.
3. Python `oct()` function is used to get an octal value of an integer number. 
4. This method takes an argument and returns an integer converted into an octal string.
5. It throws an error TypeError if argument type is other than an integer.

## `oct()` function syntax

```python
oct(integer)
```
## `oct()` function parameters

integer : An integer value which is to be converted into an octal string.
it returns octal value.

### `oct()` function  Examples:

let's go through some of examples to understand `oct()` function in python

### Example 1:

```python
# Binary to Octal
print(oct(0b1))
 
# Hexa to octal
print(oct(0XB))

# Python3 program demonstrating TypeError
print("The Octal representation of 29.5 is " + oct(78.92))
```
output:

```python
0o1
0o13
print("The Octal representation of 29.5 is " + oct(78.92))
TypeError: 'float' object cannot be interpreted as an integer
```

### Example 2:
```
x = oct(100)

print(x)
```
output:

```python
0o144
```

## Summary
In this tutorial we learnt about Python `oct()` function with simple examples

