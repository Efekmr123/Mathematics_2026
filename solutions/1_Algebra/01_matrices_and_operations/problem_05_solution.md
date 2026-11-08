# Exercise 5 Solution: Matrix Times Vector

## 1. Result
- $Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$
- Linear combination of columns: $Ax = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$

## 2. Main Steps
Given:
$$A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}, \quad x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$$

1. **Standard Matrix Multiplication**:
   $$Ax = \begin{pmatrix} (2)(4) + (-1)(2) \\ (1)(4) + (3)(2) \end{pmatrix} = \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$$

2. **Express as a Linear Combination of Columns**:
   Let the columns of $A$ be $a_1 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$ and $a_2 = \begin{pmatrix} -1 \\ 3 \end{pmatrix}$.
   The vector components of $x$ are $x_1 = 4$ and $x_2 = 2$.
   $$Ax = x_1 a_1 + x_2 a_2 = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$$

## 3. Explanation
Multiplying a matrix $A$ by a column vector $x$ yields a new vector that is equal to a linear combination of the columns of $A$, weighted by the corresponding entries of $x$.

## 4. Verification
Both calculation methods (row-by-column product and column linear combination) yield identical results: $\begin{pmatrix} 6 \\ 10 \end{pmatrix} \quad \checkmark$.
