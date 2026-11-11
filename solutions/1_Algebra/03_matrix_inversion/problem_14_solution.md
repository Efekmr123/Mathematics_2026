
# Exercise 14: A Matrix That Is Its Own Inverse

## Given Condition

We are given a square matrix A satisfying:

$$
A^2 = I
$$

where I is the identity matrix.

Our goals are to:

1. Prove that $A^{-1}=A$.
2. Give a 2x2 example of such a matrix that is neither I nor -I.
3. Verify the example by matrix multiplication.

## Step 1: Recall the Definition of an Inverse Matrix

For a square matrix A, its inverse $A^{-1}$ satisfies:

$$
AA^{-1}=I
$$

and

$$
A^{-1}A=I
$$

In other words, multiplying a matrix by its inverse in either order gives the identity matrix.

## Step 2: Prove That A Is Its Own Inverse

We are given:

$$
A^2=I
$$

By the definition of matrix powers:

$$
A^2=AA
$$

Therefore:

$$
AA=I
$$

The first copy of A multiplied by the second copy gives the identity matrix.

Since both factors are A, this also satisfies the inverse condition in the opposite order.

Thus, A itself is a two-sided inverse of A.

By the definition and uniqueness of the inverse matrix:

$$
\boxed{A^{-1}=A}
$$

Therefore, every square matrix satisfying $A^2=I$ is invertible and is equal to its own inverse.

Such a matrix is called an involutory matrix.

## Step 3: Choose a 2x2 Example

Consider the matrix:

$$
A=
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
$$

The 2x2 identity matrix is:

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$

Its negative is:

$$
-I=
\begin{pmatrix}
-1 & 0 \\
0 & -1
\end{pmatrix}
$$

Our chosen matrix is different from both:

$$
A\neq I
$$

and

$$
A\neq -I
$$

Therefore, it satisfies the requirement that the example must not be I or -I.

## Step 4: Verify That A Squared Equals I

We calculate:

$$
A^2=AA
$$

Substituting our matrix:

$$
A^2=
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
$$

Multiplying rows by columns:

$$
A^2=
\begin{pmatrix}
1(1)+0(0) & 1(0)+0(-1) \\
0(1)+(-1)(0) & 0(0)+(-1)(-1)
\end{pmatrix}
$$

Simplifying:

$$
A^2=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$

Therefore:

$$
\boxed{A^2=I}
$$

This verifies that our example satisfies the given condition.

## Step 5: Verify the Inverse Directly

The matrix is diagonal, with diagonal entries 1 and -1.

For an invertible diagonal matrix, its inverse is obtained by taking the reciprocal of each diagonal entry.

Since:

$$
\frac{1}{1}=1
$$

and

$$
\frac{1}{-1}=-1
$$

we obtain:

$$
A^{-1}=
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
$$

Comparing this with the original matrix:

$$
A=
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
$$

we confirm:

$$
\boxed{A^{-1}=A}
$$

## Step 6: Geometric Interpretation

Our example matrix represents a reflection across the x-axis.

For a vector:

$$
v=
\begin{pmatrix}
x \\
y
\end{pmatrix}
$$

applying A gives:

$$
Av=
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
$$

Therefore:

$$
Av=
\begin{pmatrix}
x \\
-y
\end{pmatrix}
$$

The x-coordinate stays the same, while the y-coordinate changes sign.

Applying A again:

$$
A(Av)=
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
\begin{pmatrix}
x \\
-y
\end{pmatrix}
$$

This gives:

$$
A(Av)=
\begin{pmatrix}
x \\
y
\end{pmatrix}
=v
$$

Thus, reflecting a vector across the x-axis twice returns it to its original position.

This provides a geometric explanation of why:

$$
A^2=I
$$

and consequently:

$$
A^{-1}=A
$$

## Conclusion

We proved that if a square matrix satisfies:

$$
A^2=I
$$

then:

$$
\boxed{A^{-1}=A}
$$

A valid 2x2 example is:

$$
\boxed{
A=
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
}
$$

This matrix is neither I nor -I.

By direct multiplication, we verified:

$$
A^2=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
=I
$$

Therefore, A is its own inverse.

This example also represents a reflection across the x-axis, which returns every vector to its original position when applied twice.
