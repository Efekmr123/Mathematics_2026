# Exercise 14 Solution: A System of Equations and the Determinant

## 1. Result
Given the linear system $A x = b$ with $A = \begin{pmatrix} 1 & 2 \\ k & 4 \end{pmatrix}$:
- Determinant formula: $\det(A) = 4 - 2k$
- Exactly one solution: $k \neq 2$
- Remaining value ($k = 2$):
  - Infinitely many solutions example: $b = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$
  - No solution example: $b = \begin{pmatrix} 1 \\ 3 \end{pmatrix}$

## 2. Main Steps

1. **Find Condition for Unique Solution**:
   - A square system $Ax = b$ has a unique solution for every vector $b$ if and only if $\det(A) \neq 0$.
   - Compute $\det(A)$:
     $$\det(A) = (1)(4) - (2)(k) = 4 - 2k$$
   - Set $\det(A) \neq 0$:
     $$4 - 2k \neq 0 \implies 2k \neq 4 \implies k \neq 2$$

2. **Analyze Exceptional Case ($k = 2$)**:
   - Substitute $k = 2$ into matrix $A$:
     $$A = \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}$$
   - The augmented matrix $[A | b]$ is:
     $$\begin{pmatrix} 1 & 2 & | & b_1 \\ 2 & 4 & | & b_2 \end{pmatrix}$$
   - Perform row operation $R_2 \leftarrow R_2 - 2R_1$:
     $$\begin{pmatrix} 1 & 2 & | & b_1 \\ 0 & 0 & | & b_2 - 2b_1 \end{pmatrix}$$

3. **Construct Right-Hand Side Examples for $k = 2$**:
   - **Case 1: Infinitely Many Solutions**
     - Requires $b_2 - 2b_1 = 0$. Let $b_1 = 1$, then $b_2 = 2$.
     - Choice: $b = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$.
     - System becomes $x_1 + 2x_2 = 1$ and $0 = 0$ (consistent with infinitely many solutions).
   - **Case 2: No Solution**
     - Requires $b_2 - 2b_1 \neq 0$. Let $b_1 = 1$ and $b_2 = 3$, giving $3 - 2(1) = 1 \neq 0$.
     - Choice: $b = \begin{pmatrix} 1 \\ 3 \end{pmatrix}$.
     - System leads to the contradiction $0 = 1$ (inconsistent).

## 3. Explanation
The determinant determines the solvability state of a system:
- When $\det(A) \neq 0$, $A$ is non-singular and spans full dimension, making $x = A^{-1}b$ uniquely defined for any $b$.
- When $\det(A) = 0$, the transformation collapses space (here, 2D into a line). The system either has no solution if $b$ falls outside that line, or infinitely many solutions if $b$ lies within it.

## 4. Verification
For $k = 2$ and $b = \begin{pmatrix} 1 \\ 3 \end{pmatrix}$, Row 2 gives $2x_1 + 4x_2 = 3$. But 2 times Row 1 gives $2x_1 + 4x_2 = 2$. $2 \neq 3$ confirms no solution exists $\quad \checkmark$.
