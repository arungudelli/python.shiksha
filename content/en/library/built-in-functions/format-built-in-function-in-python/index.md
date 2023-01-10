---
title: "python format() syntax, usage and examples in python"
description: "The 'format()' function is a one of the built-in functions in python"
date: "2022-08-22T10:00:05+09:00"
draft: false
link: "format() Built-in functions"
author: "harika"
---

## `format()` function in python

1. The `format()` function is a one of the built-in functions in python.
2. The `format()` is used for `Formats a specified value`.

The string's placeholder is filled with the formatted value(s) inserted by the format() method. 
The placeholder is defined using curly brackets: {}.


## `format()` function Syntax

```python
string.format(value1, value2...) 
```
## `format()` function parameters

value1, value2... 	Required. One or more values that should be formatted and inserted in the string.

The values can be of any data type.

### `format()` function Examples:

let's go through couple of examples to understand `format()` function in python

###  Example 1:

```python
print("{} is my country".format("India"))
```
output:

```python
India is my country
```
### Example 2:

```python

# integer 
print(format(5648, "*>+7,d"))

# float number
print(format(690.4567, "^-09.3f"))
```
output:

```python
*+5,648
0690.4570
```

## `format()` Formatting Types:

Inside the placeholders you can add a formatting type to format the result:

:< 	
Left aligns the result (within the available space)

:> 	
Right aligns the result (within the available space)

:^ 	
Center aligns the result (within the available space)

:= 	
Places the sign to the left most position

:+ 	
Use a plus sign to indicate if the result is positive or negative

:- 	
Use a minus sign for negative values only

:g 		
General format

:G 		
General format (using a upper case E for scientific notations)

:o 	
Octal format

:x 	
Hex format, lower case

:X 	
Hex format, upper case

:n 		
Number format

:% 	
Percentage format

:  	
Use a space to insert an extra space before positive numbers (and a minus sign before negative numbers)

:, 	
Use a comma as a thousand separator

:_ 	
Use a underscore as a thousand separator

:b 	
Binary format

:c 		
Converts the value into the corresponding unicode character

:d 	
Decimal format

:e 	
Scientific format, with a lower case e

:E 	
Scientific format, with an upper case E

:f 	
Fix point number format

:F 	
Fix point number format, in uppercase format (show inf and nan as INF and NAN)


## Summary
In this tutorial we learnt about Python `format()` function with simple examples.
