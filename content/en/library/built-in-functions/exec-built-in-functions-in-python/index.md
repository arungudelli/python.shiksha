---
title: "Python exec() function syntax,usage and examples"
description: "The 'exec()' function is a one of the built-in functions in Python"
date: "2022-07-05T05:00:05+09:00"
draft: false
link: "exec() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `exec()` function in Python

1. The `exec()` function is a one of the built-in functions in Python.
2. The `exec()` function executes the specified Python code.
3. The `exec()` function accepts large blocks of code, unlike the `eval()` function which only accepts a single expression

### `exec()` function Syntax

```Python
exec(object, globals, locals)
```

### `exec()` Parameter Values
object-	A String, or a code object
globals- Optional. A dictionary containing global parameters
locals 	Optional. A dictionary containing local parameter

### `exec()` function Example:

let's go through couple of examples to understand `exec()` function in Python


### Example 1:

```Python
x = compile('print("welcome to")\nprint("Python shiksha")', 'test', 'exec')
exec(x) 
```
output:

```Python
welcome to
Python shiksha
```
### Example 2:

```Python
prog = 'print("The sum of 5 and 10 is", (5+10))'
exec(prog)
```
output:

```Python
The sum of 5 and 10 is 15
```

## Summary
In this tutorial we learnt about Python `exec()` function with simple examples.


