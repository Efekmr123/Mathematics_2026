# Exercise 3 Solution: Swapping Two Rows

## 1. Result
- $\det(A) = -5$
- Predicted $\det(B)$: Since matrix $B$ is obtained by swapping two rows of $A$, its determinant should change sign: $\det(B) = -\det(A) = 5$.
- Calculation of $\det(B)$: $\det(B) = 5$.
- Verification: The prediction matches the direct calculation ($\det(B) = -\det(A)$).

## 2. Main Steps
Given matrices:
$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}$$

1. **Compute $\det(A)$**:
   Using cofactor expansion along Row 1:
   $$\det(A) = 1 \cdot \det \begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} - 2 \cdot \det \begin{pmatrix} 0 & 1 \\ 2 & 1 \end{pmatrix} + 0$$
   $$\det(A) = 1(3 - 1) - 2(0 - 2) = 1(2) - 2(-2) = 2 + 4 = 6$$

2. **Form Matrix $B$ and Predict $\det(B)$**:
   - $B$ is formed by interchanging Row 1 and Row 2 of matrix $A$ ($R_1 \leftrightarrow R_2$).
   - Property: Swapping any two rows of a square matrix multiplies its determinant by $-1$.
   - Prediction: $\det(B) = -1 \cdot \det(A) = -6$.

3. **Verify Prediction by Computing $\det(B)$ directly**:
   Using cofactor expansion along Row 1 of $B$:
   $$\det(B) = 0 - 3 \cdot \det \begin{pmatrix} 1 & 0 \\ 2 & 1 \end{pmatrix} + 1 \cdot \det \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix}$$
   $$\det(B) = -3(1 - 0) + 1(1 - 4) = -3(1) + 1(-3) = -3 - 3 = -6$$

## 3. Explanation
Interchanging two rows (or two columns) of a matrix reverses the orientation of the vector basis spanned by its rows. Algebraically, this swaps two inputs in the alternating multilinear form that defines the determinant, resulting in a sign change ($\det(B) = -\det(A)$).

## 4. Verification
Calculated $\det(B) = -6$ perfectly matches predicted $-\det(A) = -6 \quad \checkmark$.
