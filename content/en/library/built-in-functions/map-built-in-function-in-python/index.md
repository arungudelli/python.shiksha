---
title: "Python map() function syntax,usage and examples"
description: "The 'map()' function is a one of the built-in functions in Python"
date: "2022-08-18T03:05:05+09:00"
draft: false
link: "map() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `map()` function in Python

1. The `map()` function is a one of the built-in functions in Python.
2. The `map()` is used for	`Returns the specified iterator with the specified function applied to each item`.

For each item in an iterable, the map() function calls a predefined function.
The object is passed as a parameter to the function. 

# `map()` function Syntax 

```Python
map(fun, iter)
```
## `map()` function parameters

`map()` function can take two parameters
1. fun : It is a function to which map passes each element of given iterable.
2. iter : It is a iterable which is to be mapped.

NOTE : You can pass one or more iterable to the `map()` function.

## `map()` function Returns

Returns a list of the results after applying the given function  
to each item of a given iterable (list, tuple etc.) 

NOTE : The returned value from map() (map object) then can be passed to functions like list() (to create a list), set() (to create a set) .

### `map()` function Examples:

let's go through couple of examples to understand `map()` function in Python

### `map()` function Example 1:

```Python
def mylist(a, b):
  return a + b
x = map(mylist, ('apple', 'banana', 'cherry'), ('orange', 'lemon', 'pineapple'))
print(x)

#convert the map into a list, for readability:
print(list(x))
```
output:

```Python
['appleorange', 'bananalemon', 'cherrypineapple']
```
### `map()` function Example 2:

```Python
num1 = [8, 9, 6]
num2 = [9, 6, 8]

result = map(lambda n1, n2: n1+n2, num1, num2)

print(list(result))
```
output:

```Python
[17,15,14]
```
## Summary
In this tutorial we learnt about Python `map()` function with simple examples


