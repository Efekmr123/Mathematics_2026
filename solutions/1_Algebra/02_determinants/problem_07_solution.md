# Exercise 7 Solution: Using Properties Instead of Recomputing

## 1. Result
Given a $3 \times 3$ matrix $A$ with $\det(A) = -4$:
- $\det(2A) = -32$
- $\det(A^T) = -4$
- $\det(A^2) = 16$
- $\det(-A) = 4$

## 2. Main Steps

1. **Compute $\det(2A)$**:
   - **Property**: For an $n \times n$ matrix, scaling the entire matrix by scalar $c$ scales the determinant by $c^n$. Here $n = 3$ and $c = 2$.
   - **Calculation**: $\det(2A) = 2^3 \cdot \det(A) = 8 \cdot (-4) = -32$.

2. **Compute $\det(A^T)$**:
   - **Property**: The determinant of a matrix equals the determinant of its transpose.
   - **Calculation**: $\det(A^T) = \det(A) = -4$.

3. **Compute $\det(A^2)$**:
   - **Property**: The determinant of a product is the product of determinants, so $\det(A^k) = (\det(A))^k$.
   - **Calculation**: $\det(A^2) = (\det(A))^2 = (-4)^2 = 16$.

4. **Compute $\det(-A)$**:
   - **Property**: $-A = (-1)A$. For an $n \times n$ matrix with $n = 3$, $\det((-1)A) = (-1)^3 \cdot \det(A)$.
   - **Calculation**: $\det(-A) = (-1) \cdot (-4) = 4$.

## 3. Explanation
Determinant properties allow us to determine how matrix transformations (scaling, transposition, power, and negation) affect the scalar measure of volume scaling without recalculating individual entry values:
- Scaling a whole $n \times n$ matrix scales each of its $n$ rows, pulling out a factor of $c$ for each row ($c^n$).
- Transposition reflects entries across the main diagonal, leaving the alternating row products invariant.
- Negating an odd-dimensional matrix ($n=3$) flips the sign of the determinant because $(-1)^3 = -1$.

## 4. Verification
Applying the multiplicative rule $\det(A^2) = \det(A) \cdot \det(A) = (-4) \cdot (-4) = 16$ confirms the power rule $\quad \checkmark$.
