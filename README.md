# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Use 'n' for matrix size and initialize matrix 'a' and vector 'x' with zeros
2. Input matrix a elements and store in 2D numpy array
3. Gaussian elimination without partial pivoting to solve a matrix is done using the code
4. Back substitution
5. End the program

## Program:
Program to solve a matrix using Gaussian elimination without partial pivoting.
                                   
                                   #Developed by: SADHANA SHREE B
                                   #RegisterNumber: 212223230177

                                   import numpy as np
                                   import sys
                                   n= int(input())
                                   a= np.zeros((n,n+1))
                                   x= np.zeros(n)
                                   for i in range(n):
                                        for j in range(n+1):
                                            a[i][j]=float(input())
                                    for i in range(n):
                                        if a[i][j] == 0.0:
                                           sys.exit('Divide by zero detected!')
                                        for j in range(i+1,n):
                                             ratio = a[j][i]/a[i][i]
        
                                             for k in range(n+1):
                                                 a[j][k]=a[j][k] - ratio * a[i][k]

                                  x[n-1]=a[n-1][n]/a[n-1][n-1]
                                  for i in range(n-2,-1,-1):
                                       x[i] = a[i][n]
    
                                       for j in range(i+1,n):
                                           x[i]=x[i] - a[i][j]*x[j]
    
                                       x[i] = x[i]/a[i][i]
    
                                  for i in range(n):
                                      print('X%d = %0.2f'%(i,x[i]),end = ' ')

## Output:

![Screenshot 2024-04-27 031044](https://github.com/SadhanaShreee/Gaussian/assets/144517664/c94e78ab-e9cd-4545-a9b3-70d2635c88db)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

