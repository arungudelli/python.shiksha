---
title: "Python anext() function syntax, usage & example"
description: "The 'anext()' function is a one of the built-in functions in python"
date: "2022-07-07T03:40:05+09:00"
draft: false
link: "anext() Built-in functions"
author: "harika"
---

## `anext()` function in python

1. The `anext()` function is a one of the built-in functions in python.
2. `anext()` returns the next element, which could be obtained from an asynchronous source such as an asynchronous database.But it doesn't have to be

## `anext()` function Syntax 

```python
anext(async_iterator[, default])
```
## `anext()` function parameters

The `anext()` function takes two arguments 
1. asynchronous iterator
2. default value, which is to be returned on certain condition


## `anext()` function return type

When awaited, return the next item from the given asynchronous iterator, or default if given and the iterator is exhausted.

## Python `anext()` Examples

let's go through couple of examples to understand `anext()` function in python

### Example 1: `anext()` function