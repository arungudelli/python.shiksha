---
title: "Roman to Integer Problem in Python"
description: ""
lead: ""
date: 2022-10-01T01:30:00+02:00
lastmod: 2022-10-01T14:30:00+02:00
draft: false
images: []
type: docs
toc: true
---

## Problem Statement

```text
Given a Roman literals, convert it into an integer in Python

Symbol       Value

I             1
V             5
X             10
L             50
C             100
D             500
M             1000
```

## Constraints:

- $1$ $\le$ input.length $\le$ $15$
- `input` contains only the characters (`I`, `V`, `X`, `L`, `C`, `D`, `M`).
- `input` is a valid roman numeral in the range $[1, 3999]$.

## Examples

```python
Input: s = "III"
Output: 3
Explanation: III = 3.
```

```python
Input: s = "LVIII"
Output: 58
Explanation: L = 50, V= 5, III = 3.
```

## Solution

```python
def romanToInt(s):
    # Roman Dictionary to store the values of roman literals
    roman = {
        "I": 1,
        "V": 5,
        "X": 10,
        "L": 50,
        "C": 100,
        "D": 500,
        "M": 1000
    }

    # Initialize the result
    ans = 0

    # Iterate over the string
    for i in range(len(s) - 1):
        # If the current value is less than the next value then subtract the current value from the result else add the current value to the result
        if roman[s[i]] >= roman[s[i + 1]]: 
            ans += roman[s[i]]
        else: 
            ans -= roman[s[i]]
    
    # add the value of the last character
    ans += roman[s[len(s) - 1]]

    # return the result
    return ans;


# Test the function
def main():
    Roman = input("Enter the Roman literals: ")
    print('Roman to Integer: ', romanToInt(Roman))

# Call the main function
if __name__ == '__main__':
    main()
```

## Complexity Analysis

- Time Complexity: $O(n)$, where $n$ is the length of the input string.
- Each access to the dictionary `roman` is $O(1)$ as they are $7$ characters, so the time complexity is $O(n)$.
- Space Complexity: $O(n)$, where $n$ is the length of the input string.
