# Exercise 13 Solution: Nilpotent Matrices

## 1. Result
- $A^2 = \begin{pmatrix} 0 & 0 & 2 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}$
- $A^3 = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix} = 0_{3 \times 3}$
- Index of nilpotency: $k = 3$

## 2. Main Steps
Given strictly upper-triangular matrix:
$$A = \begin{pmatrix} 0 & 1 & 2 \\ 0 & 0 & 2 \\ 0 & 0 & 0 \end{pmatrix}$$

1. **Compute $A^2$**:
   $$A^2 = \begin{pmatrix} 0 & 1 & 2 \\ 0 & 0 & 2 \\ 0 & 0 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 & 2 \\ 0 & 0 & 2 \\ 0 & 0 & 0 \end{pmatrix} = \begin{pmatrix} 0 & 0 & 2 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}$$

2. **Compute $A^3$**:
   $$A^3 = A^2 A = \begin{pmatrix} 0 & 0 & 2 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 & 2 \\ 0 & 0 & 2 \\ 0 & 0 & 0 \end{pmatrix} = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}$$

3. **Determine Nilpotency Index**:
   Since $A^3 = 0$ and $A^2 \neq 0$, the index of nilpotency is $k = 3$.

## 3. Explanation
A square matrix $A$ is called **nilpotent** if there exists a positive integer $k$ such that $A^k = 0$. The smallest such integer $k$ is the index of nilpotency. Strictly upper (or lower) triangular matrices with zeros on the main diagonal are always nilpotent.

## 4. Verification
- $A \neq 0$, $A^2 \neq 0$, $A^3 = 0$.
- The power exponent $k = 3$ matches the matrix dimension $n = 3$, which aligns with the property that an $n \times n$ strictly upper triangular matrix satisfies $A^n = 0$.
