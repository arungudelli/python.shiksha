---
title: "Working with DataFrames in Python's Pandas library"
description: "How we can interact with and use DataFrames in Python."
date: "2022-04-21T22:21:00"
draft: false
author: "JamesCBartlett"
---

In this article, we will briefly discuss **How we can interact with and use DataFrames in Python.**.

## Overview of Pandas in Python

If you have not already, read the article on working with Series in Pandas to understand the basics of the Pandas module before reading this.

Pandas is a powerful data manipulation library for Python. It provides data structures to efficiently handle large datasets and perform operations on them. Pandas is commonly used to work with CSV files so is very useful to know if you have to work with excel which is a widely used software.

## Overview of Series in Pandas

A DataFrame is a two-dimensional table-like data structure that can store mixed data. It is very similar to a spreadsheet or a SQL table, and it is one of the most commonly used data structures in Pandas. A DataFrame consists of rows and columns, where each column can have a different data type. You can perform various operations on DataFrames, such as filtering, sorting, grouping, merging, and more. You can consider a DataFrame to be a number of Series put together.

## Creating a DateFrames

You can create a DataFrame in several ways, including from a dictionary, a NumPy array, a CSV file, or by merging multiple DataFrames. Here are a few examples:

## Creating a DataFrame from a dictionary

By passing in a dictionary we can create a DataFrame, as shown:

```python
import pandas as pd

data = {'name': ['Alice', 'Bob', 'Charlie', 'David'],
        'age': [25, 30, 35, 40],
        'city': ['New York', 'London', 'Paris', 'Tokyo']}

df = pd.DataFrame(data)
print(df)
```

Output

```
       name  age      city
0     Alice   25  New York
1       Bob   30    London
2   Charlie   35     Paris
3     David   40     Tokyo

```

## Creating a DataFrame from a NumPy array

By passing in a NumPy array we can create a DataFrame, as shown:

```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

df = pd.DataFrame(arr, columns=['a', 'b', 'c'])
print(df)

```

Output

```
   a  b  c
0  1  2  3
1  4  5  6
2  7  8  9

```

## Creating a DataFrame from a CSV file
By passing in a CSV file name, providing the file name is correct and present, we can create a DataFrame, as shown:

```python

df = pd.read_csv('my_data.csv')
print(df)

```

Output

```
#Whatever data is in the file will be displayed here
```

## Accessing a DataFrame

You can view the contents of a DataFrame using various methods, such as head(), tail(), and sample(). Here are a few examples:

```python
# Viewing the first few rows
print(df.head())

# Viewing the last few rows
print(df.tail())

# Viewing a random sample of rows (in this case 3 as it is passed in)
print(df.sample(3))
```

## Indexing and Selecting DataFrames

You can select specific rows and columns from a DataFrame using various methods, such as loc[], iloc[], and []. Here are a few examples:

```python
# Selecting a single column
print(df['name'])

# Selecting multiple columns
print(df[['name', 'age']])

# Selecting a single row by index label
print(df.loc[0])

# Selecting a single row by index position
print(df.iloc[0])

# Selecting multiple rows by index label
print(df.loc[[0, 2]])

# Selecting multiple rows by index position
print(df.iloc[[0, 2]])
```

Output
```
0      Alice
1        Bob
2    Charlie
3      David
Name: name, dtype: object

      name  age
0    Alice   25
1      Bob   30
2  Charlie   35
3    David   40

name       Alice
age           25
city    New York
Name: 0, dtype: object

name       Alice
age           25
city    New York
Name: 0, dtype: object

      name  age      city
0    Alice   25  New York
2  Charlie   35     Paris

      name  age      city
0    Alice   25  New York
2  Charlie   35     Paris
```

## Filtering DataFrames

You can filter a DataFrame based on a given condition using boolean indexing. Here's an example:

```python
print(df[df['age'] > 30])
```

Output

```
      name  age   city
2  Charlie   35  Paris
3    David   40  Tokyo
```

## Handling Missing Values

You can handle missing values in a Series using the fillna() method in a number of ways.

```python
df = pd.DataFrame({'A': [1, 2, np.nan], 'B': [4, np.nan, np.nan], 'C': [7, 8, 9]})

# Replace missing values with a specific value
print(df.fillna(value=0))

# Drop rows with missing values
print(df.dropna())

# Drop columns with missing values
print(df.dropna(axis=1))

```

