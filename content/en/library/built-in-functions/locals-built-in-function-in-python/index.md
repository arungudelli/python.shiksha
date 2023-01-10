---
title: "Python locals() function syntax, usage & example"
description: "The `locals()` function is a one of the built-in functions in python"
date: "2022-07-07T03:40:05+09:00"
draft: false
link: "locals() Built-in functions"
author: "harika"
---

## `locals()` function in python

1. The `locals()` function is a one of the built-in functions in python.

##  `locals()` function Syntax

```python
locals()
```

## `locals()` function Parameter Values

No parameters required this function.

## `locals()` Return Value

The `locals()` method returns the dictionary of the current local symbol table.

## `locals()` function Examples:

let's go through couple of examples to understand `list()` function in python

### Example 1: To know current working file name 

```python
x = locals()
print(x["__file__"])
```
output:

```python
c:/Users/python/locals.py
```
### Example 2:

```python
class local:
    str = "pythonshiksha"
    # locals inside a class
    print('\nlocals() value inside class\n', locals())
```

output:

```python
locals() value inside class
 {'__module__': '__main__', '__qualname__': 'local', 'str': 'pythonshiksha'}
```

## Summary
In this tutorial we learnt about Python `locals()` function with simple examples





