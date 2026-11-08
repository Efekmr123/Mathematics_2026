# Exercise 8 Solution: Determinant of a Product and Inverse

## 1. Result
Given square matrices $A$ and $B$ with $\det(A) = 3$ and $\det(B) = -5$:
- $\det(AB) = -15$
- $\det(BA) = -15$
- $\det(A^{-1}B) = -\frac{5}{3}$
- Explanation for equality: Determinant of a product is scalar multiplication, which is commutative ($\det(A)\det(B) = \det(B)\det(A)$), even though matrix multiplication is non-commutative ($AB \neq BA$).

## 2. Main Steps

1. **Compute $\det(AB)$**:
   - **Property**: $\det(AB) = \det(A) \cdot \det(B)$
   - **Calculation**: $\det(AB) = (3) \cdot (-5) = -15$

2. **Compute $\det(BA)$**:
   - **Property**: $\det(BA) = \det(B) \cdot \det(A)$
   - **Calculation**: $\det(BA) = (-5) \cdot (3) = -15$

3. **Compute $\det(A^{-1}B)$**:
   - **Property**: $\det(A^{-1}) = \frac{1}{\det(A)}$ and $\det(A^{-1}B) = \det(A^{-1}) \cdot \det(B)$
   - **Calculation**: $\det(A^{-1}B) = \frac{1}{3} \cdot (-5) = -\frac{5}{3}$

## 3. Explanation
Matrix multiplication does not commute in general ($AB \neq BA$). However, the determinant operation converts matrix multiplication into ordinary real-number scalar multiplication. Since real multiplication is commutative:
$$\det(AB) = \det(A)\det(B) = \det(B)\det(A) = \det(BA)$$
This guarantees that $\det(AB)$ and $\det(BA)$ are always identical for any square matrices of matching size.

## 4. Verification
For $\det(A^{-1}B)$, using the property $\det(X^{-1}) = (\det(X))^{-1}$:
$$\det(A^{-1}B) = \frac{\det(B)}{\det(A)} = \frac{-5}{3} = -\frac{5}{3} \quad \checkmark$$
