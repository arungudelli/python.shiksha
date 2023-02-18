---
title: "Remove Final Character From String"
description: "4 python methods to Remove Final Character From String"
lead: ""
date: 2023-02-25T14:40:56+01:00
lastmod: 2023-02-25T14:40:56+01:00
draft: false
images: []
type: docs
toc: true
---
In this article, we will briefly discuss about the different python approaches that we can use to remove final character from string.

#### Overview of Strings in Python

Strings are an array of Unicode characters occupying a storage of few bytes.

If you come from a different language, there are high chances of your interaction with the char keyword, but in python there is no such char keyword and thus we can say that a single letter inside quotation marks in python is a string with length 1.

Strings behave the same way as like arrays and thus can be accessed by using the [] operator.

A substring is a sequence of Unicode characters within a string.

Examples of Strings in python:

‘python’ , ‘coding’ , ‘py’ , ‘d’ , ‘xyz'  ,  "abcdefghij"

## Different Methods To Remove Final Character From String

Let's start exploring the various python tips and approach to remove the final character from string.

## **Using `for` loop(Brute force).**

This is the first approach which comes in your mind first.

Here,we are creating a `variable` which is empty and in that variable we are storing all the characters of string one by one except last character.

```python
empty_var=''
string='pythonShiksha'
for i in range(len(string)-1):
       empty_var+=string[i]
print('empty_var')
```

output:

```
pythonShiksh
```

**Complexity**

Time complexity is `O(n`)

space complexity is `O(n)`

## Using String Slicing:

string slicing in python is we are taking the specific part of the string.

Using [slicing](https://stackoverflow.com/questions/509211/understanding-slicing), one can specify the `start` and `stop` indexes to extract part of a string `s`. The format is `s[start:stop]`. However, `start = 0` by default. So, we only need to specify `stop`.

`Note`->`start`=0 always untill and unless we defined,` stop`=the value which you give `-` 1

For example,

```python
#printing first 5 characters of a string
#characters->p y t h o n s h i k  s h  a
#indices->   0 1 2 3 4 5 6 7 8 9 10 11 12
string='pythonShiksha'
print(string[0:6])
#printing all characters of a string
string='pythonShiksha'
print(string[0:])
Removing last character of a string
string='pythonShiksha'
print(string[0:len(string)-1])
print(string[:-1])


```

output:

```
python
pythonShiksha
pythonShiksh
pythonShiksh
```

Try the following code snippet to better understand how it works by casting the string as a list:

As string are immutable ,we cannot modify the strings that means there is no `pop` method in strings to remove the last character in that case we can type cast the string in to list

```python
str1 = "python"
list1 = list(str1)
print(list1)
print(list1[:-1])
print(list1.pop())
```

output:

```
['p','y','t','h','o','n']
['p','y','t','h','o']
['p','y','t','h','o']

```

## Summary

In this article, we discussed in detail about all the tips and methods with the help of which we can easily remove the final character of a string.

Instead of using `for` loop use `string slicing` method to remove the final character,that will be optimal
