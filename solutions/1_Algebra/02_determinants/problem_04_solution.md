# Exercise 4 Solution: Determinant of a Triangular Matrix

## 1. Result
- $\det \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix} = -42$
- Rule: The determinant of an upper or lower triangular matrix is equal to the product of its main diagonal entries.

## 2. Main Steps
Given upper triangular matrix:
$$A = \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}$$

1. **Apply the Triangular Matrix Rule**:
   $$\det(A) = a_{11} \cdot a_{22} \cdot a_{33}$$
   $$\det(A) = (2) \cdot (-3) \cdot (7) = -42$$

2. **Verify via Cofactor Expansion (Column 1)**:
   Expanding along the first column (which contains mostly zeros):
   $$\det(A) = 2 \cdot \det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} - 0 + 0$$
   $$\det(A) = 2 \cdot [(-3)(7) - (5)(0)] = 2 \cdot (-21) = -42$$

## 3. Explanation
For an arbitrary triangular matrix $T$ (where all entries below or above the main diagonal are zero), expanding along the row/column with the most zeros recursively cancels out all off-diagonal products. Thus, the determinant collapses strictly to the product of the diagonal elements:
$$\det(T) = \prod_{i=1}^n t_{ii}$$

## 4. Verification
Direct expansion along Column 1 yields $-42$, matching the main diagonal product $(2)(-3)(7) = -42 \quad \checkmark$.
