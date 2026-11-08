# Exercise 12 Solution: Symmetric Matrices and A^T A

## 1. Result
- $A^T = \begin{pmatrix} 1 & 3 \\ 2 & 4 \end{pmatrix}$
- $A^T A = \begin{pmatrix} 10 & 14 \\ 14 & 20 \end{pmatrix}$
- Is $A^T A$ symmetric? **Yes**, $A^T A$ is symmetric.
- General proof: $(A^T A)^T = A^T (A^T)^T = A^T A$.

## 2. Main Steps
Given matrix:
$$A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}$$

1. **Find Transpose $A^T$**:
   $$A^T = \begin{pmatrix} 1 & 3 \\ 2 & 4 \end{pmatrix}$$

2. **Compute $A^T A$**:
   $$A^T A = \begin{pmatrix} 1 & 3 \\ 2 & 4 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} = \begin{pmatrix} 10 & 14 \\ 14 & 20 \end{pmatrix}$$

3. **Check Symmetry of $A^T A$**:
   $$(A^T A)^T = \begin{pmatrix} 10 & 14 \\ 14 & 20 \end{pmatrix}^T = \begin{pmatrix} 10 & 14 \\ 14 & 20 \end{pmatrix} = A^T A$$

4. **General Algebraic Proof**:
   $$(A^T A)^T = A^T (A^T)^T = A^T A$$

## 3. Explanation
A matrix $M$ is symmetric if $M^T = M$. For any matrix $A$, the product $A^T A$ is always square and symmetric.

## 4. Verification
Off-diagonal elements of $A^T A$: $(A^T A)_{12} = 14$ and $(A^T A)_{21} = 14$. They are equal.
