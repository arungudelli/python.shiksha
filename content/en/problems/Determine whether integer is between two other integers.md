---
title: "Determine whether the integer is between the two other integers in Python"
description: "Different methods of checking the integer is between the two other integers "
lead: ""
date: 2023-02-25T14:40:56+01:00
lastmod: 2023-02-25T14:40:56+01:00
draft: false
images: []
type: docs
toc: true
---
In this article, we will briefly discuss about the different python methods that we can use to check if an integer is present between the two integers **along with some tips that can make our coding efficient.**

### Determine Whether Integer is between two other integer

Let's start exploring the various python tips and approach to check whether the integer is between two other integers.

## Using `if` statement inside `for` loop: (Brute force)

This is the first approach which comes in ypur mind first.

Here,we are checking each element of the for loop inside the conditional statement.If the `if` statement becomes true then we are printing the result else `else` part will get executed.

```python
Integer1=10
Integer2=20
for i in range(Integer1,Integer2):
        if i==15:
           print('present')
```

output:

```
present

[program finished]
```

**Complexity**

Time complexity is `O(n`)

space complexity is `O(1)`

As this approach is Brute force approach it won't be good fit for large numbers

It would take time to finish the execution even though we get the result since loop will not end.

##### **For example**,

Let's assign a big value to a variable integer2.

```python
Integer1=10
Integer2=2059587698678565566453434243243232523
for i in range(Integer1,Integer2):
        if i==15:
           print('present')
```

```
present
```

It prints present but not prints "program finished"since the execution not yet finished even though we get the value but it is still checking every element

## **using membership `in` operator.**:

The in operator is one of the fastest and most generic method adopted by python programmers as they know the power of the in operator and its value in python.

The `in` operator evaluates the presence of an Integer  inside a range of two integers  and return a boolean value accordingly.

```python
Integer1=10
Integer2=2059587698678565566453434243243232523
if 15 in range(Integer1,Integer2):
         print('yes present')
else:
         print('No!not present)
```

output:

```
yes present
[program finished]
```

**Complexity**

Time complexity is `O(1`)

space complexity is `O(1)`

## using logical `and` operator.

We can also use logical and operator .It will check both condition 1 and condition 2 .If both of them are true then only we see the output at the console others not since logical and operator evaluates both of the condition and both should be true if any one of them is fail it stops the execution at that point itself.

```python
Integer1=10
Integer2=2059587698678565566453434243243232523
if 15>=Integer1 and 15<=Integer2:
          print('yes present)
```

```
present
[program finished]
```

**Complexity**

Time complexity is `O(1`)

space complexity is `O(1)`

It is  an optimized approach.

## **using Interval comparison method.**

This method is simple mathematical Interval range method .

For example, `(0<= a<=b).`

```python
Integer1=10
Integer2=2059587698678565566453434243243232523
if Integer1<= 15 <=Integer2:
        print('present')
```

```
present
[program finished]
```

**Complexity**

Time complexity is `O(1`)

space complexity is `O(1)`

From the output, it is clearly visible that our mighty `in ` and `and` operator stands out above all other methods and hence `in` adds one more time-saving usability into itself.

So as a python programmer, we should always be aware that `in`  and `and` can solve many of our searching tasks.

## Summary

In this article, we discussed in detail about all the various methods with the help of which we can easily checkwhether the integer is between two other integers.
