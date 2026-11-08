# Exercise 10 Solution: Columns of a Matrix Product

## 1. Result
- $A b_1 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}$
- $A b_2 = \begin{pmatrix} 5 \\ 2 \end{pmatrix}$
- $AB = \begin{pmatrix} -1 & 5 \\ 2 & 2 \end{pmatrix}$
- Comparison: The columns of $AB$ are precisely the vectors $A b_1$ and $A b_2$, so $AB = \begin{pmatrix} A b_1 & A b_2 \end{pmatrix}$.

## 2. Main Steps
Given matrices:
$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}$$

Columns of $B$:
$$b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}, \quad b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}$$

1. **Compute $A b_1$**:
   $$A b_1 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(-1) + 0(3) \\ 0(1) + 1(-1) + 1(3) \end{pmatrix} = \begin{pmatrix} 1 - 2 + 0 \\ 0 - 1 + 3 \end{pmatrix} = \begin{pmatrix} -1 \\ 2 \end{pmatrix}$$

2. **Compute $A b_2$**:
   $$A b_2 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 1(2) + 2(0) + 0(1) \\ 0(2) + 1(0) + 1(1) \end{pmatrix} = \begin{pmatrix} 2 + 0 + 0 \\ 0 + 0 + 1 \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$$

3. **Compute full matrix product $AB$**:
   $$AB = \begin{pmatrix} (1)(1)+(2)(-1)+(0)(3) & (1)(2)+(2)(0)+(0)(1) \\ (0)(1)+(1)(-1)+(1)(3) & (0)(2)+(1)(0)+(1)(1) \end{pmatrix} = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}$$

## 3. Explanation
Matrix multiplication can be understood column-by-column. If $B = \begin{pmatrix} b_1 & b_2 & \dots & b_k \end{pmatrix}$, then the matrix product $AB$ is formed by multiplying $A$ by each column vector of $B$ individually:
$$AB = \begin{pmatrix} A b_1 & A b_2 & \dots & A b_k \end{pmatrix}$$

## 4. Verification
Comparing column 1 of $AB$ with $A b_1$: $\begin{pmatrix} -1 \\ 2 \end{pmatrix} = A b_1 \quad \checkmark$
Comparing column 2 of $AB$ with $A b_2$: $\begin{pmatrix} 2 \\ 1 \end{pmatrix} = A b_2 \quad \checkmark$
