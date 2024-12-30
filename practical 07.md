```
import sympy as sp

x, y, z = sp.symbols('x y z')

f = x**2 + y**2 + z**2

A = sp.Matrix([x * y, y * z, z * x])

gradient_f = sp.Matrix([sp.diff(f, var) for var in [x, y, z]])

divergence_A = sp.diff(A[0], x) + sp.diff(A[1], y) + sp.diff(A[2], z)

curl_A = sp.Matrix([
    sp.diff(A[2], y) - sp.diff(A[1], z),
    sp.diff(A[0], z) - sp.diff(A[2], x),
    sp.diff(A[1], x) - sp.diff(A[0], y)
])

print(f"Gradient of the scalar field f(x, y, z):\n{gradient_f}")
print(f"\nDivergence of the vector field A(x, y, z):\n{divergence_A}")
print(f"\nCurl of the vector field A(x, y, z):\n{curl_A}")
```
