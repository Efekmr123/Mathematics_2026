
# Exercise 15: Two Methods for Solving the Same System

## Given Matrices

We are given the linear system:

$$
Ax=b
$$

where:

$$
A=
\begin{pmatrix}
2 & 1\\
1 & 3
\end{pmatrix},
\qquad
b=
\begin{pmatrix}
7\\
8
\end{pmatrix}
$$

Our goal is to solve the system using two different methods:

1. The inverse matrix method, using $x=A^{-1}b$.
2. Gaussian elimination.

We will then compare the essential steps of both methods and determine which method is simpler for this particular system.

## Method 1: Solving Using the Inverse Matrix

### Step 1: Calculate the Determinant of A

For a 2x2 matrix:

$$
A=
\begin{pmatrix}
a & b\\
c & d
\end{pmatrix}
$$

the determinant is:

$$
\det(A)=ad-bc
$$

For our matrix:

$$
\det(A)=(2)(3)-(1)(1)
$$

$$
\det(A)=6-1=5
$$

Since:

$$
\det(A)\neq 0
$$

the matrix A is invertible, so we can use the inverse matrix method.

### Step 2: Calculate the Inverse of A

The inverse formula for a 2x2 matrix is:

$$
A^{-1}=
\frac{1}{ad-bc}
\begin{pmatrix}
d & -b\\
-c & a
\end{pmatrix}
$$

Substituting the values:

$$
A^{-1}=
\frac{1}{5}
\begin{pmatrix}
3 & -1\\
-1 & 2
\end{pmatrix}
$$

Therefore:

$$
\boxed{
A^{-1}=
\begin{pmatrix}
\frac35 & -\frac15\\
-\frac15 & \frac25
\end{pmatrix}
}
$$

### Step 3: Calculate x = A^(-1)b

Using the formula:

$$
x=A^{-1}b
$$

we substitute the matrices:

$$
x=
\frac15
\begin{pmatrix}
3 & -1\\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
7\\
8
\end{pmatrix}
$$

Multiplying the matrix by the vector:

$$
x=
\frac15
\begin{pmatrix}
3(7)+(-1)(8)\\
(-1)(7)+2(8)
\end{pmatrix}
$$

Simplifying:

$$
x=
\frac15
\begin{pmatrix}
21-8\\
-7+16
\end{pmatrix}
$$

$$
x=
\frac15
\begin{pmatrix}
13\\
9
\end{pmatrix}
$$

Therefore:

$$
\boxed{
x=
\begin{pmatrix}
\frac{13}{5}\\
\frac95
\end{pmatrix}
}
$$

Thus:

$$
x_1=\frac{13}{5},
\qquad
x_2=\frac95
$$

## Method 2: Solving Using Gaussian Elimination

### Step 1: Write the System of Equations

The matrix equation:

$$
Ax=b
$$

corresponds to the following system:

$$
\begin{cases}
2x_1+x_2=7\\
x_1+3x_2=8
\end{cases}
$$

We will solve this system using elementary row operations.

### Step 2: Construct the Augmented Matrix

The augmented matrix is:

$$
[A|b]=
\left[
\begin{array}{cc|c}
2 & 1 & 7\\
1 & 3 & 8
\end{array}
\right]
$$

Our goal is to transform the coefficient matrix into row echelon form.

### Step 3: Swap the Rows

We swap the first and second rows to obtain a leading coefficient of 1.

Row operation:

$$
R_1\leftrightarrow R_2
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{cc|c}
1 & 3 & 8\\
2 & 1 & 7
\end{array}
\right]
$$

### Step 4: Eliminate the Entry Below the First Pivot

We eliminate the 2 in the first column of the second row.

Row operation:

$$
R_2\rightarrow R_2-2R_1
$$

Calculating the new second row:

$$
(2,1,7)-2(1,3,8)
$$

$$
=(2-2,\ 1-6,\ 7-16)
$$

$$
=(0,-5,-9)
$$

Therefore, the augmented matrix becomes:

$$
\left[
\begin{array}{cc|c}
1 & 3 & 8\\
0 & -5 & -9
\end{array}
\right]
$$

This is now in row echelon form.

### Step 5: Solve for the Second Variable

The second row represents:

$$
-5x_2=-9
$$

Dividing both sides by -5:

$$
\boxed{x_2=\frac95}
$$

### Step 6: Use Back Substitution

The first row represents:

$$
x_1+3x_2=8
$$

Substitute:

$$
x_2=\frac95
$$

We obtain:

