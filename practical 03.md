## Practical - 3: Solve a system of linear equations using Gauss Elimination Method. 

Code / Input: 
```
import numpy as np

print("Enter the dimension of coefficients Matrix A! ")
NR = int(input("Enter the no. of rows: "))
NC = int(input("Enter the no. of columns: "))

print("Enter the elements of coefficients Matrix A in a single line (seperated by space: ")
Coeff_Entries = list(map(float, input().split()))
Coeff_Matrix = np.array(Coeff_Entries).reshape(NR, NC)
print("Coefficient Matrix A is as follows: ", '\n', Coeff_Matrix ,'\n')

print("Enter the elements of column Matrix B in a single line (seperated by spaces): ")
Column_Entries = list(map(float, input().split()))
Column_Matrix = np.array(Column_Entries).reshape(NR, 1)
print("Column Matrix B is as follows: ", '\n', Column_Matrix, '\n')

Solutions = np.linalg.solve(Coeff_Matrix, Column_Matrix)
print("Solutions of the system of equations using Gauss Elimination Method", '\n')
print(Solutions)
```

Output:-
