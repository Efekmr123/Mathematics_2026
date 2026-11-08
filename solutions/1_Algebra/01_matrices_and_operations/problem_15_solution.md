# Exercise 15 Solution: Idempotent Matrices

## 1. Result
- $A^2 = \begin{pmatrix} 4 & -6 \\ 2 & -3 \end{pmatrix} = A$
- Is $A$ idempotent? **Yes**, $A^2 = A$.
- Eigenvalues: $\lambda = 1$ and $\lambda = 0$.

## 2. Main Steps
Given matrix:
$$A = \begin{pmatrix} 4 & -6 \\ 2 & -3 \end{pmatrix}$$

1. **Compute $A^2$**:
   $$A^2 = \begin{pmatrix} 4 & -6 \\ 2 & -3 \end{pmatrix} \begin{pmatrix} 4 & -6 \\ 2 & -3 \end{pmatrix} = \begin{pmatrix} (4)(4) + (-6)(2) & (4)(-6) + (-6)(-3) \\ (2)(4) + (-3)(2) & (2)(-6) + (-3)(-3) \end{pmatrix}$$
   $$A^2 = \begin{pmatrix} 16 - 12 & -24 + 18 \\ 8 - 6 & -12 + 9 \end{pmatrix} = \begin{pmatrix} 4 & -6 \\ 2 & -3 \end{pmatrix} = A$$

2. **Find Eigenvalues**:
   - For an idempotent matrix, $A v = \lambda v \implies A^2 v = \lambda^2 v$.
   - Since $A^2 = A$, we have $\lambda^2 v = \lambda v \implies \lambda^2 - \lambda = 0 \implies \lambda(\lambda - 1) = 0$.
   - Therefore, the only possible eigenvalues of any idempotent matrix are $\lambda = 0$ or $\lambda = 1$.

## 3. Explanation
A square matrix $A$ is called **idempotent** if multiplying it by itself yields the original matrix ($A^2 = A$). Geometrically, idempotent matrices represent projection operators onto a subspace. Applying a projection twice has the same effect as applying it once.

## 4. Verification
- $A^2 = A$ holds entry-by-entry $\quad \checkmark$.
- Trace of $A$: $\text{Tr}(A) = 4 + (-3) = 1$.
- Since the trace equals the sum of eigenvalues and $\lambda \in \{0, 1\}$, the eigenvalues are indeed $\lambda_1 = 1$ and $\lambda_2 = 0 \quad \checkmark$.
