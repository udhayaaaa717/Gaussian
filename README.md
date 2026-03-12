# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Write a Python program for the problem.
2. Import the numpy library.
3. Apply Gaussian elimination to solve the matrix.
4.. Run the program.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Udhaya dharshini 
RegisterNumber: 212225230288
*/
```
import numpy as np
import sys

n = int(input())
a = np.zeros((n, n+1))
x = np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j] = float(input())

for i in range(n):
    if a[i][i] == 0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1, n):
        ratio = a[j][i] / a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]

x[n-1] = a[n-1][n] / a[n-1][n-1]

for i in range(n-2, -1, -1):
    x[i] = a[i][n]
    for j in range(i+1, n):
        x[i] = x[i] - a[i][j] * x[j]
    x[i] = x[i] / a[i][i]

for i in range(n):
    print('X%d = %0.2f' % (i, x[i]), end=' ')
    ```

## Output:
![gaussian elimination]()
<img width="1732" height="933" alt="image" src="https://github.com/user-attachments/assets/aba6f4f0-84a6-4ec8-aee1-3c2f7241c3f4" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

