# Exercise 9 Solution: Composing Transformations

## 1. Result
- $RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$
- $SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$
- Comparison: $RSx \neq SRx$ because matrix multiplication is non-commutative. Geometrically, scaling first and then rotating produces a different final vector than rotating first and then scaling.

## 2. Main Steps
Given transformation matrices and vector:
$$S = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}, \quad R = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}, \quad x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$$

1. **Compute $RSx$ (Scale then Rotate)**:
   - First, apply $S$ to $x$:
     $$Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix}$$
   - Next, apply $R$ to $(Sx)$:
     $$R(Sx) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$$

2. **Compute $SRx$ (Rotate then Scale)**:
   - First, apply $R$ to $x$:
     $$Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \end{pmatrix}$$
   - Next, apply $S$ to $(Rx)$:
     $$S(Rx) = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$$

## 3. Explanation
Matrix-vector multiplication $Ax$ represents a geometric transformation. The product $RSx = (RS)x$ represents the composition of transformations where $S$ is applied first, followed by $R$. Since non-uniform scaling alters lengths along specific axes, rotating the scaled vector changes which coordinates get expanded, making the order of operations crucial ($RS \neq SR$).

## 4. Verification
- Direct matrix product $RS = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 0 & -1 \\ 2 & 0 \end{pmatrix}$
- $(RS)x = \begin{pmatrix} 0 & -1 \\ 2 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix} \quad \checkmark$
