# Exercise 15 Solution: Cramer's Rule for a 2x2 System

## 1. Result
Given system:
$$\begin{aligned} 2x + 3y &= 8 \\ 4x - y &= 2 \end{aligned}$$
- Coefficient determinant: $\det(A) = -14$
- Modified determinants: $\det(A_x) = -14$, $\det(A_y) = -28$
- Solution via Cramer's Rule: $x = 1, \quad y = 2$

## 2. Main Steps

1. **Form Coefficient Matrix $A$ and Compute $\det(A)$**:
   $$A = \begin{pmatrix} 2 & 3 \\ 4 & -1 \end{pmatrix}$$
   $$\det(A) = (2)(-1) - (3)(4) = -2 - 12 = -14$$
   Since $\det(A) = -14 \neq 0$, Cramer's Rule applies uniquely.

2. **Form Modified Matrix $A_x$ and Compute $\det(A_x)$**:
   - Replace Column 1 with column vector $b = \begin{pmatrix} 8 \\ 2 \end{pmatrix}$:
     $$A_x = \begin{pmatrix} 8 & 3 \\ 2 & -1 \end{pmatrix}$$
   - Compute determinant:
     $$\det(A_x) = (8)(-1) - (3)(2) = -8 - 6 = -14$$

3. **Form Modified Matrix $A_y$ and Compute $\det(A_y)$**:
   - Replace Column 2 with column vector $b = \begin{pmatrix} 8 \\ 2 \end{pmatrix}$:
     $$A_y = \begin{pmatrix} 2 & 8 \\ 4 & 2 \end{pmatrix}$$
   - Compute determinant:
     $$\det(A_y) = (2)(2) - (8)(4) = 4 - 32 = -28$$

4. **Calculate Solutions $(x, y)$**:
   $$x = \frac{\det(A_x)}{\det(A)} = \frac{-14}{-14} = 1$$
   $$y = \frac{\det(A_y)}{\det(A)} = \frac{-28}{-14} = 2$$

## 3. Explanation
Cramer's Rule isolates each unknown variable in a linear system by scaling the main determinant $\det(A)$ with a determinant $\det(A_i)$ obtained by replacing the $i$-th column of $A$ with the constants vector $b$. It provides an explicit algebraic formula for solutions when $\det(A) \neq 0$.

## 4. Verification
Substitute $x = 1$ and $y = 2$ back into the original equations:
- Equation 1: $2(1) + 3(2) = 2 + 6 = 8 \quad \checkmark$
- Equation 2: $4(1) - (2) = 4 - 2 = 2 \quad \checkmark$
