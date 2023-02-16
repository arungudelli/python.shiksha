---
title: "Check if strings are anagrams in Python without sorting"
description: "Different ways to determine whether the integer is between two other integers"
lead: ""
date: 2023-02-25T14:40:56+01:00
lastmod: 2023-02-25T14:40:56+01:00
draft: false
images: []
type: docs
weight: 2
---
There are four ways to determine whether the integer is between two other integers.

1. Using Membership Operator With Range function
2. Using If Statement Inside the For Loop
3. Using Logical (and) Operator
4. Using Interval Comparision Method

## Approach 1: Using Character Counting

We can count the occurrences of both strings and compare them to check if they are anagrams not not.

```python

    def CheckIfStringsAreAnagramWithoutSorting(source: str, target: str) -> bool:

        if len(source) != len(target):
            return False

        sourceCounter = [0]*26
        targetCounter = [0]*26

        for character in source:
            sourceCounter[ord(character)-ord('a')] += 1
        for character in target:
            targetCounter[ord(character)-ord('a')] += 1
        for count in range(26):
            if sourceCounter[count] != targetCounter[count]:
                return False
        return True

```

We can use only single counter array instead of two.

```python

    def CheckIfStringsAreAnagramWithoutSorting(source: str, target: str) -> bool:

        if len(source) != len(target):
            return False

        characterCounter = [0]*26

        for index in range(len(source)):
            characterCounter[ord(source[index])-ord('a')] += 1
            characterCounter[ord(target[index])-ord('a')] -= 1

        for count in characterCounter:
            if count != 0:
                return False
        return True

```

To understand the logic go through the [Check if two strings are anagrams in Python](/problems/string-anagram-python) article.

### Complexity

**Time Complexity is `O(n)`**

Where `n` is the length of the string.

**Space Complexity is `O(n)`**

## Approach 2: Using dictionary Hash Table

If strings are unicode characters (not only alphabets), we should use `Python` dictionary to count the characters

```go
func CheckIfStringsAreAnagramWithoutSorting(source string, target string) bool {

    if len(source) != len(target) {
        return false
    }

    sourceDictionary, targetDictionary = {}, {}

    for character in source:
        sourceDictionary[character] = sourceDictionary.get(character, 0) + 1
    for character in target:
        targetDictionary[character] = targetDictionary.get(character, 0) + 1
    return sourceDictionary == targetDictionary


}
```

## Approach 3:*[ Using]()* and operator.

Instead of `sorting()` we can use Python built in function `Counter()` which is part of `collections`.

```python

    def CheckIfStringsAreAnagramWithoutSorting(source: str, target: str) -> bool:

        if len(source) != len(target):
            return False

        from collections import Counter

        return Counter(source)==Counter(target)
```

## Summary

In this Python tutorial, we learnt different ways to **check if two strings are anagrams or not without using sorting.**

Prefer using character counting method or dictionary based method as we are not using any built in functions in Python.
