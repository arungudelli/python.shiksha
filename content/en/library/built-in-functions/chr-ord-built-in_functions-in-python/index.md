---
title: "python chr() and ord() functions syntax,usage and examples"
description: "The 'chr()' and 'ord()' functions both are Built in functions in python"
date: "2022-06-28T011:00:05+09:00"
draft: false
link: "chr() ord() built-in functions in python"
author: "harika"
---

## `chr()` and `ord()` functions in python

`chr()` and `ord()` functions both are Built in functions in python.

These functions can used to convert `unicode values to character` and `character to unicode`  

## ASCII values:

Every character is represented by ASCII value.
This ASCII values is a string encoding format.
ASCII values can represent only 256 values.

Example:
A-65
a-97

## python UNICODE

Every form of character, including letters, symbols, and emojis, has a numerical value according to the Unicode standard.

The standard made it considerably simpler for computers to comprehend symbols, which was especially helpful given how many new symbols are being introduced to the internet. 

UNICODE is superset of ASCII values.

It is represent multiple number of values compare to ASCII.
A-65
a-97
all the values are same in UNICODE and ASCII values.



## python `ord()` convert char to unicode:

The Python `ord()` function converts `a character into an integer` that represents the Unicode code of the character. 


### `ord()` Examples:

let's go through couple of examples to understand `ord()` function in python

### Example 1: To find UNICODE Value

```python
ch =input("Enter character to find corresponding UNICODE value:")
print(ord(ch))
```
output:

```python
Enter character to find corresponding UNICODE value:D
68
```

### Example 2: if input is single character

```python
ch =input("Enter character to find corresponding UNICODE value:")
print(ord(ch))
```
output:

```python
Enter character to find corresponding UNICODE value:H
72
```

### Example 3: If input is two characters 

```python
ch =input("Enter character to find corresponding UNICODE value:")
print(ord(ch))
```
output:

```python
Enter character to find corresponding UNICODE value:AB
Traceback (most recent call last):
  File "c:/Users/Vamshi/date.py", line 2, in <module>
    print(ord(ch))
TypeError: ord() expected a character, but string of length 2 found
```
why because the character length is `one`.
We can pass in any `single string character` and the function will return an integer

## `chr()` function convert unicode to char

The `chr()` function converts a Unicode code `character into the corresponding string`.

## `chr()` Function Syntax

```python
chr(num)
```
## `chr()` Function parameter
num: an Unicode code integer

## `chr()` Function return type
Return: Returns str

### `chr()` function Examples:

let's go through couple of examples to understand `chr()` function in python

### Example:

```python
unicode =int(input("Enter  UNICODE value to find corresponding value:"))
print(chr(unicode))
```
output:

```python
Enter  UNICODE value to find corresponding value:100
d

Enter  UNICODE value to find corresponding value:68
D
```

## Summary
In this tutorial we learnt about Python `chr()` and `ord()` functions with simple examples.





