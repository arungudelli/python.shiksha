---
title: "python print() function syntax,usage and examples"
description: "The 'print()' function is one of the built-in function in python"
date: "2022-07-25T11:10:40+09:00"
draft: false
link: "print() Built-in functions"
author: "harika"
---

## `print()` function  in python

1. The `print()` function is one of the built-in function in python.
2. The `print()` is used for `Prints to the standard output device`.
3. The `print()` function prints the specified message to the screen,
the message can be a string, or any other object, the object will be converted into a string before written to the screen.

## `print()` function syntax

```python
print(object(s))
sep=separator, end=end, file=file, flush=flush
```

## `print()` function parameters

object(s)- Any object, 
and as many as you like. Will be converted to string before printed

sep='separator' - (Optional)
Specify how to separate the objects, if there is more than one. Default is ' '

end='end' (Optional) 
Specify what to print at the end. Default is '\n' (line feed)

file (Optional) 
An object with a write method. Default is sys.stdout

flush (Optional) 
A Boolean, specifying if the output is flushed (True) or buffered (False). Default is False

### `print()` function Examples:

let's go through some of examples to understand `print()` function in python

### `print()` Example 1:
```python
print("welcome to pythonshiksha")
print("easy to learn")
```
output:

```python
welcome to pythonshiksha
easy to learn
```
### `print()` Example 2:

```python
print("Hello", "BEST TUTORIAL FOR PYTHON", sep="---")
```
Output:

```python
Hello---BEST TUTORIAL FOR PYTHON
```
whatever we can write in print function can display on the screen that is any spelling mistakes in any words or any type of data type also can display on the screen.

### `print()` Example 3:

```python
print("mnbjj,787,9.0,hdhk,hyd")
```
output:

```python
mnbjj,787,9.0,hdhk,hyd
```
## Summary
In this tutorial we learnt about Python `print()` function with simple examples