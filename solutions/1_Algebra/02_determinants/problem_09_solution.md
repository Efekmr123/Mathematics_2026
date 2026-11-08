# Exercise 9 Solution: Area and the Determinant

## 1. Result
- Area of the parallelogram spanned by $u$ and $v$: $\text{Area} = 11$
- Determinant with ordered vectors $(u, v)$: $\det \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix} = 11$
- Determinant with reversed vectors $(v, u)$: $\det \begin{pmatrix} 1 & 4 \\ 3 & 1 \end{pmatrix} = -11$
- **What changes**: The sign of the determinant reverses (flips from $+11$ to $-11$) due to row interchange.
- **What does not change**: The geometric area remains unchanged ($\text{Area} = |\det| = 11$).

## 2. Main Steps
Given vectors:
$$u = \begin{pmatrix} 3 \\ 1 \end{pmatrix}, \quad v = \begin{pmatrix} 1 \\ 4 \end{pmatrix}$$

1. **Compute Determinant with Matrix $[u \quad v]^T$**:
   - Form matrix $M_1$ with rows $u^T$ and $v^T$:
     $$M_1 = \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix}$$
   - Compute determinant:
     $$\det(M_1) = (3)(4) - (1)(1) = 12 - 1 = 11$$

2. **Compute Area**:
   $$\text{Area} = |\det(M_1)| = |11| = 11$$

3. **Reverse Vector Order $[v \quad u]^T$ and Recompute**:
   - Form matrix $M_2$ with rows $v^T$ and $u^T$:
     $$M_2 = \begin{pmatrix} 1 & 4 \\ 3 & 1 \end{pmatrix}$$
   - Compute determinant:
     $$\det(M_2) = (1)(1) - (4)(3) = 1 - 12 = -11$$
   - Compute Area with reversed order:
     $$\text{Area} = |\det(M_2)| = |-11| = 11$$

## 3. Explanation
The determinant of a $2 \times 2$ matrix formed by two 2D vectors measures the **signed area** of the parallelogram spanned by them:
- **Sign**: Indicates the orientation (handedness) of the vector pair. Ordering $(u, v)$ forms a counterclockwise orientation (positive), while $(v, u)$ forms a clockwise orientation (negative).
- **Absolute Value**: Represents the actual physical area, which is geometric and independent of orientation.

## 4. Verification
Using the geometric vector cross-product / determinant magnitude formula:
$$\text{Area} = |u_x v_y - u_y v_x| = |(3)(4) - (1)(1)| = |11| = 11 \quad \checkmark$$
