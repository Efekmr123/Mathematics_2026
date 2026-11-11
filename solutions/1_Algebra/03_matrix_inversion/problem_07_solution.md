
# Exercise 7: Inverse of a Product

## Given Matrices

We are given the matrices:

$$
A =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix},
\qquad
B =
\begin{pmatrix}
2 & 0 \\
0 & 3
\end{pmatrix}
$$

Our goal is to calculate $(AB)^{-1}$ and $B^{-1}A^{-1}$, verify that they are equal, and explain why the order of multiplication is reversed.

## Step 1: Calculate AB

First, we multiply A and B:

$$
AB =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3
\end{pmatrix}
$$

Multiplying rows by columns:

$$
AB =
\begin{pmatrix}
1(2)+1(0) & 1(0)+1(3) \\
0(2)+1(0) & 0(0)+1(3)
\end{pmatrix}
$$

Therefore:

$$
AB =
\begin{pmatrix}
2 & 3 \\
0 & 3
\end{pmatrix}
$$

## Step 2: Calculate the Inverse of AB

For a 2x2 matrix:

$$
M =
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

the inverse formula is:

$$
M^{-1} =
\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
$$

First, calculate the determinant:

$$
\det(AB) = (2)(3)-(3)(0)=6
$$

Since the determinant is nonzero, the inverse exists.

Applying the formula:

$$
(AB)^{-1} =
\frac{1}{6}
\begin{pmatrix}
3 & -3 \\
0 & 2
\end{pmatrix}
$$

Therefore:

$$
\boxed{
(AB)^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3}
\end{pmatrix}
}
$$

## Step 3: Calculate the Inverse of A

We have:

$$
A =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

Its determinant is:

$$
\det(A) = (1)(1)-(1)(0)=1
$$

Using the inverse formula:

$$
A^{-1} =
\frac{1}{1}
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
$$

Thus:

$$
A^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
$$

## Step 4: Calculate the Inverse of B

We have:

$$
B =
\begin{pmatrix}
2 & 0 \\
0 & 3
\end{pmatrix}
$$

Since B is a diagonal matrix with nonzero diagonal entries, its inverse is obtained by taking the reciprocals of those entries.

Therefore:

$$
B^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3}
\end{pmatrix}
$$

## Step 5: Calculate B^(-1)A^(-1)

Now multiply the two inverse matrices in reversed order:

$$
B^{-1}A^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3}
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
$$

Multiplying rows by columns:

$$
B^{-1}A^{-1} =
\begin{pmatrix}
\frac{1}{2}(1)+0(0) &
\frac{1}{2}(-1)+0(1) \\
0(1)+\frac{1}{3}(0) &
0(-1)+\frac{1}{3}(1)
\end{pmatrix}
$$

Therefore:

$$
\boxed{
B^{-1}A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3}
\end{pmatrix}
}
$$

## Step 6: Compare the Results

From Step 2:

$$
(AB)^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3}
\end{pmatrix}
$$

From Step 5:

$$
B^{-1}A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3}
\end{pmatrix}
$$

Both matrices are identical.

Therefore:

$$
\boxed{(AB)^{-1}=B^{-1}A^{-1}}
$$

## Step 7: Explain the Reversed Order

The order of multiplication is reversed because matrix multiplication is generally not commutative.

To undo the product AB, we must apply the inverse operations in the opposite order.

We can verify this algebraically:

$$
(AB)(B^{-1}A^{-1})
=
A(BB^{-1})A^{-1}
$$

Since:

$$
BB^{-1}=I
$$

we obtain:

$$
AIA^{-1}=AA^{-1}=I
$$

Similarly:

$$
(B^{-1}A^{-1})(AB)
=
B^{-1}(A^{-1}A)B
=
B^{-1}IB
=
I
$$

Thus, $B^{-1}A^{-1}$ is the inverse of AB.

The rightmost matrix acts first on a column vector. Therefore, AB applies B first and then A. To reverse the transformation, we undo A first using $A^{-1}$, followed by B using $B^{-1}$.

This is why the inverse of a product has the factors in reversed order.

## Conclusion

We calculated the inverse of AB directly and by multiplying the individual inverses.

Both methods gave:

$$
\boxed{
(AB)^{-1}=B^{-1}A^{-1}
=
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3}
\end{pmatrix}
}
$$

The result confirms the inverse-of-a-product property and demonstrates why the order of operations must be reversed.
