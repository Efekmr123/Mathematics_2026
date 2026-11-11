
# Exercise 13: Undoing a Composite Transformation

## Given Matrices

We are given two transformation matrices:

$$
S =
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
$$

and

$$
H =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

The composite transformation is defined as:

$$
T = HS
$$

Our goal is to:

1. Calculate the composite transformation T.
2. Find the inverse of T directly.
3. Find the inverse using the formula $T^{-1}=S^{-1}H^{-1}$.
4. Compare the results.
5. Explain why reversing the inverse multiplication order is necessary.

## Step 1: Calculate the Composite Transformation T

We are given:

$$
T = HS
$$

Substituting the matrices:

$$
T =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
$$

Multiplying rows by columns:

$$
T =
\begin{pmatrix}
1(2)+1(0) & 1(0)+1(1) \\
0(2)+1(0) & 0(0)+1(1)
\end{pmatrix}
$$

Therefore:

$$
\boxed{
T =
\begin{pmatrix}
2 & 1 \\
0 & 1
\end{pmatrix}
}
$$

## Step 2: Find the Inverse of T Directly

For a 2x2 matrix:

$$
A =
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

the inverse formula is:

$$
A^{-1} =
\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
$$

First, calculate the determinant of T:

$$
\det(T) = (2)(1)-(1)(0)
$$

$$
\det(T) = 2
$$

Since the determinant is nonzero, T is invertible.

Applying the formula:

$$
T^{-1} =
\frac{1}{2}
\begin{pmatrix}
1 & -1 \\
0 & 2
\end{pmatrix}
$$

Therefore:

$$
\boxed{
T^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1
\end{pmatrix}
}
$$

## Step 3: Calculate the Inverse of S

We have:

$$
S =
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
$$

Since S is a diagonal matrix with nonzero diagonal entries, we can find its inverse by taking the reciprocals of the diagonal entries.

Therefore:

$$
\boxed{
S^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1
\end{pmatrix}
}
$$

## Step 4: Calculate the Inverse of H

We have:

$$
H =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

First, calculate its determinant:

$$
\det(H) = (1)(1)-(1)(0)=1
$$

Applying the inverse formula:

$$
H^{-1} =
\frac{1}{1}
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
$$

Therefore:

$$
\boxed{
H^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
}
$$

## Step 5: Find the Inverse Using the Product Rule

For two invertible matrices:

$$
(AB)^{-1} = B^{-1}A^{-1}
$$

Since:

$$
T = HS
$$

we have:

$$
T^{-1} = (HS)^{-1} = S^{-1}H^{-1}
$$

Substituting the inverse matrices:

$$
S^{-1}H^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
$$

Multiplying rows by columns:

$$
S^{-1}H^{-1} =
\begin{pmatrix}
\frac{1}{2}(1)+0(0) &
\frac{1}{2}(-1)+0(1) \\
0(1)+1(0) &
0(-1)+1(1)
\end{pmatrix}
$$

Simplifying:

$$
\boxed{
S^{-1}H^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1
\end{pmatrix}
}
$$

This is exactly the same matrix obtained by directly inverting T.

Therefore:

$$
\boxed{T^{-1}=S^{-1}H^{-1}}
$$

## Step 6: Check What Happens with the Wrong Order

Now consider multiplying the inverses in the opposite order:

$$
H^{-1}S^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1
\end{pmatrix}
$$

Multiplying:

$$
H^{-1}S^{-1} =
\begin{pmatrix}
1(\frac{1}{2})+(-1)(0) &
1(0)+(-1)(1) \\
0(\frac{1}{2})+1(0) &
0(0)+1(1)
\end{pmatrix}
$$

Therefore:

$$
\boxed{
H^{-1}S^{-1} =
\begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1
\end{pmatrix}
}
$$

However, the correct inverse is:

$$
T^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1
\end{pmatrix}
$$

Clearly:

$$
\boxed{H^{-1}S^{-1}\neq T^{-1}}
$$

We can also verify the incorrect order by multiplying T with $H^{-1}S^{-1}$:

$$
T(H^{-1}S^{-1}) =
\begin{pmatrix}
2 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1
\end{pmatrix}
$$

$$
T(H^{-1}S^{-1}) =
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
$$

Since this is not the identity matrix, $H^{-1}S^{-1}$ is not the inverse of T.

## Step 7: Explain the Geometric Meaning

The matrix S represents a horizontal scaling transformation:

$$
S
\begin{pmatrix}
x \\
y
\end{pmatrix}
=
\begin{pmatrix}
2x \\
y
\end{pmatrix}
$$

It stretches the x-coordinate by a factor of 2.

The matrix H represents a horizontal shear transformation:

$$
H
\begin{pmatrix}
x \\
y
\end{pmatrix}
=
\begin{pmatrix}
x+y \\
y
\end{pmatrix}
$$

Since:

$$
T = HS
$$

the transformation S is applied first, followed by H.

Therefore:

$$
T
\begin{pmatrix}
x \\
y
\end{pmatrix}
=
\begin{pmatrix}
2x+y \\
y
\end{pmatrix}
$$

To undo this transformation, we must reverse the operations:

1. First undo the shear using $H^{-1}$.
2. Then undo the scaling using $S^{-1}$.

Thus, the inverse transformation is:

$$
T^{-1} = S^{-1}H^{-1}
$$

The rightmost matrix acts first on a column vector, so this product applies $H^{-1}$ before $S^{-1}$.

## Step 8: Verify the Correct Inverse

Finally, we verify that:

$$
TT^{-1}=I
$$

Substituting:

$$
TT^{-1} =
\begin{pmatrix}
2 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1
\end{pmatrix}
$$

Multiplying:

$$
TT^{-1} =
\begin{pmatrix}
2(\frac{1}{2})+1(0) &
2(-\frac{1}{2})+1(1) \\
0(\frac{1}{2})+1(0) &
0(-\frac{1}{2})+1(1)
\end{pmatrix}
$$

Simplifying:

$$
TT^{-1} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$

Therefore:

$$
\boxed{TT^{-1}=I}
$$

The inverse is verified.

## Conclusion

The composite transformation is:

$$
\boxed{
T = HS =
\begin{pmatrix}
2 & 1 \\
0 & 1
\end{pmatrix}
}
$$

Both methods give the same inverse:

$$
\boxed{
T^{-1}=S^{-1}H^{-1}=
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1
\end{pmatrix}
}
$$

However, multiplying the inverse matrices in the wrong order gives:

$$
H^{-1}S^{-1} =
\begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1
\end{pmatrix}
$$

which is not equal to $T^{-1}$.

This demonstrates that the inverse of a composite transformation must undo the individual transformations in reverse order.

The final result was verified by showing that:

$$
TT^{-1}=I
$$
