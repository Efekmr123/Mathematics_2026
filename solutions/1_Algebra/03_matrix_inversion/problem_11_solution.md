
# Exercise 11: Parameter and Invertibility

## Given Matrix

We are given the matrix:

$$
A(t) =
\begin{pmatrix}
1 & t \\
t & 1
\end{pmatrix}
$$

Our goal is to determine all values of t for which the matrix is invertible, find a formula for its inverse, and explain what happens at the excluded values.

## Step 1: Calculate the Determinant

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
\det(A(t)) = (1)(1) - (t)(t)
$$

Therefore:

$$
\boxed{\det(A(t)) = 1-t^2}
$$

We can factor this expression:

$$
1-t^2 = (1-t)(1+t)
$$

## Step 2: Determine When the Matrix Is Invertible

A square matrix is invertible if and only if its determinant is nonzero.

Therefore, we require:

$$
1-t^2 \neq 0
$$

This means:

$$
t^2 \neq 1
$$

Hence:

$$
t \neq 1
\quad \text{and} \quad
t \neq -1
$$

Therefore, the matrix is invertible for:

$$
\boxed{t \in \mathbb{R}\setminus\{-1,1\}}
$$

## Step 3: Find the Inverse Matrix

The inverse formula for a 2x2 matrix is:

$$
A^{-1} =
\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
$$

Applying this formula to A(t):

$$
A(t)^{-1} =
\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix}
$$

Therefore:

$$
\boxed{
A(t)^{-1} =
\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix},
\quad t \neq \pm 1
}
$$

## Step 4: Verify the Inverse Formula

We verify the result by multiplying A(t) by its inverse:

$$
A(t)A(t)^{-1} =
\begin{pmatrix}
1 & t \\
t & 1
\end{pmatrix}
\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix}
$$

Multiplying the matrices:

$$
A(t)A(t)^{-1} =
\frac{1}{1-t^2}
\begin{pmatrix}
1-t^2 & -t+t \\
t-t & -t^2+1
\end{pmatrix}
$$

Simplifying:

$$
A(t)A(t)^{-1} =
\frac{1}{1-t^2}
\begin{pmatrix}
1-t^2 & 0 \\
0 & 1-t^2
\end{pmatrix}
$$

For t different from 1 and -1, we can divide by 1-t^2:

$$
A(t)A(t)^{-1} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
= I
$$

Thus, the inverse formula is verified.

## Step 5: Explain What Happens at t = 1

Substituting t = 1:

$$
A(1) =
\begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix}
$$

The determinant becomes:

$$
\det(A(1)) = 1-1^2=0
$$

The two rows are identical:

$$
R_1 = R_2
$$

Therefore, the rows are linearly dependent, and the matrix is singular.

The inverse formula also becomes undefined because its denominator is zero.

Hence:

$$
\boxed{A(1)^{-1} \text{ does not exist}}
$$

## Step 6: Explain What Happens at t = -1

Substituting t = -1:

$$
A(-1) =
\begin{pmatrix}
1 & -1 \\
-1 & 1
\end{pmatrix}
$$

The determinant becomes:

$$
\det(A(-1)) = 1-(-1)^2=0
$$

Here, the second row is the negative of the first row:

$$
R_2 = -R_1
$$

Therefore, the rows are linearly dependent, and the matrix is singular.

Again, the inverse formula is undefined because the denominator equals zero.

Hence:

$$
\boxed{A(-1)^{-1} \text{ does not exist}}
$$

## Conclusion

The matrix:

$$
A(t) =
\begin{pmatrix}
1 & t \\
t & 1
\end{pmatrix}
$$

is invertible for all real values of t except 1 and -1:

$$
\boxed{t \neq \pm 1}
$$

Its inverse is:

$$
\boxed{
A(t)^{-1} =
\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix}
}
$$

At t = 1 and t = -1, the determinant is zero, the rows become linearly dependent, and the inverse does not exist.

The formula is undefined at these excluded values because division by zero is not allowed.
