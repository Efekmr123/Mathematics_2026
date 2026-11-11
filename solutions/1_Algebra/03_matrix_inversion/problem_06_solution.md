
# Exercise 6: Solving a System Using the Inverse

## Given Matrices

We are given the linear system:

$$
Ax = b
$$

where:

$$
A =
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix},
\qquad
b =
\begin{pmatrix}
5 \\
7
\end{pmatrix}
$$

Our goal is to solve the system using the inverse matrix method:

$$
x = A^{-1}b
$$

Then, we will verify the solution by substituting it back into the original equation.

## Step 1: Calculate the Determinant of A

For a 2x2 matrix:

$$
A =
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

the determinant is:

$$
\det(A) = ad - bc
$$

For our matrix:

$$
\det(A) = (2)(3) - (1)(1)
$$

$$
\det(A) = 6 - 1 = 5
$$

Since the determinant is not zero, A is invertible.

## Step 2: Find the Inverse Matrix

The inverse formula for a 2x2 matrix is:

$$
A^{-1} =
\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
$$

Substituting our values:

$$
A^{-1} =
\frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix}
$$

Therefore:

$$
A^{-1} =
\begin{pmatrix}
\frac{3}{5} & -\frac{1}{5} \\
-\frac{1}{5} & \frac{2}{5}
\end{pmatrix}
$$

## Step 3: Calculate x = A^(-1)b

We use the formula:

$$
x = A^{-1}b
$$

Substituting the matrices:

$$
x =
\frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
5 \\
7
\end{pmatrix}
$$

Multiplying the matrix by the vector:

$$
x =
\frac{1}{5}
\begin{pmatrix}
3(5) + (-1)(7) \\
(-1)(5) + 2(7)
\end{pmatrix}
$$

Simplifying:

$$
x =
\frac{1}{5}
\begin{pmatrix}
15 - 7 \\
-5 + 14
\end{pmatrix}
$$

$$
x =
\frac{1}{5}
\begin{pmatrix}
8 \\
9
\end{pmatrix}
$$

Therefore:

$$
\boxed{
x =
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5}
\end{pmatrix}
}
$$

## Step 4: Verify the Solution

We substitute the calculated vector into the original equation:

$$
Ax = b
$$

Using our values:

$$
Ax =
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix}
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5}
\end{pmatrix}
$$

Multiplying:

$$
Ax =
\begin{pmatrix}
2(\frac{8}{5}) + 1(\frac{9}{5}) \\
1(\frac{8}{5}) + 3(\frac{9}{5})
\end{pmatrix}
$$

Simplifying:

$$
Ax =
\begin{pmatrix}
\frac{16}{5} + \frac{9}{5} \\
\frac{8}{5} + \frac{27}{5}
\end{pmatrix}
$$

$$
Ax =
\begin{pmatrix}
\frac{25}{5} \\
\frac{35}{5}
\end{pmatrix}
=
\begin{pmatrix}
5 \\
7
\end{pmatrix}
$$

This is exactly the original vector b.

Therefore:

$$
Ax = b
$$

The solution is verified.

## Conclusion

Using the inverse matrix method, we found:

$$
\boxed{
x =
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5}
\end{pmatrix}
}
$$

Equivalently:

$$
x_1 = \frac{8}{5},
\qquad
x_2 = \frac{9}{5}
$$

The result was verified by substituting it into the original system.

Since the determinant of A is nonzero, the system has a unique solution.
