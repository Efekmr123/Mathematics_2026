# Exercise 7 Solution: Identity Matrix, Zero Matrix, and Powers

## 1. Result
- $AI = IA = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
- $A + 0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
- $A^2 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$
- $A^3 = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$
- General pattern: $A^n = \begin{pmatrix} 2^n & n \cdot 2^{n-1} \\ 0 & 2^n \end{pmatrix}$

## 2. Main Steps
Given:
$$A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$$

1. **Identity Matrix ($I$) and Zero Matrix ($0$) Operations**:
   $$I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \quad 0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$$
   - $AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
   - $IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
   - $A + 0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$

2. **Compute Powers of $A$**:
   - $A^2 = AA = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 4 & 2+2 \\ 0 & 4 \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$
   - $A^3 = A^2 A = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 8 & 4+8 \\ 0 & 8 \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$

## 3. Explanation
- **Identity matrix ($I$)** acts as the multiplicative neutral element ($AI = IA = A$).
- **Zero matrix ($0$)** acts as the additive neutral element ($A + 0 = A$).
- The main diagonal entries of $A^n$ double in powers of 2 ($2^n$), while the upper-right entry grows as $n \cdot 2^{n-1}$.

## 4. Verification
For $n = 3$:
- Diagonal: $2^3 = 8 \quad \checkmark$
- Upper-right entry: $3 \cdot 2^{3-1} = 3 \cdot 4 = 12 \quad \checkmark$
