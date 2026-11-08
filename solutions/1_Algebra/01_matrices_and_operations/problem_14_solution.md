# Exercise 14 Solution: Trace of a Matrix Product

## 1. Result
- $\text{Tr}(AB) = 19$
- $\text{Tr}(BA) = 19$
- Property verified: $\text{Tr}(AB) = \text{Tr}(BA)$

## 2. Main Steps
Given matrices:
$$A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}, \quad B = \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix}$$

1. **Compute $AB$ and its Trace**:
   $$AB = \begin{pmatrix} (1)(5)+(2)(7) & (1)(6)+(2)(8) \\ (3)(5)+(4)(7) & (3)(6)+(4)(8) \end{pmatrix} = \begin{pmatrix} 5+14 & 6+16 \\ 15+28 & 18+32 \end{pmatrix} = \begin{pmatrix} 19 & 22 \\ 43 & 50 \end{pmatrix}$$
   $$\text{Tr}(AB) = 19 + 50 = 69$$

2. **Compute $BA$ and its Trace**:
   $$BA = \begin{pmatrix} (5)(1)+(6)(3) & (5)(2)+(6)(4) \\ (7)(1)+(8)(3) & (7)(2)+(8)(4) \end{pmatrix} = \begin{pmatrix} 5+18 & 10+24 \\ 7+24 & 14+32 \end{pmatrix} = \begin{pmatrix} 23 & 34 \\ 31 & 46 \end{pmatrix}$$
   $$\text{Tr}(BA) = 23 + 46 = 69$$

3. **General Algebraic Proof**:
   For matrices $A_{m \times n}$ and $B_{n \times m}$:
   $$\text{Tr}(AB) = \sum_{i=1}^m (AB)_{ii} = \sum_{i=1}^m \sum_{j=1}^n A_{ij} B_{ji}$$
   $$\text{Tr}(BA) = \sum_{j=1}^n (BA)_{jj} = \sum_{j=1}^n \sum_{i=1}^m B_{ji} A_{ij} = \sum_{i=1}^m \sum_{j=1}^n A_{ij} B_{ji}$$
   Therefore, $\text{Tr}(AB) = \text{Tr}(BA)$ always holds.

## 3. Explanation
The trace of a square matrix is the sum of its main diagonal elements. Even though matrix multiplication is non-commutative ($AB \neq BA$), the trace operation is cyclic: $\text{Tr}(AB) = \text{Tr}(BA)$.

## 4. Verification
Both $\text{Tr}(AB) = 69$ and $\text{Tr}(BA) = 69$ yield identical scalar values $\quad \checkmark$.
