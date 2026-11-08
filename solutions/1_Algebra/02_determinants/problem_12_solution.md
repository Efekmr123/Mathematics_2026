# Exercise 12 Solution: A Parameter Revealed by a Row Operation

## 1. Result
- Determinant formula: $\det(A(t)) = 6 - 2t$
- Non-invertible value: $t = 3$
- Special Row Behavior: When $t = 3$, Row 2 becomes an exact scalar multiple of Row 1 ($R_2 = 2R_1$).

## 2. Main Steps
Given parameterized matrix:
$$A(t) = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & t \\ 0 & 1 & 1 \end{pmatrix}$$

1. **Perform Recommended Row Operation ($R_2 \leftarrow R_2 - 2R_1$)**:
   - Subtract 2 times Row 1 from Row 2 to simplify the matrix:
     $$A'(t) = \begin{pmatrix} 1 & 2 & 3 \\ 2 - 2(1) & 4 - 2(2) & t - 2(3) \\ 0 & 1 & 1 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & t - 6 \\ 0 & 1 & 1 \end{pmatrix}$$

2. **Compute $\det(A(t))$ using $A'(t)$**:
   - Expand along Column 1:
     $$\det(A(t)) = 1 \cdot \det \begin{pmatrix} 0 & t - 6 \\ 1 & 1 \end{pmatrix} - 0 + 0$$
     $$\det(A(t)) = (0 \cdot 1) - (1 \cdot (t - 6)) = -(t - 6) = 6 - t$$

3. **Solve for Non-Invertibility**:
   - $A(t)$ is non-invertible when $\det(A(t)) = 0$:
     $$6 - t = 0 \implies t = 6$$

4. **Analyze Special Row Behavior**:
   - For $t = 6$, substituting back into the original matrix yields:
     $$A(6) = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 1 \end{pmatrix}$$
   - Comparing $R_1 = (1, 2, 3)$ and $R_2 = (2, 4, 6)$ shows that $R_2 = 2R_1$. The first two rows are directly proportional.

## 3. Explanation
Performing the target row operation $R_2 \leftarrow R_2 - 2R_1$ isolated the parameter $t$ into a single entry ($(t-6)$) while revealing that $t=6$ eliminates the entire second row. This linear dependence between $R_1$ and $R_2$ collapses the row space dimension, forcing the determinant to zero.

## 4. Verification
Expanding $A(6)$ along Row 2:
$$\det(A(6)) = -2(2 - 3) + 4(1 - 0) - 6(1 - 0) = 2 + 4 - 6 = 0 \quad \checkmark$$
