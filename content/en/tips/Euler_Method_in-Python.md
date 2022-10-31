

#                       ************************** CODE Discription ***********************************

# There is already exist a algorithm of Euler_Method, there is a python program for this to automate.


# 1) We include / use library called sympy which is used to simplify the function/expression using simpify() , calculates
#    its derivative and then find the numeric value using sympy.subs()
# 2) var( y , t ) generates two variables y and t which is commonly used in ODE,  Ex: y' = 1 + (t-y)**2
# 3) Program flow:
#                  1) First take the lower and upper limit of function.
#                  2) value of h (equally space)
#                  3) Take ODE ( y') in the form like [ -y + t*y**(1/2) ]
#                  4) Then take input the initial value of the ODE
#                  5) Finally calculates.

from sympy import var
from sympy import sympify

a = float(input("\nEnter value of lower-limit: "))
b = float(input("\nEnter value of upper-limit: "))
y , t = var('y t')
h = float(input("\nEnter value of h: "))
der_function = input("\nEnter derivative of function: ")
expr1 = sympify(der_function)
ini = float(input("\nEnter initial output value of function: ")) 

final = ini
i=a
n = 0
print("\nIteration     tn        Wn")
while i!=b+h:
    print(n,"           ",i,"    ",f"{final:.6f}")
    final = final + h*(expr1.subs( [ (t,float(i)) , (y,float(final)) ] ) )
    i=i+h
    n+=1