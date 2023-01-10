---
title: "Python compile() function syntax,usage and examples"
description: "The 'compile()' is one of the built-in functions in Python"
date: "2022-07-05 T004:30:05+09:00"
draft: false
link: "compile() function in Python "
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `compile()` function in Python

1. The `compile()` is one of the built-in functions in Python.
2. The `compile()` function returns the specified source as a code object,
ready to be executed.

## `compile()` function Syntax

```Python
compile(source, filename, mode, flag, dont_inherit, optimize)
```
## `compile()` function Parameter

1. source: Required. The source to compile, can be a String, a Bytes object, or an AST object

2. filename: Required. The name of the file that the source comes from. If the source does not come from a file, you can write whatever you like

3. mode: Required. Legal values:
   eval: if the source is a single expression
   exec: if the source is a block of statements
   single: if the source is a single interactive statement

4. flags: Optional. How to compile the source. Default 0

5. dont-inherit: Optional. How to compile the source. Default False

6. optimize: Optional,Defines the optimization level of the compiler.
 Default -1

### `compile()` Examples:

let's go through couple of examples to understand `compile()` function in Python

### Example 1: if source code is block of statements then we can use `exec()` built-in function in Python

```Python
x = compile('print("welcome to")\nprint("Pythonshiksha")', 'test', 'exec')
exec(x) 
```
output:

```Python
welcome to
Pythonshiksha
```

### Example 2:  if source code is single expression then we can use `eval()` built-in function in Python

```Python
x = compile('print("welcome")', 'test', 'eval')
eval(x) 
```
output:

```Python
welcome
```

## Summary
In this tutorial we learnt about Python `compile()` function with simple examples.





