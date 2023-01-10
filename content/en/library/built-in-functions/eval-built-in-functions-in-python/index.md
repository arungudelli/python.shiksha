---
title: "python eval() function syntax,usage and examples"
description: "The 'eval()' function is one of the built-in functions in python"
date: "2022-07-05T05:00:05+09:00"
draft: false
link: "eval() Built-in functions"
author: "harika"
---

## `eval()` function in python

1. The `eval()` function is one of the built-in functions in python.
2. The `eval()` function evaluates the specified expression, if the expression is a legal Python statement, it will be executed.


## `eval()` function syntax

```python
eval(expression, globals, locals) 
```
## `eval()` function parameters

The `eval()` can tke three parameters.
expression- A String, that will be evaluated as Python code
globals- Optional. A dictionary containing global parameters
locals- Optional. A dictionary containing local parameters


###  `eval()` function example:

let's go through couple of examples to understand `eval()` function in python

### Example 1: if source code is single expression then we can use `eval()` built-in function in python

```python
x = compile('print("welcome")', 'test', 'eval')
eval(x) 
```
output:
```python
welcome
```
### Example 2:

```python
x = 'print(75)'
eval(x)
```
output:

```python
75
```
## Summary
In this tutorial we learnt about Python `eval()` function with simple examples.


