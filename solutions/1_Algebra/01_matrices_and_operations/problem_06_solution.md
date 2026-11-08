# Exercise 6 Solution: Transpose

## 1. Result
- $A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}$
- $B^T = \begin{pmatrix} 1 & 1 \\ 0 & -1 \\ 2 & 3 \end{pmatrix}$
- $AB = \begin{pmatrix} 7 & 11 \\ 16 & 20 \end{pmatrix}$
- $(AB)^T = B^T A^T = \begin{pmatrix} 7 & 16 \\ 11 & 20 \end{pmatrix}$

## 2. Main Steps
Given matrices:
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}$$

1. **Find Transposes $A^T$ and $B^T$**:
   - Transpose swaps rows and columns: $(A^T)_{ij} = A_{ji}$.
   - $A_{2 \times 3} \implies A^T_{3 \times 2} = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}$
   - $B_{3 \times 2} \implies B^T_{2 \times 3} = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}$

2. **Compute $AB$**:
   $$AB = \begin{pmatrix} (1)(1)+(2)(2)+(3)(-1) & (1)(0)+(2)(1)+(3)(3) \\ (4)(1)+(5)(2)+(6)(-1) & (4)(0)+(5)(1)+(6)(3) \end{pmatrix} = \begin{pmatrix} 1+4-3 & 0+2+9 \\ 4+10-6 & 0+5+18 \end{pmatrix} = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}$$

3. **Compute $(AB)^T$**:
   $$(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$$

4. **Compute $B^T A^T$**:
   $$B^T A^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix} = \begin{pmatrix} 1+4-3 & 4+10-6 \\ 0+2+9 & 0+5+18 \end{pmatrix} = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$$

## 3. Explanation
The transpose of a product satisfies the property $(AB)^T = B^T A^T$. Transposing reverses the order of factors because the row-column dimensions shift, requiring the second matrix's transpose to come first to remain compatible.

## 4. Verification
Both $(AB)^T$ and $B^T A^T$ yield $\begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$, verifying the property $(AB)^T = B^T A^T \quad \checkmark$.
