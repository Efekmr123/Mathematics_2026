# Exercise 5 Solution: Row Operations and Determinant

## 1. Result
- $\det(A) = -40$
- Row operations tracking:
  1. $R_2 \leftarrow R_2 - 2R_1$: Determinant does not change ($\det(A) = \det(A_1)$).
  2. $R_3 \leftarrow R_3 + R_1$: Determinant does not change ($\det(A_1) = \det(A_2)$).
  3. $R_3 \leftarrow R_3 + 2R_2$: Determinant does not change ($\det(A_2) = \det(U)$).

## 2. Main Steps
Given matrix:
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}$$

1. **Step 1: Eliminate $a_{21}$ ($R_2 \leftarrow R_2 - 2R_1$)**:
   - Operation: Subtracting a multiple of one row from another does not alter the determinant.
   $$A_1 = \begin{pmatrix} 1 & 2 & 3 \\ 2 - 2(1) & 1 - 2(2) & 0 - 2(3) \\ -1 & 4 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 & 4 & 2 \end{pmatrix}$$
   $$\det(A) = \det(A_1)$$

2. **Step 2: Eliminate $a_{31}$ ($R_3 \leftarrow R_3 + R_1$)**:
   - Operation: Adding a multiple of one row to another does not alter the determinant.
   $$A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 + 1 & 4 + 2 & 2 + 3 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}$$
   $$\det(A) = \det(A_2)$$

3. **Step 3: Eliminate $a_{32}$ ($R_3 \leftarrow R_3 + 2R_2$)**:
   - Operation: Adding 2 times Row 2 to Row 3 does not alter the determinant.
   $$U = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 + 2(-3) & 5 + 2(-6) \end{pmatrix} = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{pmatrix}$$
   $$\det(A) = \det(U)$$

4. **Compute determinant of upper triangular matrix $U$**:
   $$\det(A) = \det(U) = (1) \cdot (-3) \cdot (-7) = 21$$

## 3. Explanation
Elementary row operations affect the determinant as follows:
- **Adding/subtracting a scalar multiple of one row to another ($R_i \leftarrow R_i + c R_j$)**: Leaves the determinant completely unchanged.
- **Swapping two rows ($R_i \leftrightarrow R_j$)**: Multiplies the determinant by $-1$.
- **Scaling a row ($R_i \leftarrow c R_i$)**: Multiplies the determinant by $c$.

Since we only used row replacement operations, $\det(A)$ remained identical to $\det(U)$ throughout all transformation steps.

## 4. Verification
Expanding $A$ directly via Sarrus' rule
