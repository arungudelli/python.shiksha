---
title: "python memoryview() function syntax,usage and examples "
description: "The 'memoryview()' function is a one of the built-in functions in python"
date: "2022-08-23T01:30:05+09:00"
draft: false
link: "memoryview() Built-in functions"
author: "harika"
---

## `memoryview() `function in python

1. The `memoryview()` function is a one of the built-in functions in python.
2. `memoryview()` is used for `Returns a memory view object`.

3. The `memoryview()` function returns a memory view object from a specified object.

## what is `memoryview` in python 

A `memory view` is a safe way to expose the buffer protocol in Python.
It allows you to access the internal buffers of an object by creating a memory view object.

## what is buffer protocol in python
We can utilize the buffer protocol to grant another object access to the huge data without copying it.

This reduces memory usage and enhances programme execution speed. 

This protocol is only accessible to us at the C-API level and not using our normal codebase.

So, in order to expose the same protocol to the normal Python codebase, memory views are present.


## `memoryview() `function Syntax

```python
memoryview(obj)
```
## `memoryview() `function parameter

`memoryview() `function can take only one parameter.
obj is A Bytes object or a Bytearray object.

### `memoryview() `function Examples:

let's go through some of examples to understand `memoryview()` function in python

### Example 1:

```python
x = memoryview(b"pythonshiksha")

print(x)

#return the Unicode of the fifth character
print(x[5])

#return the Unicode of the third character
print(x[3])
```
output:

```python
<memory at 0x1468b5fbfa00>
110
104
```
### Example 2:

```python
barr = bytearray('Python','utf-8')
mv = memoryview(barr)
print(type(mv))
print(mv[0])
print(mv[1])
print(mv[2])
print(mv[3])
print('Converted to list: ', list(mv)) # convert to list
```

output:

```python
<class 'memoryview'>
80
121
116
104
Converted to list:  [80, 121, 116, 104, 111, 110]
```

## Summary
In this tutorial we learnt about Python `memoryview()` function with simple examples