OUTPUT:
```
     A    B  C
0  1.0  4.0  7
1  2.0  0.0  8
2  0.0  0.0  9

     A    B  C
0  1.0  4.0  7

   C
0  7
1  8
2  9
4

```

## Sorting DataFrames

You can sort a DataFrame based on one or more columns using the sort_values() method. Here's an example:

```python
# Sorting a DataFrame
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'age': [25, 30, 35, 40],
                   'city': ['New York', 'London', 'Paris', 'Tokyo']})

print(df.sort_values(by='age'))
```

Output
```
       name  age      city
0     Alice   25  New York
1       Bob   30    London
2   Charlie   35     Paris
3     David   40     Tokyo
```

## Grouping DataFrames

You can group a DataFrame based on one or more columns using the groupby() method. Here's an example:

```python
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'age': [25, 30, 35, 40],
                   'city': ['New York', 'London', 'Paris', 'Tokyo']})

grouped = df.groupby('city')

for name, group in grouped:
    print(name)
    print(group)
    print()

```

Output
```
London
  name  age    city
1  Bob   30  London

New York
    name  age      city
0  Alice   25  New York

Paris
      name  age   city
2  Charlie   35  Paris

Tokyo
    name  age   city
3  David   40  Tokyo

```

## Merging DataFrames

You can merge multiple DataFrames using the merge() method. Here's an example:

```python
df1 = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                    'age': [25, 30, 35, 40],
                    'city': ['New York', 'London', 'Paris', 'Tokyo']})

df2 = pd.DataFrame({'name': ['Charlie', 'David', 'Ella', 'Frank'],
                    'salary': [5000, 6000, 7000, 8000]})

merged = pd.merge(df1, df2, on='name')

print(merged)

```

Output:
```
      name  age      city  salary
0  Charlie   35     Paris    5000
1    David   40     Tokyo    6000
2     Ella  NaN       NaN    7000
3    Frank  NaN       NaN    800

```
## Manipulating columns

You can manipulate columns in a number of ways, here are some examples:

## Adding a New Column

You can add a new column to a DataFrame using indexing or the assign() method. Here's an example:

```python
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'age': [25, 30, 35, 40],
                   'city': ['New York', 'London', 'Paris', 'Tokyo']})

df['salary'] = [5000, 6000, 7000, 8000]

print(df)

# Using the assign() method
df = df.assign(debt=[1000, 2000, 3000, 4000])

print(df)
```

Output:
```
      name  age      city  salary
0    Alice   25  New York    5000
1      Bob   30    London    6000
2  Charlie   35     Paris    7000
3    David   40     Tokyo    8000

      name  age      city  salary  debt
0    Alice   25  New York    5000  1000
1      Bob   30    London    6000  2000
2  Charlie   35     Paris    7000  3000
3    David   40     Tokyo    8000  4000


```

## Renaming Columns

You can rename the columns of a DataFrame using the rename() method. Here's an example:

```python
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'age': [25, 30, 35, 40],
                   'city': ['New York', 'London', 'Paris', 'Tokyo']})

df = df.rename(columns={'name': 'Name', 'age': 'Age', 'city': 'City'})

print(df)
```

Output:
```
      Name  Age      City
0    Alice   25  New York
1      Bob   30    London
2  Charlie   35     Paris
3    David   40     Tokyo

```

## Removing columns

You can drop one or more columns of a DataFrame using the drop() method. Here's an example:

```python
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'age': [25, 30, 35, 40],
                   'city': ['New York', 'London', 'Paris', 'Tokyo']})

df = df.drop(columns=['age', 'city'])

print(df)
```

Output
```
      name
0    Alice
1      Bob
2  Charlie
3    David

```

## Saving Dataframes as a CSV file

You can save DataFrames that you create and edit to CSV files to be viewed in excel or other spreadsheet software. Here is an example:

```python
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'age': [25, 30, 35, 40],
                   'city': ['New York', 'London', 'Paris', 'Tokyo']})

# Save the DataFrame to a new CSV file
df.to_csv('data.csv', index=False)
```

If you were to look in the folder the file is in you would find a file called data.csv containing the data in the DataFrame.

## Conclusion

To conclude, this article has discussed a number of ways to manipulate and process a Pandas DataFrame. By understanding both Series and DateFrames you now have the framework to master Pandas as a library and begin to put your skills to use. Good luck