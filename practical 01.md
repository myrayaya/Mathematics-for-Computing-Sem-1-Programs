## Practical - 1: Find the cofactor, determinant, adjoint and inverse of the matrix

### Input / Code
```
import numpy as np

NR = int(input("Enter the no. of rows: "))
NC = int(input("Enter the no. of columns: "))

print("Enter the entries in a single line (seperated by space: ")

entries = list(map(int, input().split()))

A = np.array(entries).reshape(NR, NC)
print("Matrix A is as follows : ", '\n', A)

A_Inv = np.linalg.inv(A)
print("Inverse of Matrix A is:", '\n', A_Inv)

A_Tran = np.transpose(A_Inv)
print("Transpose of Matrix A is: ", '\n', A_Tran)

Det_A = np. linalg.det(A)
print("Dterminant of Matrix A is: ", '\n', Det_A)

Cofactor_A = np.dot(A_Tran, Det_A)
print("Cofactors of Matrix A is: ", '\n', Cofactor_A)

Adjoint_A = np.transpose(Cofactor_A)
print("Ajoint of Matrix A is: ", '\n', Adjoint_A)
```

### Output:-
![image](https://github.com/user-attachments/assets/937a8f4a-b8f6-400d-b19d-08a4ab6ff702)
![image](https://github.com/user-attachments/assets/2bebbf2b-ac2e-4e72-8c1c-c2b9ae0f7418)
