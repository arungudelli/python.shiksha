
#       ************************** CODE Discription ***********************************


# 1) We include / use library called sympy which is used to simplify the function/expression using simpify() 
#   and then find the its numeric value using sympy.subs()
# Program flow:
#             1) Take inputs of lower and upper limits.
#             2) Then wants to take function as input.
#             4) Take input of no: of maximum iterations and tolerance value
#             5) Program will terminate if, tolerance value is matched / pre-value == cur-value / no: of iteration will greater than user input
#             6) Check if solution exist or not.
#             7) Final print the outputs according to the method.

import sympy as sym
from sympy import var
from sympy import sympify

P0 = float(input("Enter value of P0: "))
P1 = float(input("Enter value of P1: "))

x = var('x')
print("Enter function: ")
function  = input()

expr1 = sympify(function)

r = int(input("Enter max no: of iterations: "))
e = float(input("Enter tolerance value: "))

text0 = expr1.subs(x, float(P0))
text1 = expr1.subs(x,float(P1))
P = (P0*text1 - P1*text0) / (text1 - text0)
error = P
if text0 * text1 > 0.0:
    print("Solution Doesn't exist because, it doesn't satisfies the intermediate value theorem")
else:
    i=1
    termination = True
    while termination:
        pre = P1

        text0 = expr1.subs(x, float(P0))
        text1 = expr1.subs(x,float(P1))
    
        P = (P0*text1 - P1*text0) / (text1 - text0)
        far = P
        termination = abs( expr1.subs(x,float(P)) ) > e 
        if( (pre == far) or i>r):
            break
        print("At Iteration no: ",i, "P= ",f"{P:.6f}" , "and f(P)= ",f"{expr1.subs(x, float(P)) :.6f}","and error ",f"{error:.6f}")
        i+=1
        error = abs(pre - far)
        P0 = P1 
        P1 = P