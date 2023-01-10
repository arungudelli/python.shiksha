---
title: "how to use functions in python"
description: " Introduction of functions and how to use functions in python"
date: "2022-06-23T11:35:05+09:00"
draft: false
link: "how to use functions"
author: "harika"
---

## what is function:

A function is a group statements that exist within a program for the purpose of performing a specific task and it will be executed only when it is called.

Instead of writing a large program as one long sequence of statements,it
can be written as several small functions.

These small functions can be executed in the desired order to perform the overall task.

This approach is called `divide and conquer` because a large task is divided into several smaller tasks that are easily performed.

A program that has been written with each task in its own function is called a `modularized program`



## How to define a function:
 
**Define a Function:**
To create a Function we write its definition using `def` keyword.
A Function name to uniquely identify it.

Here is the general for format of a function definition in python

```
>>> def function_name():
	statements
```
The first line is known as the function header,it marks the beginning of the function definition.

The function name begins with the keyword of `def`,allowed by the name of the function,then  set of parentheses `()`, and then by a colon `:`.

The statements of the function must be `indented`.

## Example:
```
>>> def greet():
	print("hello, welcome")
	print("how are you")

	
>>> greet()
```
output:

```
hello, welcome
how are you
```
In this program `greet` is a `function name`

## Calling a Function:
**How to call a function**:
A Function definition specifies what  function does,but it does not cause the function to exicute.

To execute a function, we must call it as shown below:

## Example:
```
>>> def greet():    #define a function
	print("hello, welcome")
	print("how are you")

	
>>> greet()         #calling a function
```
## output:
```
hello, welcome
how are you
```
In this program `greet` is a `function name`
In this program `greet()` is used to call that function, after calling the function can executes its statements 

## Example2:

```
>>> def hi():
	print("good morning")
	print("have a good day")

>>> hi()
```
## output:
```
good morning
have a good day
```

In this `hi():` is a `function name` we define hi(): function with `def`
keyword.

and `hi()` is used to call that hi function after calling this function it executes its statements like this.

check example and try with your own function names and statements also.

## conclusion:

Functions are a crucial topic in Python for breaking down large tasks into smaller chunks that can be executed properly. 