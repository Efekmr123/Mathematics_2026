# Exercise 4 Solution: Matrix Multiplication and Noncommutativity

## 1. Result
- $AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}$
- $BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}$
- Is $AB = BA$? **No**, $AB \neq BA$.

## 2. Main Steps
Given matrices:
$$A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}$$

1. **Compute $AB$**:
   $$AB = \begin{pmatrix} (1)(2) + (2)(3) & (1)(0) + (2)(1) \\ (0)(2) + (1)(3) & (0)(0) + (1)(1) \end{pmatrix} = \begin{pmatrix} 2+6 & 0+2 \\ 0+3 & 0+1 \end{pmatrix} = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}$$

2. **Compute $BA$**:
   $$BA = \begin{pmatrix} (2)(1) + (0)(0) & (2)(2) + (0)(1) \\ (3)(1) + (1)(0) & (3)(2) + (1)(1) \end{pmatrix} = \begin{pmatrix} 2+0 & 4+0 \\ 3+0 & 6+1 \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}$$

3. **Compare**:
   $$\begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} \neq \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix} \implies AB \neq BA$$

## 3. Explanation
Noncommutativity of matrix multiplication means that changing the order of matrices in a product generally changes the result ($AB \neq BA$). Unlike real numbers where $ab = ba$, matrix multiplication depends strictly on the order of factors because rows of the first matrix interact with columns of the second.

## 4. Verification
- Check entry $(1,1)$ of $AB$: $1 \cdot 2 + 2 \cdot 3 = 8 \quad \checkmark$
- Check entry $(1,1)$ of $BA$: $2 \cdot 1 + 0 \cdot 0 = 2 \quad \checkmark$
- Since $8 \neq 2$, $AB$ cannot equal $BA$.
