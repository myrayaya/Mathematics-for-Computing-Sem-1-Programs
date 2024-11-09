## Program 2: Generate the matrix into echelon form and find its rank.

## Code:

```
import numpy as np

NR = int(input("Enter the no. of rows: "))
NC = int(input("Enter the no. of columns: "))

print("Enter the entries in a single line (separated by space): ")

entries = list(map(int, input().split()))

matrix = np.array(entries).reshape(NR, NC)
print('\n', "The matrix is as follows: ", '\n', matrix)

print('\n', "The Rank of the matrix: ", '\n', np.linalg.matrix_rank(matrix))
```

![image](https://github.com/user-attachments/assets/02ea5273-df28-4c87-aede-fdd4c723e72c)
