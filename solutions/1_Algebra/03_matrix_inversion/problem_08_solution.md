
# Exercise 8: Inverse of a Transformation

## Given Matrix

We are given the scaling matrix:

$$
S =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2}
\end{pmatrix}
$$

This matrix describes a scaling transformation of the plane.

Our goal is to find the inverse matrix $S^{-1}$, explain its geometric meaning, and verify the transformation using a simple vector.

## Step 1: Understand the Scaling Transformation

The matrix S acts on a vector:

$$
v =
\begin{pmatrix}
x \\
y
\end{pmatrix}
$$

Multiplying S by v gives:

$$
Sv =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2}
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
$$

Therefore:

$$
Sv =
\begin{pmatrix}
2x \\
\frac{y}{2}
\end{pmatrix}
$$

This transformation has two effects:

1. It stretches the plane horizontally by a factor of 2.
2. It compresses the plane vertically by a factor of 1/2.

## Step 2: Find the Inverse Matrix

Since S is a diagonal matrix with nonzero diagonal entries, its inverse is obtained by taking the reciprocal of each diagonal entry.

The original matrix is:

$$
S =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2}
\end{pmatrix}
$$

The reciprocal of 2 is 1/2, and the reciprocal of 1/2 is 2.

Therefore:

$$
\boxed{
S^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix}
}
$$

## Step 3: Explain the Geometric Meaning

The inverse transformation reverses the effects of the original scaling.

For a vector:

$$
w =
\begin{pmatrix}
x \\
y
\end{pmatrix}
$$

the inverse acts as:

$$
S^{-1}w =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
$$

Therefore:

$$
S^{-1}w =
\begin{pmatrix}
\frac{x}{2} \\
2y
\end{pmatrix}
$$

Geometrically, the inverse transformation:

1. Compresses the horizontal direction by a factor of 1/2.
2. Stretches the vertical direction by a factor of 2.

Thus, applying S and then its inverse returns every vector to its original position.

## Step 4: Verify Using a Simple Vector

Choose the vector:

$$
v =
\begin{pmatrix}
3 \\
4
\end{pmatrix}
$$

First, apply S:

$$
Sv =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2}
\end{pmatrix}
\begin{pmatrix}
3 \\
4
\end{pmatrix}
$$

$$
Sv =
\begin{pmatrix}
2(3)+0(4) \\
0(3)+\frac{1}{2}(4)
\end{pmatrix}
$$

Therefore:

$$
Sv =
\begin{pmatrix}
6 \\
2
\end{pmatrix}
$$

Now apply the inverse transformation:

$$
S^{-1}(Sv) =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix}
\begin{pmatrix}
6 \\
2
\end{pmatrix}
$$

$$
S^{-1}(Sv) =
\begin{pmatrix}
\frac{1}{2}(6)+0(2) \\
0(6)+2(2)
\end{pmatrix}
$$

$$
S^{-1}(Sv) =
\begin{pmatrix}
3 \\
4
\end{pmatrix}
$$

This is exactly the original vector v.

## Step 5: Verify by Matrix Multiplication

We can also verify that S and its inverse satisfy the definition of inverse matrices:

$$
SS^{-1} =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2}
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix}
$$

Multiplying:

$$
SS^{-1} =
\begin{pmatrix}
2(\frac{1}{2}) & 0 \\
0 & \frac{1}{2}(2)
\end{pmatrix}
$$

Therefore:

$$
SS^{-1} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
= I
$$

## Conclusion

The inverse of the scaling matrix is:

$$
\boxed{
S^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix}
}
$$

The original transformation stretches the x-direction and compresses the y-direction, while the inverse reverses these effects.

Using the vector:

$$
v =
\begin{pmatrix}
3 \\
4
\end{pmatrix}
$$

we verified that:

$$
S^{-1}(Sv) = v
$$

Therefore, the inverse transformation successfully restores the original vector.
