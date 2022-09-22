---
title: "How do i append to a file"
description: "How you can easily i append to a file in python"
date: "2022-09-04"
draft: false
link: "How do i append to a file"
author: "Shittu Olumide"
---

In Python, reading, writing, and editing files are common tasks since the language gives us built-in functions to do so. 

As a developer there are so many reason why you will want to read, write and also edit the files in your project, and python really offers the flexibility to do so in very simple and easy ways. There are a couple of file handling operations in python such as `r` which works for reading the file, `w` opening a file and writing to it, `a` opens a file for appending at the end of the file without truncating it, `+` opens a file for updating(reading & writing) and so on.


In this article, I will be discussing briefly how you can easy append to a file using the python programming language and how to use the append operation effectively.

### What is a file?
A file is a designated spot on the hard drive where associated data is kept. It is used to keep data in non-volatile memory for all time (e.g. hard disk). 

A file must first be opened before we can append to it. It must be closed once we are finished so that the resources associated with the file can be released.

Consequently, a file operation in Python happens in the following order:
- Open a file
- Append to the file
- Close the file


### How to append a text to a file
There are different methods to append a text to a file and I will be showing you that shortly, but firstly let us talk about how it works.
So bascially when you are trying to append to a file, what you are trying to do is that you are trying to add a word, character or a sentence to the end of the file. In simpler terms, whatever goes into the `.write()` method will be added to the end of the text file.

Let us take a look at the different way to append to a file.

#### Using the with statement
The concise shorthand of a try-catch block is replaced with the with statement. More significantly, it makes sure that resources are closed immediately after being processed. Reading from or writing to a file is a typical example of using the with statement. A context manager is a function or class that supports the with statement.

Imagine you have a file with the name `example.txt` and the content looks like this.

> The sun shines brighter in the day especially in the afternoon

Code sample:
```python
with open("example.txt","a") as file:
    file.write("I like to play in the sun light")
```

The example.txt file should look like this now.

> The sun shines brighter in the day especially in the afternoon, I like to play in the sun light

When you're done appending to the file, the with statement immediately closes it.

#### Using the open function 
The file is opened via the open() function, which also returns the appropriate file object. 
The syntax of `open()` is:

```python
open(file, mode='')
```
Let's say we have a file called `example2.txt` with this content:

> The quick brown fox jumps over the lazy dog And says

Now let’s append text 'Hi' at the end of this file,
```python
    # Open a file with access mode 'a'
    ham = open('example2.txt', 'a')

    # Append 'Hi' at the end of file
    ham.write(' Hi.')
    # Close the file
    ham.close()
```
Contents of the file example2.txt’ will now be,
> The quick brown fox jumps over the lazy dog And says Hi.

#### Append to a file as a new line 
Let's start with the primary technique, discuss its shortcomings, and look for ways to make it better.

File should be opened in append and read mode `('a+')`. The file's end is indicated by both the read and write cursors, the place the read cursor at the file's beginning. Check to see if the file is empty or not by reading some content from it. If the file is not empty, use the `write()` function to insert `"\n"` at the end of the file. Using the `write()` function, add a specified line to the file and close the file.

We hava a file named `test.txt` with this content:

> This is a test file and I am going to append a new line to it.

Let's append the new line to the `text.txt` file,

```python
with open("test.txt", "a+") as ram:
    ram.seek(0)
    data = ram.read(100)
    if len(data) > 0 :
        ram.write("\n")
    ram.write("This is the new added line.")
```
I had to open the file in append & read mode ('a+'), then I moved the cursor to the start of the file, I did a check to see if the file is not empty then I append the text at the end of the file in a new line.

The `test.txt` should look like this now,

> This is a test file and I am going to append a new line to it.
> This is the new added line.

#### Append multiple lines
The File should be opened in append & read mode `('a+')`,the file's end is indicated by both the read and write cursors. Make sure you place the read cusor at the file's beginning. Check to see if the file is empty or not by reading some content from it. If the file is empty set appendEOL as False, for each list item if appendEOL is False and its first element in the List is False. Don't use the `write()` function to append `'\n'` to the file's end. Else using the `write()` function, append '\n' to the end of the file. Utilize the `write()` function to append the element to the file then close the file.

We have a file with the name `test.txt` containing,
> This ia a line
> This ia a second line

Lets write a function to add multiple lines to this file.

```python
def add_lines(file_name, line_list):
    with open(file_name, "a+") as ham:
        appendEOL = False
        ham.seek(0)
        data = ham.read(100)
        if len(data) > 0:
            appendEOL = True
        for line in line_list:
            if appendEOL == True:
                ham.write("\n")
            else:
                appendEOL = True
            ham.write(line)
```
if we pass a series of lines to our `line_list` array,

```python
line_list = ['This is the third line', 'Followed by the fourth line']
```
Let's call the function and append the new lines to it

```python
# Append strings in list as seperate new lines in the end of file
append_multiple_lines('test.txt', line_list)
```
The content of the file 'test.txt' is,
> This ia a line
> This ia a second line
> This is the third line
> Followed ny the fourth line

It appended all the given strings in the list as newlines in the file.



## Conclusion

We covered a lot in this article on how to append to a file. We looked at using the `with` statement, the `open` function, append to a file as a new line and appending multiple lines to a file. I genuinely hope that this article has taught you one or two things.





