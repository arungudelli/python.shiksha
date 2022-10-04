---
title: "Check if two strings are anagrams in Python"
description: "Different ways to check if two strings are anagrams or not in Python"
lead: ""
date: 2022-01-25T14:40:56+01:00
lastmod: 2022-01-25T14:40:56+01:00
draft: false
images: []
type: docs
weight: 1
---

In this Tutorial we will write a `Python` program to check if two string are anagrams are not. 

An Anagram is a word or phrase formed by rearranging the letters of a different word or phrase.

## Problem Statement 

Given two strings `source` and `target`, write a `Python` function to check whether the given strings are anagrams of each other or not. 

If both are anagrams return `true` else `false`.

Examples of Anagrams are 

```
//Example 1

Input: source = "anagram", target = "nagaram"
Output: true

// Example 2

Input: source = "below", target = "elbow"
Output: true

// Example 3

Input: source = "study", target = "dusty"
Output: true

// Example 4

Input: source = "night", target = "thing"
Output: true

// Example 5

Input: source = "act", target = "cat"
Output: true

```

## Approach 1: Using Sorting

The simple way to check if strings are anagrams or not is too sort the both strings and compare them.

If they are equal then both are anagrams otherwise they are not.

We can use Python `sorted()` function to sort the strings.

`sorted()` is a built in function in `Python`, which returns the sorted string without modifying the existing string. 

```python

def CheckIfStringsAreAnagram(source: str, target: str) -> bool:

    ## Basic use case check if both strings length
    if(len(source)!=len(target)):
        return False
    return sorted(s)==sorted(t)

```

### Complexity

**Time Complexity:**

As we are using `sorted()` function, the worst case it takes `O(nlogn)`. 

So the Time complexity is `O(nlogn)`. 

Where `n` is the length of the string.

**Space Complexity:**

The space complexity is `O(n)`.

## Approach 2: Using Character Frequency Counter 

We can check if both strings are anagrams or not without sorting the strings.

As both strings contains only alphabets, we can count the occurrences of each character in two strings and then compare the count.

### Algorithm 

1. Check if both strings length equal or not.
2. Create two counter arrays for both strings, as they contain only alphabets we can create arrays with size `26`.
3. Then count the occurrences of each letter and store them in corresponding arrays.
4. Finally compare both arrays count. If both arrays counts are equal then strings are anagram return `true` else return `false`.

```python

    def CheckIfStringsAreAnagram(source: str, target: str) -> bool:
        
        if len(source) != len(target):
            return False
        
        numberOfAlphabets = 26
        sourceCharacterCounter = [0]*numberOfAlphabets
        targetCharacterCounter = [0]*numberOfAlphabets
        
        for character in source:
            sourceCharacterCounter[ord(character)-ord('a')] += 1
        for character in target:
            targetCharacterCounter[ord(character)-ord('a')] += 1
        for count in range(numberOfAlphabets):
            if sourceCharacterCounter[count] != targetCharacterCounter[count]:
                return False
        return True

```

`ord()` function returns the integer representation of unicode character. 

`ord('a')` is equal to `97`. 
`ord('z')` is equal to `122`.

We created two arrays with size `26` and initialized with all `0`'s.

```
[0,0,0.....,0] // 26 size
```
Let's say our source string is `cat`. 

```python
for character in source:
 sourceCharacterCounter[ord(character)-ord('a')] += 1

# [a,b,c,,,,,,,t,,,,,z]  
# [1,0,1,,,,,,,1,,,,,0] 
```

`ord('c')-ord('a')` represents index of character `c`. 

`sourceCharacterCounter[ord('c')-ord('a')]` is nothing but number of occurrences of character `c`.

To understand further print both `sourceAlphabetCounter` and `targetAlphabetCounter` arrays is using `Python`'s `print` function.

```python

#CheckIfStringsAreAnagram("anagram", "nagaram")
print(sourceAlphabetCounter)
print(targetAlphabetCounter)

"""
[3 0 0 0 0 0 1 0 0 0 0 0 1 1 0 0 0 1 0 0 0 0 0 0 0 0]
[3 0 0 0 0 0 1 0 0 0 0 0 1 1 0 0 0 1 0 0 0 0 0 0 0 0]
"""
```

If both array counts are same then both strings are anagrams. 

Let's improve the solution further.

Do we really need two counter arrays? **No**

Instead we can create only one counter array, then increase the count of each character in one string i.e, `source` and decrease the count of character in other string i.e.,`target`.

And if all values in the counter array are zero, then **both strings are anagrams**.

```python

    def CheckIfStringsAreAnagram(source: str, target: str) -> bool:
        
        if len(source) != len(target):
            return False
        
        numberOfAlphabets = 26
        characterCounter = [0]*numberOfAlphabets
        
        for index in range(len(source)):
            characterCounter[ord(source[index])-ord('a')] += 1
            characterCounter[ord(target[index])-ord('a')] -= 1

        for count in characterCounter:
            if count != 0:
                return False
        return True

```

We will slightly change the implementation further.

Instead of loop through all characters in both strings, we can increase the character count of source string in one loop, and in other loop decrease the destination character count.

If the count becomes less than `0` we can say that both **strings are not anagram** as destination string have few extra characters. 

```python

    def CheckIfStringsAreAnagram(source: str, target: str) -> bool:
        
        if len(source) != len(target):
            return False
        
        numberOfAlphabets = 26
        characterCounter = [0]*numberOfAlphabets
        
        for index in range(len(source)):
            characterCounter[ord(source[index])-ord('a')] += 1

        for index in range(len(source)):
            characterCounter[ord(target[index])-ord('a')] -= 1
            if(characterCounter[ord(target[index])-ord('a')]<0):
                return False
        
        return True

```

### Complexity

**Time Complexity is `O(n)`**

Where `n` is the length of the string.

**Space Complexity is `O(n)`**

## Approach 3: Using Hash Table

If strings contains unicode characters (not only alphabets), we cannot use fixed size integer array. 

Instead of that we should Hash table for the counters.  

In `Python` dictionary implements a hash table.

So we will create two `dictionary` variables to store the character count.

```go
func CheckIfStringsAreAnagram(source string, target string) bool {
    
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

## Approach 4: Using `Counter()` function in `collections`.

The most simple way to solve the problem is to use `Python`'s `Counter()` function.

`Counter()` function counts the occurrences characters and stores as dictionary keys and their count as dictionary value.

`Counter()` function is part of `collections`.

```python
print(Counter("anagram"))

## Outpur
## Counter({'a': 3, 'n': 1, 'g': 1, 'r': 1, 'm': 1})
```

So we can pass both strings to `Counter()` function to check whether they are anagrams or not. 

```python

    def CheckIfStringsAreAnagram(source: str, target: str) -> bool:
       
        if len(source) != len(target):
            return False
        
        from collections import Counter
        
        return Counter(source)==Counter(target)
```

### Complexity

**Time Complexity is `O(n)`**

Where `n` is the length of the string.

**Space Complexity is `O(n)`**


## Summary

We learnt different ways to check if two strings are anagrams or not in `Python` language.

In your daily projects you can use built in functions like `sorted()` or `counter()` to check if strings are anagrams or not. 

Otherwise use character counting approach.

1. Use frequency counter approach as it's simple and easy to understand.
2. Use Hash table approach if the strings contains unicode characters. 
