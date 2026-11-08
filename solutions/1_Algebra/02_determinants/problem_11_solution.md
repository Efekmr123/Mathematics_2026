# Exercise 11 Solution: Shortening the Calculation with Row Operations

## 1. Result
- $\det \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix} = 1$
- Row operations used: $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$.
- Impact on determinant: Neither operation changes the determinant value.

## 2. Main Steps
Given matrix:
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix}$$

1. **Perform Row Operations to Create Zeros in Column 1**:
   - Operation 1: $R_2 \leftarrow R_2 - R_1$ (does not change determinant)
     $$A_1 = \begin{pmatrix} 1 & 2 & 3 \\ 1-1 & 3-2 & 4-3 \\ 1 & 4 & 6 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 4 & 6 \end{pmatrix}$$
   - Operation 2: $R_3 \leftarrow R_3 - R_1$ (does not change determinant)
     $$A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1-1 & 4-2 & 6-3 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}$$

2. **Compute Determinant by Cofactor Expansion along Column 1**:
   $$\det(A) = \det(A_2) = 1 \cdot \det \begin{pmatrix} 1 & 1 \\ 2 & 3 \end{pmatrix} - 0 + 0$$
   $$\det(A) = (1)(3) - (1)(2) = 3 - 2 = 1$$

## 3. Explanation
Instead of calculating the $3 \times 3$ determinant directly via lengthy multiplications, we can use row replacements of the form $R_i \leftarrow R_i + c R_j$. These operations keep the determinant invariant while creating leading zeros, simplifying the determinant calculation to a basic $2 \times 2$ matrix expansion.

## 4. Verification
Applying one additional row operation $R_3 \leftarrow R_3 - 2R_2$ to $A_2$:
$$U = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$$
$U$ is upper triangular, so its determinant is the product of its main diagonal elements: $\det(A) = (1)(1)(1) = 1 \quad \checkmark$.
