
# Exercise 4: Gauss–Jordan Method

## Given Matrix

We are given the matrix:

$$
A = \begin{pmatrix}
1 & 2 \\
3 & 5
\end{pmatrix}
$$

Our goal is to find the inverse of A using the Gauss–Jordan elimination method.

## Step 1: Construct the Augmented Matrix

We begin by placing the identity matrix next to A:

$$
[A \mid I] =
\left[
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
3 & 5 & 0 & 1
\end{array}
\right]
$$

We will perform elementary row operations until the left side becomes the identity matrix.

## Step 2: Eliminate the First Entry in Row 2

Apply the row operation:

$$
R_2 \rightarrow R_2 - 3R_1
$$

Calculating the new second row:

$$
(3,5,0,1)-3(1,2,1,0)
=(-0,-1,-3,1)
$$

Therefore:

$$
\left[
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & -1 & -3 & 1
\end{array}
\right]
$$

## Step 3: Make the Second Pivot Equal to 1

Multiply the second row by -1:

$$
R_2 \rightarrow -R_2
$$

We obtain:

$$
\left[
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & 1 & 3 & -1
\end{array}
\right]
$$

## Step 4: Eliminate the Second Entry in Row 1

Apply the row operation:

$$
R_1 \rightarrow R_1 - 2R_2
$$

Calculating the new first row:

$$
(1,2,1,0)-2(0,1,3,-1)
=(1,0,-5,2)
$$

Therefore:

$$
\left[
\begin{array}{cc|cc}
1 & 0 & -5 & 2 \\
0 & 1 & 3 & -1
\end{array}
\right]
$$

The left side is now the identity matrix.

## Step 5: Read the Inverse Matrix

We have transformed:

$$
[A \mid I] \rightarrow [I \mid A^{-1}]
$$

Therefore:

$$
\boxed{
A^{-1} =
\begin{pmatrix}
-5 & 2 \\
3 & -1
\end{pmatrix}
}
$$

## Step 6: Verify the Result

We verify the inverse by multiplying A by the calculated inverse:

$$
AA^{-1} =
\begin{pmatrix}
1 & 2 \\
3 & 5
\end{pmatrix}
\begin{pmatrix}
-5 & 2 \\
3 & -1
\end{pmatrix}
$$

Multiplying rows by columns:

$$
AA^{-1} =
\begin{pmatrix}
1(-5)+2(3) & 1(2)+2(-1) \\
3(-5)+5(3) & 3(2)+5(-1)
\end{pmatrix}
$$

$$
AA^{-1} =
\begin{pmatrix}
-5+6 & 2-2 \\
-15+15 & 6-5
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

## Explanation of the Gauss–Jordan Method

Each elementary row operation corresponds to multiplication by an invertible elementary matrix.

When we apply these operations to the augmented matrix [A | I], we perform the same transformations on both sides.

If the combined row operations are represented by E, then:

$$
EA = I
$$

Therefore:

$$
E = A^{-1}
$$

Since the right side started as I, the same operations transform it into:

$$
EI = E = A^{-1}
$$

This explains why obtaining the identity matrix on the left produces the inverse matrix on the right.

## Conclusion

Using the Gauss–Jordan elimination method, we found:

$$
\boxed{
A^{-1} =
\begin{pmatrix}
-5 & 2 \\
3 & -1
\end{pmatrix}
}
$$

The result was verified by matrix multiplication:

$$
AA^{-1} = I
$$

Therefore, the calculated inverse is correct.
