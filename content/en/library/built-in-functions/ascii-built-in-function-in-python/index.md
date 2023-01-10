---
title: "python ascii() function syntax, usage and example"
description: "The 'ascii()' function is one of the built-in functions in python"
date: "2022-07-21T10:00:00+00:00"
draft: false
link: "ascii() built-in functions"
author: "harika"
---

## `ascii()` function in python

1. The `ascii()` function is one of the built-in functions in python.
2. The `ascii()` is used for `Returns a readable version of an object`. Replaces none-ascii characters with escape character

The `ascii()` function will replace any non-ascii characters with escape characters like this

`å `will be replaced with `\xe5.`

1. `ASCII` stands for `American Standard Code for Information Interchange`.

2. The `ascii()` method in Python returns a string containing a printable representation of an object for non-alphabets or invisible characters such as tab, carriage return, form feed, etc. 

3. It escapes the non-ASCII characters in the string using \x, \u or \U escapes.


## `ascii()` function Syntax

```python
ascii(object)
```

## `ascii()` function parameters


object is An object, like String, List, Tuple, Dictionary etc.

## Python `ascii()` function Examples 

Input : ascii("¥")
Output : '\xa5'

Input : ascii("µ")
Output : '\xb5'

Input : ascii("Ë")
Output : '\xcb'

We see that in these examples, all the non-ASCII characters have been escaped, i.e, their encoded code gets displayed by using the ascii() method.

### Example 1: `ascii()` function for `å`

```python
# welcome to Pythonshiksha
x = ascii("my tutorial name is pythonshikshå")
print(x)
```
output:

```python
'my tutorial name is pythonshiksh\xe5'
```
### Difference between ascii() vs print()

### Example 2:

```python
# welcome to Pythonshiksha
str = '''E
For 
egg'''
print("Display with ascii function : ",ascii(str))
print("Display with print function : ",str)
```
output:

```python
Display with ascii function :  'E\nFor \negg'
Display with print function :  E
For
egg
```
from this output we can clear that difference between ascii value and print.

## Summary 
In this tutorial we learnt about Python `ascii()` function with simple examples.




