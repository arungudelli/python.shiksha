---
title: "python complex()function syntax,usage and examples "
description: "The 'complex()' function is a one of the built-in functions in python"
date: "2022-08-17T11:39:05+09:00"
draft: false
link: "python complex() function"
author: "harika"
---

## `complex()` function in python

1. The `complex()` function is a one of the built-in functions in python.
2. The `complex()` is used for `Returns a complex number`.


## `complex()` function Syntax

```python
complex(real, imaginary)
```

## `complex()` function parameters

The `complex()` function can take two parameters.

1. 'real'  is Required-  A number representing the real part of the complex number. Default 0. 
The real number can also be a String, like this '3+5j', when this is the case, the second parameter should be omitted.

2. 'imaginary' is Optional- A number representing the imaginary part of the complex number. Default 0.

## ## `complex()` function return value

The `complex()` function returns a complex number by specifying a real number and an imaginary number.


### Example 1:

```python
x=complex(4,9) 
print(x) 

```
output:

```python
(4+9j)
```

### Example 2: 

```python
x = complex('8+5j')
print(x)
```
output:

```python
8+5j
```
## Summary
In this tutorial we learnt about Python `complex()` function with simple examples.





