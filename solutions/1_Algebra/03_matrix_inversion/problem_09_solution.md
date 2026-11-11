
# Exercise 9: Matrix Equation

## Given Matrices

We are given the matrices:

$$
A =
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix},
\qquad
B =
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix}
$$

Our goal is to solve the matrix equation:

$$
AX = B
$$

We need to determine which side to multiply by the inverse of A and verify the result by calculating AX.

## Step 1: Determine the Correct Multiplication Side

We start with:

$$
AX = B
$$

Since A is multiplied on the left side of X, we must multiply both sides of the equation by $A^{-1}$ from the left.

$$
A^{-1}AX = A^{-1}B
$$

Using the inverse property:

$$
A^{-1}A = I
$$

we obtain:

$$
IX = A^{-1}B
$$

Therefore:

$$
\boxed{X = A^{-1}B}
$$

We cannot simply multiply by $A^{-1}$ from the right because matrix multiplication is generally not commutative.

## Step 2: Calculate the Inverse of A

We have:

$$
A =
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}
$$

For a 2x2 matrix, the inverse formula is:

$$
A^{-1} =
\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
$$

First, calculate the determinant:

$$
\det(A) = (1)(1)-(2)(0)=1
$$

Since the determinant is nonzero, A is invertible.

Applying the inverse formula:

$$
A^{-1} =
\frac{1}{1}
\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix}
$$

Therefore:

$$
\boxed{
A^{-1} =
\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix}
}
$$

## Step 3: Calculate X = A^(-1)B

Using:

$$
X = A^{-1}B
$$

Substitute the matrices:

$$
X =
\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix}
$$

Multiplying rows by columns:

$$
X =
\begin{pmatrix}
1(3)+(-2)(2) & 1(1)+(-2)(4) \\
0(3)+1(2) & 0(1)+1(4)
\end{pmatrix}
$$

Simplifying:

$$
X =
\begin{pmatrix}
3-4 & 1-8 \\
0+2 & 0+4
\end{pmatrix}
$$

Therefore:

$$
\boxed{
X =
\begin{pmatrix}
-1 & -7 \\
2 & 4
\end{pmatrix}
}
$$

## Step 4: Verify the Result by Calculating AX

We substitute the calculated matrix X into the original equation:

$$
AX = B
$$

Using our matrices:

$$
AX =
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4
\end{pmatrix}
$$

Multiplying rows by columns:

$$
AX =
\begin{pmatrix}
1(-1)+2(2) & 1(-7)+2(4) \\
0(-1)+1(2) & 0(-7)+1(4)
\end{pmatrix}
$$

Simplifying:

$$
AX =
\begin{pmatrix}
-1+4 & -7+8 \\
0+2 & 0+4
\end{pmatrix}
$$

Therefore:

$$
AX =
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix}
$$

This is exactly the original matrix B.

Thus:

$$
\boxed{AX = B}
$$

The solution is verified.

## Step 5: Explain Why Matrix Order Matters

Matrix multiplication is generally not commutative:

$$
AB \neq BA
$$

Therefore, the order of multiplication must be preserved when solving matrix equations.

In our equation:

$$
AX = B
$$

the matrix A appears to the left of X.

To eliminate A, we multiply both sides by $A^{-1}$ from the left:

$$
A^{-1}(AX) = A^{-1}B
$$

This gives:

$$
X = A^{-1}B
$$

Multiplying from the right would not cancel A because $AXA^{-1}$ is not generally equal to X.

## Conclusion

We solved the matrix equation:

$$
AX = B
$$

and obtained:

$$
\boxed{
X =
\begin{pmatrix}
-1 & -7 \\
2 & 4
\end{pmatrix}
}
$$

We verified the solution by calculating:

$$
AX =
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix}
= B
$$

Therefore, the solution is correct.

This exercise demonstrates the importance of multiplying by the inverse matrix on the correct side when solving matrix equations.
