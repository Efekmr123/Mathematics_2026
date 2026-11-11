
# Exercise 5: A 3×3 Matrix

## Given Matrix

We are given the matrix:

$$
A =
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}
$$

Our goal is to find the inverse of A using the Gauss-Jordan elimination method and verify the result by matrix multiplication.

## Step 1: Construct the Augmented Matrix

We begin with the augmented matrix [A | I]:

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
1 & 0 & 1 & 0 & 0 & 1
\end{array}
\right]
$$

We perform elementary row operations to transform the left side into the identity matrix.

## Step 2: Eliminate the First Entry in Row 3

Apply:

$$
R_3 \rightarrow R_3 - R_1
$$

We obtain:

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & -1 & 1 & -1 & 0 & 1
\end{array}
\right]
$$

## Step 3: Eliminate the Second Entry in Row 3

Apply:

$$
R_3 \rightarrow R_3 + R_2
$$

We obtain:

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 2 & -1 & 1 & 1
\end{array}
\right]
$$

## Step 4: Make the Third Pivot Equal to 1

Divide the third row by 2:

$$
R_3 \rightarrow \frac{1}{2}R_3
$$

Therefore:

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{array}
\right]
$$

## Step 5: Eliminate the Third Entry in Row 2

Apply:

$$
R_2 \rightarrow R_2 - R_3
$$

We obtain:

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{array}
\right]
$$

## Step 6: Eliminate the Second Entry in Row 1

Apply:

$$
R_1 \rightarrow R_1 - R_2
$$

We obtain:

$$
\left[
\begin{array}{ccc|ccc}
1 & 0 & 0 & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{array}
\right]
$$

The left side is now the identity matrix, so the right side is the inverse of A.

## Step 7: Write the Inverse Matrix

Therefore:

$$
\boxed{
A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{pmatrix}
}
$$

## Step 8: Verify by Multiplication

We calculate:

$$
AA^{-1} =
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{pmatrix}
$$

Multiplying the rows of A by the columns of its inverse:

$$
AA^{-1} =
\begin{pmatrix}
\frac{1}{2}+\frac{1}{2} &
-\frac{1}{2}+\frac{1}{2} &
\frac{1}{2}-\frac{1}{2} \\

\frac{1}{2}-\frac{1}{2} &
\frac{1}{2}+\frac{1}{2} &
-\frac{1}{2}+\frac{1}{2} \\

\frac{1}{2}-\frac{1}{2} &
-\frac{1}{2}+\frac{1}{2} &
\frac{1}{2}+\frac{1}{2}
\end{pmatrix}
$$

Simplifying:

$$
AA^{-1} =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
= I
$$

## Explanation

The Gauss-Jordan method applies elementary row operations to both A and the identity matrix simultaneously.

When the left side becomes I, the right side contains the inverse matrix because the same sequence of operations transforms A into I.

## Conclusion

Using Gauss-Jordan elimination, we obtained:

$$
\boxed{
A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{pmatrix}
}
$$

Since:

$$
AA^{-1} = I
$$

the inverse has been verified successfully.
