---
title: "Palindrome Number in Python"
description: "Different methods to check for Palindrome number using Python."
lead: ""
date: 2022-01-25T14:40:56+01:00
lastmod: 2022-01-25T14:40:56+01:00
draft: false
images: []
type: docs
---

# Check if a Number is Palindrome or not using Python

In this tutorial we will learn, how to check for a palindrome number using `Python`.

## Problem Statement

Given an integer x, return true if x is palindrome integer.

An integer is a palindrome when it reads the same backward as forward.

For example, 121 is a palindrome while 123 is not.

**Constraints:**
-231 <= x <= 231 - 1

Example:

```
# Example 1
Input: 121
Output: Palindrome

#Example 2
Input: 404
Output: Palindrome
```

## Approach 1: Simple Iteration

Starting off with the simplest approach for solving the palindrome number problem is by iteration and checking.

### Algorithm

- We want to check that if the reverse of the number is equal to that of the input number.
- The most basic way to reverse a number is by using a temporary variable.
- We can declare a temporary variable in which we can store the reverse of the number.
- Running a `while` loop with condition of the temporary variable being less than zero.
  - Using the modulus operator, to find the remainder
  - And then by adding the remainder to (reverse \* 10) and updating the reverse number
  - Then dividing the original number to shorten it for consecutive iterations.
- After that, we can compare both the numbers and draw a conclusion.

```
n = 121
temp = n
rev = 0

# Loop to divide the original temporary number for
# iterations

while temp > 0:
    r = temp % 10
    rev = (rev * 10) + r
    temp = temp // 10
if n == rev:
  print('Palindrome')
else:
  print("Not Palindrome")
```

Output
`Palindrome`

### Complexity

**Time Complexity**:
In the program we are using a while loop to simply recursively iterate through the number and therefore the time complexity of the code is `OlogN`, where N is the no. of iterations.

**Space Complexity**:
Since we are storing the reverse number as well as the temporary number until the last iteration therefore the space complexity of the above code would be`O(N)`.

## Approach 2: String Slicing

In the above approach we took the input as an integer and performed the operation for check.

But in this method, we will first typecast the number into a string and will then perform the check for palindrome by using the string slicing method.

### Algorithm

- We will convert the integer to a string first, then reverse the string using string slicing and then we compare the original and the reversed string.
- First typecast the integer into a string by using the `str ()` constructor.
- Using the string slicing method, then reverse the number.
- Compare both the reversed string and original string to draw a conclusion

```
n = 404
rev = int(str(n)[::-1])

if n == rev:
  print('Palindrome')
else:
  print("Not Palindrome")
```

Output

`Palindrome`

### Complexity

**Time Complexity**:
Since we are performing a slice operation inside of our function execution, therefore the time complexity of the function is `O(K)`, where K is the length of the whole string.

**Space Complexity**
We are storing only the reversed string inside of the memory and therefore the space complexity of the code is `O(1)`.`

## Approach 3: Recursive Function

We will create a method that can be called recursively and will implement the same logic as that of the `while` loop.

A recursive function is more optimal than while loop because of its time complexity.

### Algorithm

- Define a recursive function which takes the number and taking reverse variables as arguments.
- Checking for the number if is equal to 0 and calling the function recursive with the logic (number // 10).
- Check if the returned value matches the original number.

```
def recurNum(n, rev):
    if n== 0:
        return rev

    r = int(n% 10)
    rev = (rev * 10) + r

    return recurNum(int(n/ 10), rev)


m = 12321
rev = 0
rev = recurNum(m, rev)

if(rev == m):
	print("Palindrome")
else:
	print("Not Palindrome")
```

Output

`Pallindrome`

### Complexity

**Time Complexity**
Since we are replacing the while loop call with a recursive function call and therefore the time complexity of the code would be `O(N)`, where N is the no. of the iterations.

**Space Complexity**
Since we are storing the values in the function and therefore the Space Complexity of the code would be `O(N)` as well.

## Approach 4: Character Matching

In the previous methods we have been using numbers as integers, but we can achieve the same results by converting the numbers to strings as well as we saw in the String slicing approach.

### Algorithm

- We first type cast the integer into a string to perform various string methods.
- We then iterate until the middle of the string and check if the element at the ith index is same as that of the (n-i-1)th index. If the condition satisfies for all the digits, then the number is said to be palindrome.

```
# Method to check for Palindrome number

def checkForPalindrome(s):

    st = str(s)
    mid = int(len(st) / 2)

    for i in range(0, mid):
        if st[i] != st[len(st) - i - 1]:
            return False

    return True

# Driver Code
s = 1221

if checkForPalindrome(s):
    print("Palindrome")
else:
    print("Not Palindrome")
```

Output
`Palindrome`

### Complexity

**Time Complexity**:
Since, we are using only a for loop with a simple check, therefore the time complexity of the above code is `O(N)`, where N is the half of the length of the number / number of digits.

**Space Complexity**:
Since, we aren't storing any values inside of our function, therefore the space complexity of the code is `O(1)`.

## Approach 5: Built in Reversed Function

We have started to discuss about type casting the integer before performing the function.
And in this approach, we will discuss on how we can use the built in `reversed()` method in python to achieve the desired result.

```
def checkForPalindrome(s):
    rev = ''.join(reversed(str(s)))

    if str(s) == rev:
        return True

    return False


# Driver Code

string = 1231

if checkForPalindrome(string):
    print("Palindrome")
else:
    print("Not Palindrome")
```

Output
`Not Palindrome`

We got the exact same output as required but with much more flexible code and dynamically managing the values.

## Summary

In this article, we learnt about another famous DSA problem **Palindrome Number** and we discussed with very beginner methods to very advanced methods of how to solve the problem using Python.

After discussing all the approaches and having a brief about the time and space complexities of those methods, we can conclude that the string methods are much more efficient and optimized than going along with the numerical methods.
