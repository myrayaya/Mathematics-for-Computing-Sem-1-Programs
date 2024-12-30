```
import numpy as np

#Define the vectors
v1 = np.array([1, 2, 3])
v2 = np.array([2, 4, 6])
v3 = np.array([3, 6, 9])
A = np.column_stack((v1, v2, v3))
U, S, Vt = np.linalg.svd(A)
rank = np.sum(S > 1e-10)
num_vectors = A.shape[1]

if rank < num_vectors:
    print("The vectors are linearly dependent")
else:
    print("The vectors are linearly independent")

c1 = int(input("Enter a coefficient for v1: "))
c2 = int(input("Enter a coefficient for v2: "))
c3 = int(input("Enter a coefficient for v3: "))
linear_combination = c1 * v1 + c2 * v2 + c3 * v3

print("Linear Combination: ", linear_combination)
if np.all(linear_combination == 0):
    print("The linear combination equals the zero vectors")
else:
    print("The linear combination does not equal the zero vector")
```
