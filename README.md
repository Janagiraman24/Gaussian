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
### Program to find the solution of a matrix using Gaussian Elimination.
### Developed by: Janagiraman.M
### RegisterNumber: 212224230101
```
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())

for i in range(n):
    if(a[i][j]==0.0):
        sys.exit('Divide by zero detected')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print("X%d = %.2f"%(i,x[i]),end=' ')
```

## Output:
<img width="1207" height="735" alt="Screenshot 2025-09-09 141105" src="https://github.com/user-attachments/assets/fd70dccc-1b29-42c1-a56c-fb21ceeca3bc" />
<img width="861" height="466" alt="Screenshot 2025-09-09 141112" src="https://github.com/user-attachments/assets/f768eaf5-aae2-4d8d-b5ce-44b10140ffff" />

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

