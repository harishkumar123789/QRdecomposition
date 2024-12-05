# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.
2.
3.
4.
5.
## Program:
### Gram-Schmidt Method
Program to QR decomposition using the Gram-Schmidt method
```
Developed by: HARISH KUMAR S
RegisterNumber: 24010415

import numpy as np
def QR_Decomposition(A):
    n,m=A.shape
    Q=np.empty((n,n))
    u=np.empty((n,n))
    u[:,0]=A[:,0]
    Q[:,0]=u[:,0]/np.linalg.norm(u[:,0])
    for i in range(1,n):
        u[:,i]=A[:,i]
        for j in range(i):
            u[:,i]-=(A[:,i]@Q[:,j])*Q[:,j]
        Q[:,i]=u[:,i]/np.linalg.norm(u[:,i])
    R=np.zeros((n,m))        
    for i in range(n):
        for j in range(i,m):
            R[i,j]=A[:,j]@Q[:,i]
    print("The Q Matrix is \n",Q)        
    print("The R Matrix is \n",R)
a=np.array(eval(input()))    
QR_Decomposition(a)
```
##Output
![alt text](<Screenshot 2024-12-05 185921.png>)
![alt text](<Screenshot 2024-12-05 185945.png>)
![alt text](<Screenshot 2024-12-05 190009.png>)
## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
