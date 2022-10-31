
#                       ************************** CODE Discription **************************

# There is already exist Lagrange_interpolation algorithm, there is a python program for this to automate.

# 1) We include / use numpy library to use arrays.
# 2) Program flow:
#                1) Take input of data points ( for size of the array ), then initialize it with zero ( for both x and y ).
#                2) Take data for x and y.
#                3) Input of interpolation point
#                4) Finally calculates the interpolated value.


import numpy as np
n = int(input('Enter number of data points: '))

x = np.zeros((n))
y = np.zeros((n))

print('Enter data for x and y: ')
for i in range(n):
    x[i] = float(input( 'x['+str(i)+']='))
    y[i] = float(input( 'y['+str(i)+']='))

xp = float(input('Enter interpolation point: '))

# Set interpolated value initially to zero
yp = 0

# Implementing Lagrange Interpolation
for i in range(n):
    p = 1
    
    for j in range(n):
        if i != j:
            p = p * (xp - x[j])/(x[i] - x[j])
    
    yp = yp + p * y[i]    

print("Interpolated value at: ",f"{xp:.3f}","is ",f"{yp:.3f}")