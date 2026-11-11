
# Exercise 1: Definition of the Inverse

## Given Matrices

We are given the following matrices:

$$
A = \begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}
\qquad
B = \begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix}
$$

We need to determine whether $B = A^{-1}$ without using the inverse formula.

According to the definition, two square matrices are inverses of each other if:

$$
AB = BA = I
$$

where $I$ is the identity matrix.

## Step 1: Calculate AB

$$
AB =
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix}
$$

Multiplying rows by columns:

$$
AB =
\begin{pmatrix}
2(1)+1(-1) & 2(-1)+1(2) \\
1(1)+1(-1) & 1(-1)+1(2)
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
= I
$$

## Step 2: Calculate BA

$$
BA =
\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}
$$

Multiplying rows by columns:

$$
BA =
\begin{pmatrix}
1(2)+(-1)(1) & 1(1)+(-1)(1) \\
(-1)(2)+2(1) & (-1)(1)+2(1)
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
= I
$$

## Conclusion

Since both matrix products are equal to the identity matrix:

$$
AB = BA = I
$$

we can conclude that:

$$
\boxed{B = A^{-1}}
$$

Therefore, B is the inverse of A.

This result follows directly from the definition of an inverse matrix, without using any inverse formula.
