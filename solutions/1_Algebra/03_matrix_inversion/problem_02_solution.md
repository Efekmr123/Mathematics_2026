
# Exercise 2: Formula for a 2×2 Matrix

## Given Matrix

We are given the matrix:

$$
A = \begin{pmatrix}
3 & 2 \\
5 & 4
\end{pmatrix}
$$

We need to find the inverse of A using the formula for a 2×2 matrix and verify the result by multiplication.

## Step 1: Recall the Inverse Formula

For a 2×2 matrix:

$$
A = \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

the inverse is:

$$
A^{-1} = \frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
$$

provided that the determinant is not zero.

## Step 2: Calculate the Determinant

$$
\det(A) = ad-bc
$$

Substituting the values:

$$
\det(A) = (3)(4)-(2)(5)
$$

$$
\det(A) = 12-10 = 2
$$

Since the determinant is not zero, the inverse exists.

## Step 3: Calculate the Inverse

Using the formula:

$$
A^{-1} = \frac{1}{2}
\begin{pmatrix}
4 & -2 \\
-5 & 3
\end{pmatrix}
$$

Multiplying each element by 1/2:

$$
A^{-1} =
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2}
\end{pmatrix}
$$

## Step 4: Verify the Result

We check the result by calculating:

$$
AA^{-1} =
\begin{pmatrix}
3 & 2 \\
5 & 4
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2}
\end{pmatrix}
$$

Multiplying rows by columns:

$$
AA^{-1} =
\begin{pmatrix}
3(2)+2(-\frac{5}{2}) & 3(-1)+2(\frac{3}{2}) \\
5(2)+4(-\frac{5}{2}) & 5(-1)+4(\frac{3}{2})
\end{pmatrix}
$$

Simplifying:

$$
AA^{-1} =
\begin{pmatrix}
6-5 & -3+3 \\
10-10 & -5+6
\end{pmatrix}
$$

$$
AA^{-1} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
= I
$$

## Conclusion

The inverse of the given matrix is:

$$
\boxed{
A^{-1} =
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2}
\end{pmatrix}
}
$$

Since the product of A and its inverse equals the identity matrix, the result is verified.
