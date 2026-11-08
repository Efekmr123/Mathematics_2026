# Exercise 10 Solution: Detecting Dependence

## 1. Result
- $\det \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix} = 0$
- Row Dependence: Row 2 is twice Row 1 ($R_2 = 2R_1$).
- Invertibility: The matrix is **non-invertible** (singular) because linearly dependent rows collapse the determinant to zero.

## 2. Main Steps
Given matrix:
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix}$$

1. **Identify Row Dependence**:
   - Compare Row 1 ($R_1 = (1, 2, 3)$) and Row 2 ($R_2 = (2, 4, 6)$).
   - Observe that $R_2 = 2 \cdot R_1$.

2. **Apply Determinant Property**:
   - If a matrix has two rows that are linearly dependent (proportional to each other), its determinant is identically zero ($\det(A) = 0$).
   - Therefore, no full expansion is needed to conclude $\det(A) = 0$.

3. **Connect to Non-Invertibility**:
   - The invertibility criterion states that a matrix $A$ is invertible if and only if $\det(A) \neq 0$.
   - Since $\det(A) = 0$, $A$ is non-invertible.

## 3. Explanation
A zero determinant indicates that the rows of the matrix do not span a full-dimensional space ($3\text{D}$ space in this case). Because Row 2 contains no independent information beyond Row 1, the 3D volume spanned by the rows collapses into a 2D plane, yielding a volume (determinant) of zero.

## 4. Verification
Performing row operation $R_2 \leftarrow R_2 - 2R_1$:
$$A' = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \end{pmatrix}$$
Since $A'$ has an entire row of zeros ($R_2 = (0, 0, 0)$), expanding along Row 2 gives $\det(A) = 0 \quad \checkmark$.
