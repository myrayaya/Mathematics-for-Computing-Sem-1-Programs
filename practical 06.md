```
import numpy as np

def diagonalizable(A):
    
    # Compute eigenvalues and eigenvectors
    eigenvalues, eigenvectors = np.linalg.eig(A)
    
    # Check if the matrix of eigenvectors has full rank (this is the condition for diagonalizability)
    if np.linalg.matrix_rank(eigenvectors) == A.shape[0]:
        # If rank is equal to the size of the matrix, the matrix is diagonalizable
        D = np.diag(eigenvalues)  # Diagonal matrix D
        P = eigenvectors  # Matrix of eigenvectors
        return True, D, P
    else:
        # Not diagonalizable if the rank is less than the size of the matrix
        return False, None, None

def cayley_hamilton(A):
    
   
    eigenvalues, eigenvectors = np.linalg.eig(A)
    
    
    p_A = np.poly(A) 
    
    
    poly_A = np.polyval(p_A, A)
    
    
    return np.allclose(poly_A, np.zeros_like(A))

A = np.array([[4, -2],
              [1,  1]])


diagonalizable, D, P = diagonalizable(A)

if diagonalizable:
    print(f"The matrix is diagonalizable. The diagonal matrix D is:\n{D}")
    print(f"The matrix of eigenvectors P is:\n{P}")
else:
    print("The matrix is not diagonalizable.")

# Verify the Cayley-Hamilton theorem
if cayley_hamilton(A):
    print("The Cayley-Hamilton theorem is satisfied.")
else:
    print("The Cayley-Hamilton theorem is not satisfied.")
```
