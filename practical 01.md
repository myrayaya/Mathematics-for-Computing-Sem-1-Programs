# Mathematics for Computing Practical Programs:-

## Program 1: Create and transform vectors and matrices (the transpose vector (matrix) conjugate transpose of a vector (matrix))

## Code:

```
import numpy as np

NR = int(input("Enter the no. of rows: "))
NC = int(input("Enter the no. of columns: "))

print("Enter the entries in a single line (separated by space): ")

entries = list(map(int, input().split()))

matrix = np.array(entries).reshape(NR, NC)
print("Matrix is as follows: ", '\n', matrix)

print("Transpose of the matrix: ", '\n', np.transpose(matrix))
```

![image](https://github.com/user-attachments/assets/996ecc72-83e6-4000-8bcb-e4f48bb9e5e4)
