# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
import numpy as np
import sys
solve using for loop
print the output
## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by: S.S.Sriram
RegisterNumber: 22004880
'''
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
        x[i]= x[i]-arr[i][j]*x[j]
    x[i]= x[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
    
*/
```

## Output:
![image](https://user-images.githubusercontent.com/120554177/214800940-0f329eed-2fe4-42ba-b9b7-1eb734c2f5e9.png)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

