---
title: "Python aiter() function syntax, usage & example"
description: "The 'aiter()' function is a one of the built-in functions in python"
date: "2022-07-07T03:40:05+09:00"
draft: false
link: "aiter() Built-in functions"
author: "harika"
---

## `aiter()` function in python

1. The `aiter()` function is a one of the built-in functions in python.
2. The `aiter()` is used to Returns the absolute value of a number.
3. The `aiter()` is a new function that came in Python 3.10 version

## `aiter()` function Syntax 

The syntax `aiter()` function is 

```python
aiter(iter)
```
## `aiter()` function parameters

The `aiter()` function can take only one parameter
iter	asynchronous iterable.

##  `aiter()` function return type

It returns an asynchronous iterator for an asynchronous iterable

## Python `aiter()` Examples

```python
async def aaa(iterable):
    async for element in aiter(iterable):
        if element:
            element = [1,2,3]
            element>2
            return True
            element> 0
        return False
print(aaa)
```

output:

```python
<function aaa at 0x001777C0>
```

## Summary

In this tutorial we learnt about Python `aiter()` function with simple examples.



