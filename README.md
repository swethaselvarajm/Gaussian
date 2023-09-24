# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable.
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3. For that we want to make a range accorting to our program output.
4. Then print the program with correct form then the output will display.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: SWETHA.S
RegisterNumber: 212222230155
import numpy as np
import sys

#Reading no of unknowns
n= int(input())

#Making numpy array of n x n+1 size and initializing to zero for storing soln vector
a = np.zeros((n,n+1))

#Making numpy array of n size and initializing to zero for storing soln vector
x = np.zeros(n)

#Reading augmented matrix coefficients
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
        
#Applying Gauss Elimination
for i in range(n):
    if a[i][j] == 0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]

# back substitution
x[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    
    for j in range(i+1,n):
        x[i] = x[i] - a[i][j]*x[j]
        
    x[i] = x[i]/a[i][i]
    
#Displaying the soln
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]), end = ' ')
*/
```

## Output:
![Screenshot 2023-09-24 202502](https://github.com/swethaselvarajm/Gaussian/assets/119525603/cd5b792a-fd7b-4fad-aebb-a93d3a0a9fe3)

![Screenshot 2023-09-24 202539](https://github.com/swethaselvarajm/Gaussian/assets/119525603/ba599b5c-5fd3-4623-af60-7cd53ac13bc9)

![Screenshot 2023-09-24 202550](https://github.com/swethaselvarajm/Gaussian/assets/119525603/c80ca0b0-abe1-4bb8-9453-73360273ac67)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

