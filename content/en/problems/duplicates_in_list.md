---
title: "Duplicates in a List in Python"
description: "Different methods to check if a list contains duplicates or not in Python."
lead: ""
date: 2022-01-25T14:40:56+01:00
lastmod: 2022-01-25T14:40:56+01:00
draft: false
images: []
type: docs
---

# Check if a List contains duplicate using Python

In this tutorial we will learn, how to check if a list contains duplicates using `Python`.

## Problem Statement

Given an integer array of numbers, return `true` if any number appears **at least twice** in the array, and return `false` if every element is distinct.

**Assumptions:**

- 1 <= nums.length <= 105
- -109 <= nums[i] <= 109

Example:

```
# Example 1

Input: nums = [1,2,3,1]
Output: true

# Example 2

Input: nums = [1,2,3,4]
Output: false
```

## Approach 1: Set () constructor

The most optimal way to remove duplicates from a list is by converting the list to a set by using the `set()` constructor.

Sets are a collection of only unique elements and do not allow duplicates inside of the collection.

### Algorithm

- First type case the input list into set by using the `set()` constructor and store the set in a new variable.
- Then check if the length of the list and the length of the set are equal or not.
- If equal, then _no duplicates_ in the list else the list contains duplicates.

```
def findDuplicate(lst):
    result = set(lst)

    if len(result) == len(lst):
        return 'false'
    else:
        return 'true'

# Driver Code

arr = [1, 2, 3, 1]
output = findDuplicate(arr)
print(output)
```

Output
`true`

We got the expected result as the input list contained duplicates i.e. Two '1's and thus we have completed discussing about the simplest method for achieving the desired result.

## Approach 2: Brute Force

For solving any complex problem in problem solving, the beginner's approach is always the brute force method.

And this problem is no different and now then discuss the brute force approach for checking the duplicates.

### Algorithm

- We will first iterate through the whole list and then use a nested loop to iterate within the range (0, index).
- And then we check if the ith index element is equal to the jth index element and if they are equal then return true else false.

```
def findDuplicates(lst):
    n = len(lst)
    for i in range(n):
        for j in range(0,i):
            if lst[i] == lst[j]:
                return 'true'
    return 'false'

# Driver Code

arr = [1,2,5,6,7]
print (findDuplicates(arr))
```

Output
`false`

### Complexity

**Time Complexity**:
Since we are using a nested loop structure in order to achieve the result, therefore the time complexity for the code execution is `O(N2)`.

**Space Complexity**:
Since we aren't storing any data in our program memory, therefore the space complexity of the code is `O(1)`.

## Approach 3: Sorting and Checking

In the previous method, we learnt about the brute force approach which had a hefty time complexity of `O(N2)`.

In order to reduce the time complexity and optimize the code, we can first sort the list and then check for duplicates using brute force technique.

### Algorithm

- First sort the list using the `sort()` method and then applying the brute force technique to achieve the desired output.
- In this way we will reduce the number of iterations because after sorting the duplicate values will be arranged consecutively.

```
def findDuplicates(lst):
    lst.sort();
    for i in range(len(lst)):
        for j in range(0,i):
            if lst[i] == lst[j]:
                return 'true'
    return 'false'

# Driver Code

arr = [1,2,5,6,1]
print (findDuplicates(arr))
```

Output
`true`

### Complexity

**Time Complexity**:
We have discussed earlier that this approach takes less time than the brute force technique.
And thus, the time complexity of the code is `O(NlogN)`, where N is the length of the list.

**Space Complexity**:
This code executes in `O(1)` space complexity.

## Approach 4: Using Count ()

We have until now discussed about the generic method, but we haven't delved deep into any list methods, so let's do it now.

In this approach we are going to look at a very common method of list i.e., the `count()` method.

```
def findDuplicates(lst):
    for num in lst:

	    # Counting the number of occurences of the list
        n = lst.count(num)
        if n > 1:
            return 'true'

    return 'false'

# Driver Code

arr = [1,4,5,7,8,3,2,1,5,6,0]
print(findDuplicates(arr))
```

Output
`true`

As we can see that, we have got the desired output and thus we can conclude that using the list method gives us an edge over the other methods.

## Summary

We have now completed discussing all the method to **check for duplicate items in a list** using `Python`.

Taking an overview of what we have discussed, we started off with discussing the simplest for solving this problem i.e., by using `set()` and then we looked upon two methods using the Beginner / Brute force approach, one with sorted list and the other with the unsorted list.

At the end we concluded the article by learning about using one of the list methods to solve the problem i.e., the `count()` method.
