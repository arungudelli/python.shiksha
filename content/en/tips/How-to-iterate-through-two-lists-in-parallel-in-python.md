---
title: "How to iterate  through two lists in parallel in Python"
description: "we can iterate 2 python lists in parallel by using 3 methods, using zip(),using for loop,using enumerate
"
date: "2022-03-09T00:00:00+00:00"
draft: false
link: "iterate  through two lists in parallel"
---

We can iterate 2 python lists in parallel by using 3 methods.

1. using zip()
2. using for loop
3. using enumerate

Using these three methods, we can obtain a distinct one-list advantage over the two-list advantage.

Example:

```
List1 =[1,2,3,4,5]
List=[‘a’,’b’,’c’,’d’,’e’]
```

These are the 2 lists to iterate on, after the iteration process  we should have 1 clear list.

After iteration our list is

```
1	a
2	b
3	c
4	d
5	e
```

## using `zip()` function to iterate 2 list parallel in python

We can use `zip()` function, which is a built-in python function used to iterates tuples and lists.

To iterate two lists, use `zip()` function as explained below

We have two lists, favorite fruits and vegetables. And after iteration, we will get one single list.

```
li_1 = ['apple','banana','papaya']
li_2 =['tomato','potato','carrot']
print('fruits',"  "  'vegetables'
for f, o in zip(li_1,li_2):
    print(f,o)
```

output :

```
fruits vegetables
apple  tomato
banana  potato
papaya  carrot
```

Like this, we have 1 list that is favorite fruits and vegetables. 

Iteration is done in such a way that the first item from the first list and the first item from the second list are paired, and the next second item from the first list and the second item from the second list are paired, and so on until all items in those two lists are completed.

We have one disadvantage in that if we have the same number of items in the two lists, it is no problem to pair to that particular item. 

The problem here is that if we have 4 items in the first list and 3 items in the second list, that 4th item wants to pair to some particular item, but that is not possible. 


```
li_1 = ['apple','banana','papaya','guava']
li_2 =['tomato','potato','carrot']
print('fruits',"  "  'vegetables')
for f, o in zip(li_1,li_2):
    print(f,o)
```

output:

```
fruits vegetables
apple  tomato
banana  potato
papaya  carrot
```


List1 has four items, but the fourth item i.e., `guava` is not displayed. 


To avoid this, we use the `itertools` method, which run through all of the elements in an iteration.

```
import itertools
li_1 = ['apple','banana','papaya','guava']
li_2 =['tomato','potato','carrot']
print('fruits',"  "  'vegetables')
for f,o in itertools.zip_longest(li_1,li_2):
    print(f,o)
```

output:

```
fruits vegetables
apple  tomato
banana  potato
papaya  carrot
guava  None
```

We successfully obtained an output in which all items were displayed.


## To iterate two lists, use for loop in python

It is quite simple, we will not use any other built-in Python functions in this case, instead we will use `for` loop along with `range`.

```
fruits=['apple','banana','papaya']
vegetables=['tomato','potato','carrot']
print("fruits   vegetables")
for i in range(len(fruits)):
    print(fruits[i],"   ",vegetables[i])
```

output:

```
fruits  vegetables
apple  tomato
banana  potato
papaya  carrot
```

## Use `enumerate()` to iterate two lists in Python

`enumerate()` is a built-in Python function, and used to iterate through a sequence and it will keep track  of both index and the number. 

```
fruits=['apple','banana','papaya']
vegetables=['tomato','potato','carrot']
print("fruits   vegetables")
for n, f in  enumerate(fruits):
    print(f,"   ",vegetables[n])
```

output:

```
fruits  vegetables
apple  tomato
banana  potato
papaya  carrot
```

`enumerate()` function takes a collection and returns an enumerate object,this adds a counter as the key of the enumerate object.

```
x = ('apple','banana','papaya' )
y = enumerate(x)
print(list(y))
```

output:

```
[(0,apple),(1,banana),(2,papaya)]

```