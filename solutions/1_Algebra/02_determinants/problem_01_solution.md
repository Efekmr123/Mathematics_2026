# Exercise 1 Solution: Determinant of a 2x2 Matrix

## 1. Result
- $\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix} = 22$
- $\det \begin{pmatrix} 14 & 7 \\ 2 & 1 \end{pmatrix} = 0$
- Invertible matrix: **First matrix** is invertible ($\det \neq 0$), while the second is not ($\det = 0$).

## 2. Main Steps
The determinant of a $2 \times 2$ matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ is given by the formula $ad - bc$.

1. **Compute First Determinant**:
   $$\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix} = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22$$

2. **Compute Second Determinant**:
   $$\det \begin{pmatrix} 14 & 7 \\ 2 & 1 \end{pmatrix} = (14)(1) - (7)(2) = 14 - 14 = 0$$

3. **Check Invertibility**:
   - A matrix $M$ is invertible if and only if $\det(M) \neq 0$.
   - Since $22 \neq 0$, the first matrix is invertible.
   - Since $0 = 0$, the second matrix is singular (non-invertible).

## 3. Explanation
The determinant measures the scaling factor of the transformation induced by the matrix. A non-zero determinant means the transformation preserves dimensions, making it reversible (invertible). A zero determinant indicates that the space collapses to a lower dimension (e.g., a 2D area collapses into a line), making the transformation irreversible.

## 4. Verification
For the second matrix, observe that Row 1 is a scalar multiple of Row 2: $(14, 7) = 7 \cdot (2, 1)$. Linearly dependent rows always result in a zero determinant $\quad \checkmark$.
