---
title: "4 methods for Writing a list to a file in Python"
description: "In this article, we will see about all the different methods about how to write a list onto a file in python."
date: "2022-09-21T00:00:00+09:00"
draft: false
author: "dmohanty"
---

Writing lines to a file in python is quite simple and easy, but is it also true for writing lists to a file.

Let’s see.

In this article, we will see about all the different methods about how to write a list onto a file in python.

## Method 1: Using the `for` loop

This is again one of the many use cases of the `for` loop.

The mighty `for` loop is capable of solving many of the problems in python.

For **writing a list to a file in python, we have to use both the `for` loop and the `write()` method**.  

By this we can imply iterate through a list of strings and by the help of the `write()` method, write each iteration to the file.

```python
lines = ['Hello','World', 'Welcome to Python.shiksha']
path = "E:/Sample Folder/test.txt"
f=open(path,'w')
for i in lines:
    f.write(i+'\n')

f.close()
```

This is a very beginner method of solving this problem i.e. good and effective for novice coders.

But if you are not a beginner, you might not be interested in the same.

Let’s see the other methods.

## Method 2: Using the `string.join()` method

Since, python is a very versatile language, it has a lot of inbuilt methods to work on with, thus there is also a string method that we can use in order to write a list to a file.

Instead of a `for` loop we can use the `join()` method, by the help of which we can join the whole list using a `delimiter` and forming one super string and then we can use the `write()` method to add the super string onto our file.

```python
lines = ['Hello','World', 'Welcome to Python.shiksha']
path = "E:/Sample Folder/test.txt"
f=open(path,'w')
string='\n'.join(lines)
f.write(string)

f.close()
```

Thus pretty easily by using the `join()` method we wrote a list to a file.

But can we make this code a little bit more compact?

Yes, we can.

## Method 3: Using `string.join()` with `open()` method

In the previous section, we saw about the `join()` method but can we make that code more *compact*. 

Yes, of course we can, by making the opening of the file using `open()` method and using the `string.join()` method directly.

```python
lines = ['Hello','World', 'Welcome to Python.shiksha']
path = "E:/Sample Folder/test.txt"
with open(path,'w') as f:
  f.write('\n'.join(lines))
```

## Method 4: Using the `writelines()` method

Previously we saw the use of the `write()` method, which takes in a string as an argument and writes it onto a file. 

But files in python also have a `writelines()` method which takes in a **list of strings** as the argument and writes the list onto a file.

We can directly use the list but in order to make our text look better and cleaner, firstly we need to append the **newline** character after every line by using the `map()` function.

```python
lines = ['Hello','World', 'Welcome to Python.shiksha']
path = "E:/Sample Folder/test.txt"
f=open(path,'w')
lines=map(lambda x:x+'\n', lines)
f.writelines(lines)
f.close()
```

I am using `lamba` function append new line to every element in a list.

## Conclusion

In this article, we discussed in detail about the various methods that we can use in order to write a list to a file in python.

We started our discussion from the beginner approach i.e. a `for` loop and later extended it to the inbuilt `join()` method followed by its compact version and then finally concluding with the programmer approach i.e. the `writelines()` method.
