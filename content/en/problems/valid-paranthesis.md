---
title: "Valid Paranthesis problem in Python"
description: "To check wether a given string is valid according to the paranthesis order"
lead: ""
date: 2022-01-25T14:40:56+01:00
lastmod: 2022-01-25T14:40:56+01:00
draft: false
images: []
type: docs
toc: true
---

## Problem Statment 

Given a string input containing just the characters '(', ')', '{', '}', '[' and ']'. Check wether the given string is valid according to the order of the paranthesis.

Examples of Valid Paranthesis are 

```
//Example 1

Input: "((}}"
Output: True

// Example 2

Input: "(({})[])"
Output: True

// Example 3

Input: "(({}{}[])[])"
Output: True

// Example 4

Input: "(([]}))"
Output: False

// Example 5

Input: "(({}])"
Output: False

```

Conditions to be Evaluvated

  1.If every opening paranthesis has a closing paranthesis

  2. if every pair of opening and closing paranthesis are in correct order

## Approach 1 : Using an empty list

Explanation: A new empty list is created and while traversing through the string each opening paranthesis is stored in the list.

Whenever a closing paranthesis is encountered the last element inserted in the list is checked for its opening pranthesis. If the condition is true it is poped from the list and the loop goes on otherwise it returns `False` since it violates condition 2.

After completing all the iterations, if the list is empty then it return `True` else `False`. Reason here is that if the list is not empty means condition 1 is not satisfied.

List here acts as a stack

```python
def isValid(x):
    y=[]
    for i in x:
        if i=='(' or i=='{' or i=='[':
            y.append(i)
        else:
            if i==')':
                if y[-1]=='(':    
                    y.pop()
                else:
                    # violated condition 2
                    return False
            if i=='}':
                if y[-1]=='{':
                    y.pop()
                else:
                    # violated condition 2
                    return False
            if i==']':
                if y[-1]=='[':
                    y.pop()
                else:
                    # violated condition 2
                    return False
    else:
        if len(y)==0:
            return True
        else:
            # violated condition 1
            return False

``` 

**Time Complexity**
This has a time complexity of `O(n)` where n is the number of characters in the string.

## Approach 2: Using a dictionary.

Explanation: 
Similar to above approach but instead of list we are using stack and intead of checking each of the values seperatly we are assinging keys of dictionary as the open paranthesis and the values as the closing paranthesis and checking them in a single go. 

If the string given as input is valid function will return `True` else `False`.

This optimises the code and runs faster when compared to the above approach.

```python
def isValid(test_str):  
    par_dict = {'(':')','{':'}','[':']'}
    stack = []
    for char in test_str:
        if char in par_dict.keys(): 
            stack.append(char)
        elif char in par_dict.values():
            if stack == []:
                # violated condition 1
                return False
            open_brac = stack.pop()
            if char != par_dict[open_brac]:
                # Violated condition 2
                return False
    if stack == [] :
        return True
    else: 
        # violated condition 1               
        return False
```
**Time Complexity**

This has a time complexity of `O(n)` where n is the number of characters in the string.

## Summary

We have learned how to check wether a given string has valid paranthesis.

Even though the above two approaches uses similar ideas the second one runs faster and has a more optimised code.
