```
import numpy as np

# Taking input for coefficient matrix A
print("Enter the dimensions of the coefficient matrix A:-") 
NR = int(input("Enter the no. of rows: "))
NC = int(input("Enter the no. of columns: "))

# Taking input for the elements of matrix A
print("Enter the elements of the coefficient matrix A in a single line (separated by spaces): ")
Coeff_Entries = list(map(int, input().split()))
Coeff_Matrix = np.array(Coeff_Entries).reshape(NR, NC)
print("Coefficient Matrix A is as follows: ", '\n',Coeff_Matrix)

# Taking input for column matrix B
print("Enter the elements of the column matrix B in a single line (separated by spaces): ")
Column_Entries = list(map(float, input().split()))
Column_Matrix = np.array(Column_Entries).reshape(NR, 1)
print("Column Matrix B is as follows: ", '\n', Column_Matrix)

#Solutions of homogenous system of equations using Gauss Jordan Method
Coeff_Matrix_Inv = np.linalg.inv(Coeff_Matrix)
Solutions = np.matmul(Coeff_Matrix_Inv, Column_Matrix)
print("Solutions of the system of equations using Gauss Jordan Method: ", '\n', Solutions)
```

