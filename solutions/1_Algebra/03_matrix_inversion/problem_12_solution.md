
# Exercise 12: Finding Inverses Without Starting from Scratch

## Given Matrix

We are given the inverse of a matrix A:

$$
A^{-1} =
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}
$$

Without calculating A itself, we need to determine:

1. $(3A)^{-1}$
2. $(A^T)^{-1}$
3. $(A^2)^{-1}$

We will use the properties of inverse matrices to calculate each expression directly.

## Step 1: Calculate the Inverse of 3A

For any invertible matrix A and any nonzero scalar k, the following property holds:

$$
(kA)^{-1} = \frac{1}{k}A^{-1}
$$

This is because:

$$
(kA)\left(\frac{1}{k}A^{-1}\right)
= AA^{-1} = I
$$

In our case:

$$
k = 3
$$

Therefore:

$$
(3A)^{-1} = \frac{1}{3}A^{-1}
$$

Substituting the given inverse matrix:

$$
(3A)^{-1} =
\frac{1}{3}
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}
$$

Multiplying each entry by 1/3:

$$
\boxed{
(3A)^{-1} =
\begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3}
\end{pmatrix}
}
$$

## Step 2: Calculate the Inverse of the Transpose of A

For any invertible matrix A, the inverse of its transpose satisfies:

$$
(A^T)^{-1} = (A^{-1})^T
$$

This property means that we can transpose the already known inverse matrix instead of finding A.

We are given:

$$
A^{-1} =
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}
$$

To transpose a matrix, we exchange its rows and columns.

Therefore:

$$
(A^{-1})^T =
\begin{pmatrix}
2 & -3 \\
-1 & 2
\end{pmatrix}
$$

Thus:

$$
\boxed{
(A^T)^{-1} =
\begin{pmatrix}
2 & -3 \\
-1 & 2
\end{pmatrix}
}
$$

We can justify the property using:

$$
AA^{-1} = I
$$

Taking the transpose of both sides:

$$
(AA^{-1})^T = I^T
$$

Using the transpose-of-a-product rule:

$$
(A^{-1})^T A^T = I
$$

Similarly, transposing $A^{-1}A=I$ gives:

$$
A^T(A^{-1})^T = I
$$

Therefore, $(A^{-1})^T$ is the inverse of $A^T$.

## Step 3: Calculate the Inverse of A Squared

For any invertible matrix A:

$$
(A^2)^{-1} = (A^{-1})^2
$$

This follows from the inverse-of-a-product property:

$$
(AB)^{-1} = B^{-1}A^{-1}
$$

Since:

$$
A^2 = AA
$$

we obtain:

$$
(A^2)^{-1} = (AA)^{-1}
$$

Therefore:

$$
(A^2)^{-1} = A^{-1}A^{-1}
$$

Now substitute the given inverse matrix:

$$
(A^2)^{-1} =
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}
$$

Multiplying rows by columns:

$$
(A^2)^{-1} =
\begin{pmatrix}
2(2)+(-1)(-3) & 2(-1)+(-1)(2) \\
(-3)(2)+2(-3) & (-3)(-1)+2(2)
\end{pmatrix}
$$

Simplifying each entry:

$$
(A^2)^{-1} =
\begin{pmatrix}
4+3 & -2-2 \\
-6-6 & 3+4
\end{pmatrix}
$$

Therefore:

$$
\boxed{
(A^2)^{-1} =
\begin{pmatrix}
7 & -4 \\
-12 & 7
\end{pmatrix}
}
$$

## Step 4: Explain Why We Do Not Need to Find A

All three expressions can be calculated directly from the given inverse matrix.

The important properties are:

### Scalar Multiplication

$$
(kA)^{-1} = \frac{1}{k}A^{-1}, \quad k \neq 0
$$

### Transpose

$$
(A^T)^{-1} = (A^{-1})^T
$$

### Matrix Powers

$$
(A^n)^{-1} = (A^{-1})^n
$$

for any positive integer n.

These properties allow us to find new inverse matrices without reconstructing the original matrix A.

## Conclusion

Using the properties of inverse matrices, we obtained the following results.

**1. Inverse of 3A:**

$$
\boxed{
(3A)^{-1} =
\begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3}
\end{pmatrix}
}
$$

**2. Inverse of the transpose of A:**

$$
\boxed{
(A^T)^{-1} =
\begin{pmatrix}
2 & -3 \\
-1 & 2
\end{pmatrix}
}
$$

**3. Inverse of A squared:**

$$
\boxed{
(A^2)^{-1} =
\begin{pmatrix}
7 & -4 \\
-12 & 7
\end{pmatrix}
}
$$

All three inverses were calculated directly from the given matrix $A^{-1}$, without finding A itself.

This demonstrates how inverse matrix properties can simplify calculations and avoid unnecessary operations.
