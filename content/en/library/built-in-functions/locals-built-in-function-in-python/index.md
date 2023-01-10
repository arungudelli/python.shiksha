---
title: "Python locals() function syntax, usage & example"
description: "The `locals()` function is a one of the built-in functions in Python"
date: "2022-07-07T03:40:05+09:00"
draft: false
link: "locals() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `locals()` function in Python

1. The `locals()` function is a one of the built-in functions in Python.

##  `locals()` function Syntax

```Python
locals()
```

## `locals()` function Parameter Values

No parameters required this function.

## `locals()` Return Value

The `locals()` method returns the dictionary of the current local symbol table.

## `locals()` function Examples:

let's go through couple of examples to understand `list()` function in Python

### Example 1: To know current working file name 

```Python
x = locals()
print(x["__file__"])
```
output:

```Python
c:/Users/Python/locals.py
```
### Example 2:

```Python
class local:
    str = "Pythonshiksha"
    # locals inside a class
    print('\nlocals() value inside class\n', locals())
```

output:

```Python
locals() value inside class
 {'__module__': '__main__', '__qualname__': 'local', 'str': 'Pythonshiksha'}
```

## Summary
In this tutorial we learnt about Python `locals()` function with simple examples





