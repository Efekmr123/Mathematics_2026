# Exercise 6 Solution: Parameter and Invertibility

## 1. Result
- Determinant formula: $\det(A(t)) = t^2 - 2$
- Non-invertible values of $t$: $t = \sqrt{2}$ and $t = -\sqrt{2}$
- Explanation: A matrix is non-invertible if and only if its determinant equals zero.

## 2. Main Steps
Given parameterized matrix:
$$A(t) = \begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}$$

1. **Compute $\det(A(t))$**:
   Using the $2 \times 2$ determinant formula ($ad - bc$):
   $$\det(A(t)) = (t)(t) - (1)(2) = t^2 - 2$$

2. **Find values of $t$ for Non-Invertibility**:
   - A matrix $A(t)$ fails to be invertible (is singular) precisely when $\det(A(t)) = 0$.
   - Set the determinant to zero and solve for $t$:
     $$t^2 - 2 = 0 \implies t^2 = 2 \implies t = \pm\sqrt{2}$$

3. **Summary of Invertibility Conditions**:
   - Matrix is **non-invertible** for $t = \sqrt{2}$ and $t = -\sqrt{2}$.
   - Matrix is **invertible** for all $t \in \mathbb{R} \setminus \{-\sqrt{2}, \sqrt{2}\}$.

## 3. Explanation
The determinant provides a scalar measure of whether a linear map represented by $A(t)$ collapses space. When $t = \pm\sqrt{2}$, the rows $(t, 1)$ and $(2, t)$ become linearly dependent (one row becomes a scalar multiple of the other), which causes the determinant to vanish ($\det(A)=0$) and renders the matrix non-invertible.

## 4. Verification
Substitute $t = \sqrt{2}$ back into $A(t)$:
$$A(\sqrt{2}) = \begin{pmatrix} \sqrt{2} & 1 \\ 2 & \sqrt{2} \end{pmatrix}$$
Observe that Row 2 is $\sqrt{2}$ times Row 1: $(2, \sqrt{2}) = \sqrt{2} \cdot (\sqrt{2}, 1)$. Since the rows are dependent, $\det(A(\sqrt{2})) = 0$, confirming non-invertibility $\quad \checkmark$.
