---
title: "Python bytearray() function syntax,usage and examples"
description: "The 'bytearray()'function is one of the built-in function in Python"
date: "2022-07-26T11:00:40+09:00"
draft: false
link: "bytearray() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `bytearray()`function in Python

1. The `bytearray()` function is one of the built-in function in Python.
2. The `bytearray()` is used for `Returns an array of bytes`.

# `bytearray()`function syntax

```Python
bytearray([source[, encoding[, errors]]])
```
# `bytearray()` function Parameters

bytearray() takes three optional parameters:

    source (Optional) - source to initialize the array of bytes.
    encoding (Optional) - if the source is a string, the encoding of the string.
    errors (Optional) - if the source is a string, the action to take when the encoding conversion fails (Read more: String encoding)

The source parameter can be used to initialize the bytearray in the following ways:

String
	Converts the string to bytes using str.encode() Must also provide encoding and optionally errors
Integer
	Creates an array of provided size, all initialized to null
Object
	A read-only buffer of the object will be used to initialize the byte array
Iterable
	Creates an array of size equal to the iterable count and initialized to the iterable elements Must be iterable of integers between 0 <= x < 256
No source (arguments)
	Creates an array of size 0.
bytearray() Return Value

The bytearray() method returns an array of bytes of the given size and initialization values.

## `bytearray()` return type

`bytearray()` method returns a bytearray object (i.e. array of bytes) which is mutable (can be modified) sequence of integers in the range 0 <= x < 256.


### `bytearray()` function Examples:

let's go through couple of examples to understand `bytaarray()` function in Python


### Example 1: `bytaarray()` for string

```Python
# welcome to Pythonshiksha
str = "Pythonshiksha"
array = bytearray(str, 'utf-16')
print(array)
```
output:
```Python
bytearray(b'\xff\xfep\x00y\x00t\x00h\x00o\x00n\x00s\x00h\x00i\x00k\x00s\x00h\x00a\x00')
```

## Example 2: `bytaarray()` To find length of array

```Python
# welcome to Pythonshiksha
my_list = [29,31,11,4,24]
  
array = bytearray(my_list)
  
print(array)
print("Count of bytes:", len(array))
```
output:

```Python
Count of bytes: 5
```
Note:
If you want the immutable version, use the `bytes()` method.

## Summary

In this tutorial we learnt about Python `bytearray()` function with simple examples.