$$
x_1+3\left(\frac95\right)=8
$$

$$
x_1+\frac{27}{5}=8
$$

Express 8 with denominator 5:

$$
x_1=\frac{40}{5}-\frac{27}{5}
$$

Therefore:

$$
\boxed{x_1=\frac{13}{5}}
$$

### Step 7: Write the Solution Vector

The solution obtained using Gaussian elimination is:

$$
\boxed{
x=
\begin{pmatrix}
\frac{13}{5}\\
\frac95
\end{pmatrix}
}
$$

This is exactly the same result obtained using the inverse matrix method.

## Step 3: Verify Both Solutions

Both methods produced:

$$
x=
\begin{pmatrix}
\frac{13}{5}\\
\frac95
\end{pmatrix}
$$

We verify the solution by substituting it into the original matrix equation:

$$
Ax=b
$$

Substituting:

$$
Ax=
\begin{pmatrix}
2 & 1\\
1 & 3
\end{pmatrix}
\begin{pmatrix}
\frac{13}{5}\\
\frac95
\end{pmatrix}
$$

Multiplying:

$$
Ax=
\begin{pmatrix}
2(\frac{13}{5})+\frac95\\
\frac{13}{5}+3(\frac95)
\end{pmatrix}
$$

Simplifying:

$$
Ax=
\begin{pmatrix}
\frac{26}{5}+\frac95\\
\frac{13}{5}+\frac{27}{5}
\end{pmatrix}
$$

$$
Ax=
\begin{pmatrix}
\frac{35}{5}\\
\frac{40}{5}
\end{pmatrix}
$$

Therefore:

$$
Ax=
\begin{pmatrix}
7\\
8
\end{pmatrix}
=b
$$

Thus:

$$
\boxed{Ax=b}
$$

The solution is correct.

## Step 4: Compare the Two Methods

### Method 1: Inverse Matrix Method

The essential steps are:

1. Calculate the determinant of A.
2. Check that the determinant is nonzero.
3. Calculate the inverse matrix $A^{-1}$.
4. Multiply the inverse matrix by b.
5. Obtain the solution vector.

The main formula is:

$$
x=A^{-1}b
$$

**Advantages:**

- Provides a direct formula for the solution.
- Is convenient for small matrices with easily calculated inverses.
- Can be useful when solving several systems with the same coefficient matrix A but different right-hand sides.

**Disadvantages:**

- Requires A to be invertible.
- Computing the full inverse can require additional calculations.
- Is often inefficient for large systems.

### Method 2: Gaussian Elimination

The essential steps are:

1. Construct the augmented matrix $[A|b]$.
2. Apply elementary row operations.
3. Transform the system into row echelon form.
4. Use back substitution to calculate the unknowns.
5. Obtain the solution vector.

**Advantages:**

- Does not require explicitly calculating the inverse matrix.
- Can be applied to square and rectangular systems.
- Can identify systems with no solution or infinitely many solutions.
- Is generally more practical for solving a single linear system.

**Disadvantages:**

- Requires careful row operations.
- Arithmetic errors may occur during elimination and back substitution.

## Step 5: Which Method Is Simpler?

For this particular 2x2 system, Gaussian elimination is slightly simpler.

The inverse matrix method requires calculating the determinant, constructing the inverse matrix, and multiplying it by b.

Gaussian elimination only requires a row swap, one elimination operation, and back substitution.

Therefore, Gaussian elimination solves the system without explicitly calculating the inverse matrix.

However, both methods are straightforward for this small system, and both produce the same unique solution.

If we needed to solve several systems with the same invertible coefficient matrix but different right-hand sides, having the inverse matrix already available could be useful.

## Conclusion

We solved the system:

$$
\begin{cases}
2x_1+x_2=7\\
x_1+3x_2=8
\end{cases}
$$

using two different methods.

**Method 1: Inverse Matrix**

$$
x=A^{-1}b=
\begin{pmatrix}
\frac{13}{5}\\
\frac95
\end{pmatrix}
$$

**Method 2: Gaussian Elimination**

$$
x=
\begin{pmatrix}
\frac{13}{5}\\
\frac95
\end{pmatrix}
$$

Both methods give the same result:

$$
\boxed{
x_1=\frac{13}{5},
\qquad
x_2=\frac95
}
$$

The solution was verified by showing that:

$$
Ax=b
$$

For this particular system, Gaussian elimination is slightly simpler because it avoids calculating the full inverse matrix.

Both methods are mathematically valid and demonstrate different approaches to solving linear systems.
