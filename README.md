# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import numpy and sys module to use built-in functions for calculation.
2.Get input from the user for number of rows and add it by 1 for number of columns and by using np.zeros() set the matrix as null matrix.
3.Using nested for loop find the ratio and perform the elementary row operations and find the final matrix.
4.End the program. 

## Program:
```python
#Program to find the solution of a matrix using Gaussian Elimination.
#Developed by: HARIHARAN A
#RegisterNumber: 22001891

import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
x[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=arr[i][n]
    for j in range(i+1,n):
            x[i]=x[i]-arr[i][j]*x[j]
    x[i]=x[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")     #X0 = 53.35 X1 = -8.88 X2 = -4.40

```

## Output:
![image](https://user-images.githubusercontent.com/120353431/213848527-7cfff99a-22ea-4133-898b-d6b3be56f1ae.png)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

