# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Input Matrix:
Read the order n and the augmented matrix [A∣B].
2. Forward Elimination:
Convert the matrix into an upper triangular form by eliminating elements below the main diagonal using row operations.
3. Back Substitution:
Find the values of unknowns starting from the last equation up to the first.
4. Display Result:
Print the solution of the system of equations.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Sivasakthi S
RegisterNumber: 25017123

'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Sivasakthi S
RegisterNumber: 25017123
'''
import sys
import numpy as np
data=list(map(float,sys.stdin.read().split()))
n=int(data[0])
vals=data[1:]
A=np.array(vals,dtype=float).reshape(n,n+1)
for k in range(n-1):
    for i in range(k+1,n):
        factor=A[i,k]/A[k,k]
        A[i,k:]-=factor*A[k,k:]
x=np.zeros(n)
for i in range(n-1,-1,-1):
    x[i]=(A[i,-1]-np.dot(A[i,i+1:n],x[i+1:n]))/A[i,i]
parts=[f"X{i} = {x[i]:.2f}" for i in range(n)]
print(" ".join(parts))
    
*/
```

## Output:
<img width="1920" height="1200" alt="Screenshot (117)" src="https://github.com/user-attachments/assets/7f5066cc-093e-4561-bce9-7e9e03f477e9" />
<img width="1920" height="1200" alt="Screenshot (118)" src="https://github.com/user-attachments/assets/fe4f6355-84e0-449c-904d-20205d79048d" />
<img width="1920" height="1200" alt="Screenshot (119)" src="https://github.com/user-attachments/assets/8f5743dd-35c6-4a70-b072-83bc6fc11d11" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

