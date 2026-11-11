
# Exercise 10: Inverse of a Diagonal Matrix

## Given Matrices

We are given two diagonal matrices:

$$
D =
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5
\end{pmatrix}
$$

and

$$
E =
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5
\end{pmatrix}
$$

Our goal is to determine which matrix is invertible without using Gauss-Jordan elimination, find its inverse, and verify the result by multiplication.

## Step 1: Determine the Invertibility of D

A diagonal matrix is invertible if and only if all its diagonal entries are nonzero.

The diagonal entries of D are:

$$
2,\quad -3,\quad 5
$$

All three entries are nonzero.

We can also confirm this using the determinant. For a diagonal matrix, the determinant is the product of its diagonal entries:

$$
\det(D) = 2(-3)(5)
$$

$$
\det(D) = -30
$$

Since:

$$
\det(D) \neq 0
$$

the matrix D is invertible.

## Step 2: Determine the Invertibility of E

The diagonal entries of E are:

$$
2,\quad 0,\quad 5
$$

The second diagonal entry is zero.

Calculating the determinant:

$$
\det(E) = 2(0)(5)
$$

$$
\det(E) = 0
$$

Since the determinant is zero, E is singular and has no inverse.

Therefore:

$$
\boxed{E^{-1} \text{ does not exist}}
$$

## Step 3: Find the Inverse of D

For an invertible diagonal matrix, the inverse is obtained by taking the reciprocal of each diagonal entry.

The original matrix is:

$$
D =
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5
\end{pmatrix}
$$

The reciprocals of the diagonal entries are:

$$
\frac{1}{2},\quad -\frac{1}{3},\quad \frac{1}{5}
$$

Therefore:

$$
\boxed{
D^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5}
\end{pmatrix}
}
$$

No Gauss-Jordan elimination is necessary because the diagonal structure allows us to calculate the inverse directly.

## Step 4: Verify the Result by Multiplication

We verify the inverse by calculating:

$$
DD^{-1} =
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5}
\end{pmatrix}
$$

Since both matrices are diagonal, the product is also diagonal.

Multiplying the corresponding diagonal entries:

$$
DD^{-1} =
\begin{pmatrix}
2(\frac{1}{2}) & 0 & 0 \\
0 & (-3)(-\frac{1}{3}) & 0 \\
0 & 0 & 5(\frac{1}{5})
\end{pmatrix}
$$

Simplifying:

$$
DD^{-1} =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$

Therefore:

$$
\boxed{DD^{-1} = I}
$$

The result is verified.

## Step 5: Explain the General Rule

For a diagonal matrix:

$$
M =
\begin{pmatrix}
d_1 & 0 & 0 \\
0 & d_2 & 0 \\
0 & 0 & d_3
\end{pmatrix}
$$

if every diagonal entry is nonzero, its inverse is:

$$
M^{-1} =
\begin{pmatrix}
\frac{1}{d_1} & 0 & 0 \\
0 & \frac{1}{d_2} & 0 \\
0 & 0 & \frac{1}{d_3}
\end{pmatrix}
$$

This works because multiplying each diagonal entry by its reciprocal gives 1.

If any diagonal entry is zero, the determinant is zero, and the matrix cannot be inverted.

## Conclusion

We determined that D is invertible because all its diagonal entries are nonzero:

$$
\det(D) = -30 \neq 0
$$

Its inverse is:

$$
\boxed{
D^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5}
\end{pmatrix}
}
$$

We verified that:

$$
DD^{-1} = I
$$

The matrix E is not invertible because:

$$
\det(E) = 0
$$

Thus, only D has an inverse.
