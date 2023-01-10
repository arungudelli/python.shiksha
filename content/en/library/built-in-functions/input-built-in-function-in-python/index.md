---
title: " Python input() function syntax,usage and examples"
description: "The 'input()'function is one of the built-in function in Python"
date: "2022-07-19T11:00:00+09:00"
draft: false
link: "input() built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `input()` function in Python

1. The `input()` function is one of the built-in function in Python.
2. The `input()` is used for `Allowing user input`.
3. The `input(`) function takes input from the user and returns it.

## `input()` function syntax

```Python
input([prompt])
```
## `input()` function Parameters

The `input(`) function takes a single optional argument:

prompt (Optional) - a string that is written to standard output (usually screen) without trailing newline

## `input()` function Return Value

The `input() `function reads a line from the input (usually from the user), 

converts the line into a string by removing the trailing newline, and returns it.

If EOF is read, it raises an EOFError exception.

## `input()` function Examples:

let's go through couple of examples to understand `input()` function in Python

### `input()` Example 1:

```Python
name = input("Enter best Python tutorial name: ")
print(name)
```
output:

```Python
Enter best Python tutorial name: Python shiksha
Python shiksha
```

### `input()`Example 2: Taking two values from user and adding both values

```Python
num1 = int(input("Please Enter First Number: "))
num2 = int(input("Please Enter Second Number: "))
addition = num1 + num2
  
# printing
print("The sum of the two given numbers is {} ".format(addition))
```

output:

```Python
Please Enter First Number: 29
Please Enter Second Number: 31
The sum of the two given numbers is 60
```

like this user can use this `input()` built-in function to add numbers, append the values or any other data collection information this function can useful.

## Summary
In this tutorial we learnt about Python `input()` function with simple examples