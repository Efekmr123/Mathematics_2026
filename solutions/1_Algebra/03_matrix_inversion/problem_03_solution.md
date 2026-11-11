
# Exercise 3: When Does the Inverse Not Exist?

## Given Matrix

We are given the matrix:

$$
A = \begin{pmatrix}
2 & 4 \\
1 & 2
\end{pmatrix}
$$

We need to explain why the inverse of A does not exist using two different methods.

## Method 1: Using the Determinant

For a 2x2 matrix:

$$
A = \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

the determinant is calculated as:

$$
\det(A) = ad - bc
$$

Substituting the values from our matrix:

$$
\det(A) = (2)(2) - (4)(1)
$$

$$
\det(A) = 4 - 4 = 0
$$

A square matrix is invertible if and only if its determinant is nonzero.

Since:

$$
\det(A) = 0
$$

the matrix is singular and its inverse does not exist.

Therefore:

$$
\boxed{A^{-1} \text{ does not exist}}
$$

## Method 2: Using Linear Dependence Between Rows

Now we examine the rows of the matrix:

$$
R_1 = (2,4)
$$

$$
R_2 = (1,2)
$$

We can observe that the first row is exactly twice the second row:

$$
R_1 = 2R_2
$$

Indeed:

$$
(2,4) = 2(1,2)
$$

This means that the rows are linearly dependent.

Since one row can be obtained by multiplying another row by a constant, the rows do not provide independent information.

A square matrix with linearly dependent rows cannot have full rank.

In this case:

$$
\operatorname{rank}(A) = 1 < 2
$$

Therefore, the matrix is not invertible.

## Conclusion

We have shown that the inverse of A does not exist using two different methods:

1. The determinant is zero:

   $$
   \det(A) = 0
   $$

2. The rows are linearly dependent:

   $$
   R_1 = 2R_2
   $$

Both methods lead to the same conclusion:

$$
\boxed{A^{-1} \text{ does not exist}}
$$

These two observations are connected because linear dependence between the rows of a square matrix causes its determinant to be zero, making the matrix noninvertible.
