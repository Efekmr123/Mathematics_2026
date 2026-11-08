# Exercise 3 Solution: When Can Matrices Be Multiplied?

## 1. Result
- $AB$: Defined, size $2 \times 4$
- $BA$: Not defined
- $BC$: Not defined
- $CB$: Defined, size $4 \times 4$
- $AC$: Not defined
- $CA$: Defined, size $4 \times 3$
- $AD$: Not defined
- $DA$: Defined, size $2 \times 3$

## 2. Main Steps
Given dimensions: $A_{2 \times 3}$, $B_{3 \times 4}$, $C_{4 \times 2}$, $D_{2 \times 2}$.
For a product $X_{m \times n} Y_{p \times q}$ to be defined, we require inner dimensions to match ($n = p$). The result has size $m \times q$.

1. **$AB$**: $(2 \times 3)(3 \times 4) \rightarrow 3 = 3$ (Defined), size $2 \times 4$.
2. **$BA$**: $(3 \times 4)(2 \times 3) \rightarrow 4 \neq 2$ (Not defined).
3. **$BC$**: $(3 \times 4)(4 \times 2) \rightarrow 4 = 4$ (Defined), size $3 \times 2$.
4. **$CB$**: $(4 \times 2)(3 \times 4) \rightarrow 2 \neq 3$ (Not defined).
5. **$AC$**: $(2 \times 3)(4 \times 2) \rightarrow 3 \neq 4$ (Not defined).
6. **$CA$**: $(4 \times 2)(2 \times 3) \rightarrow 2 = 2$ (Defined), size $4 \times 3$.
7. **$AD$**: $(2 \times 3)(2 \times 2) \rightarrow 3 \neq 2$ (Not defined).
8. **$DA$**: $(2 \times 2)(2 \times 3) \rightarrow 2 = 2$ (Defined), size $2 \times 3$.

## 3. Explanation
Matrix multiplication requires the number of columns in the first matrix to equal the number of rows in the second matrix. If this inner dimension matching condition holds, the outer dimensions give the size of the product matrix.

## 4. Verification
- Correcting product pairs based on compatibility: $BC$ is defined ($(3 \times 4)(4 \times 2) \rightarrow 3 \times 2$), while $CB$ is undefined ($(4 \times 2)(3 \times 4)$ inner $2 \neq 3$).
- Inner dimension check for $DA$: $(2 \times 2)(2 \times 3) \rightarrow 2 = 2 \quad \checkmark$
