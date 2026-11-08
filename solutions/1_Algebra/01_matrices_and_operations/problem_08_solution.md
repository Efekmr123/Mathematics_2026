# Exercise 8 Solution: Row Operations and Their Reversibility

## 1. Result
- After Step 1 ($R_2 \leftarrow R_2 - 2R_1$):
  $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}$
- After Step 2 ($R_3 \leftarrow R_3 + R_1$):
  $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}$
- After Step 3 (Interchange $R_2$ and $R_3$):
  $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}$
- Reversing Operations:
  1. $R_2 \leftarrow R_2 + 2R_1$
  2. $R_3 \leftarrow R_3 - R_1$
  3. Interchange $R_2$ and $R_3$

## 2. Main Steps
Initial matrix:
$$A = \begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}$$

1. **Perform $R_2 \leftarrow R_2 - 2R_1$**:
   - $R_2 = (2, 4, 1) - 2(1, 2, -1) = (2-2, 4-4, 1-(-2)) = (0, 0, 3)$
   - Result: $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}$

2. **Perform $R_3 \leftarrow R_3 + R_1$**:
   - $R_3 = (-1, 1, 3) + (1, 2, -1) = (-1+1, 1+2, 3+(-1)) = (0, 3, 2)$
   - Result: $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}$

3. **Interchange $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$)**:
   - Swap second and third rows.
   - Result: $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}$

4. **Reversing Operations**:
   - To reverse subtracting $2R_1$ from $R_2$, add $2R_1$ back to $R_2$: $R_2 \leftarrow R_2 + 2R_1$.
   - To reverse adding $R_1$ to $R_3$, subtract $R_1$ from $R_3$: $R_3 \leftarrow R_3 - R_1$.
   - To reverse row swap $R_2 \leftrightarrow R_3$, perform the exact same swap again:
