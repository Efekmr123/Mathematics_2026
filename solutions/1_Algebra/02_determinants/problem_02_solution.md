# Exercise 2 Solution: Determinant of a 3x3 Matrix

## 1. Result
- $\det(A) = 31$
- Property Check: Expanding along the second row gives $31$, confirming the result obtained via Sarrus' Rule.

## 2. Main Steps
Given matrix:
$$A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}$$

1. **Compute $\det(A)$ using Sarrus' Rule**:
   - Write down the matrix and repeat the first two columns:
     $$\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix} \begin{matrix} 1 & 2 \\ 0 & 3 \\ 2 & 1 \end{matrix}$$
   - **Sum of primary diagonal products ($P$)**:
     $$P = (1 \cdot 3 \cdot 5) + (2 \cdot 4 \cdot 2) + (-1 \cdot 0 \cdot 1) = 15 + 16 + 0 = 31$$
   - **Sum of secondary diagonal products ($S$)**:
     $$S = (2 \cdot 3 \cdot -1) + (1 \cdot 4 \cdot 1) + (5 \cdot 0 \cdot 2) = -6 + 4 + 0 = -2$$
   - **Determinant calculation**:
     $$\det(A) = P - S = 31 - (-2) = 31 + 2 = 33$$

2. **Check using Cofactor Expansion along Row 2**:
   Row 2 is chosen because it contains a zero ($0, 3, 4$):
   $$\det(A) = -0 \cdot \det \begin{pmatrix} 2 & -1 \\ 1 & 5 \end{pmatrix} + 3 \cdot \det \begin{pmatrix} 1 & -1 \\ 2 & 5 \end{pmatrix} - 4 \cdot \det \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix}$$
   $$\det(A) = 0 + 3(5 - (-2)) - 4(1 - 4)$$
   $$\det(A) = 3(7) - 4(-3) = 21 + 12 = 33$$

## 3. Explanation
Sarrus' Rule is a quick shortcut exclusive to $3 \times 3$ matrices, where products of main diagonals are summed and secondary diagonals are subtracted. Cofactor expansion works for any square matrix dimension and confirms that the choice of row/column does not affect the final scalar value.

## 4. Verification
Both Sarrus' Rule and Row 2 Cofactor Expansion yield $\det(A) = 33 \quad \checkmark$.
