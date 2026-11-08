# Exercise 2 Solution: Addition and Scalar Multiplication

## 1. Result
- $A + B = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$
- $A - B = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}$
- $3A - 2B = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}$

## 2. Main Steps
Given matrices:
$$A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \quad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}$$

1. **Compute $A + B$**:
   $$A + B = \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$$

2. **Compute $A - B$**:
   $$A - B = \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}$$

3. **Compute $3A - 2B$**:
   $$3A = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}, \quad 2B = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}$$
   $$3A - 2B = \begin{pmatrix} 3-8 & 6-(-4) \\ -3-0 & 9-10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}$$

## 3. Explanation
Matrix addition and subtraction require entry-by-entry operations: $(A \pm B)_{ij} = A_{ij} \pm B_{ij}$. This is defined if and only if both matrices have the same dimensions (same number of rows and columns). Otherwise, corresponding entries cannot be paired up.

## 4. Verification
- Dimension check: Both $A$ and $B$ are $2 \times 2$, so operations are well-defined.
- Double check entry $(1,2)$ of $3A - 2B$: $3(2) - 2(-2) = 6 + 4 = 10 \quad \checkmark$
