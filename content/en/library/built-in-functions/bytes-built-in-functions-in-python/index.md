---
title: "Python bytes() function syntax,usage and examples"
description: "The 'bytes()' function is a Built in function in python "
date: "2022-06-26T07:30:00+00:00"
draft: false
link: "python bytes() built-in function"
author: "harika"
---

## `bytes()` function in python

1. The `bytes()` is a Built in function in python.
2. Python's `bytes()` function is used to return a bytes object.

## `bytes()` function syntax

```python
bytes(x, encoding, error) 
```

## `bytes()` function parameters

`bytes()`can take three parameters
Parameter 	Description
1. x 	        is A source to use when creating the bytes object.

                If it is an integer, an empty bytes object of the specified size will be created.

                If it is a String, make sure you specify the encoding of the source.

2. encoding 	The encoding of the string
3. error 	    Specifies what to do if the encoding fails.

It's a static version of the `bytearray()` function.

It is capable of producing an empty bytes object of the specified size. 

### `bytes()` function Examples:

let's go through couple of examples to understand `bytes()` function in python

### Example 1: `bytes()` function for string

```python
# welcome to Pythonshiksha
string = "hello python world"  
array = bytes(string, 'utf-8')  
print(array)
```
output

```python
b'hello python world'
```
### Example 2: `bytes()` function for numbers

```python
x = bytes(1)
print(x)
y = bytes(2)
print(y)
z =bytes(3)
print(z)
```
output:
```python
b'\x00'
b'\x00\x00'
b'\x00\x00\x00'
```

## Summary
In this tutorial we learnt about Python `bytes()` function with simple examples.
