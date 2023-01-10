---
title: "Python bytes() function syntax,usage and examples"
description: "The 'bytes()' function is a Built in function in Python "
date: "2022-06-26T07:30:00+00:00"
draft: false
link: "Python bytes() built-in function"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `bytes()` function in Python

1. The `bytes()` is a Built in function in Python.
2. Python's `bytes()` function is used to return a bytes object.

## `bytes()` function syntax

```Python
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

let's go through couple of examples to understand `bytes()` function in Python

### Example 1: `bytes()` function for string

```Python
# welcome to Pythonshiksha
string = "hello Python world"  
array = bytes(string, 'utf-8')  
print(array)
```
output

```Python
b'hello Python world'
```
### Example 2: `bytes()` function for numbers

```Python
x = bytes(1)
print(x)
y = bytes(2)
print(y)
z =bytes(3)
print(z)
```
output:
```Python
b'\x00'
b'\x00\x00'
b'\x00\x00\x00'
```

## Summary
In this tutorial we learnt about Python `bytes()` function with simple examples.
