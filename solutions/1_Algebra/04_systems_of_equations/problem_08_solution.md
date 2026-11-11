
# Exercise 8: Two Systems with the Same Coefficient Matrix

## Given Systems

We are given two systems of linear equations.

### System 1

$$
\begin{cases}
2x+y=5\\
x-y=1
\end{cases}
$$

### System 2

$$
\begin{cases}
2x+y=1\\
x-y=4
\end{cases}
$$

Our goals are to:

1. Solve both systems using Gaussian elimination.
2. Show the successive elimination steps.
3. Compare the row operations used in both systems.
4. Identify which calculations remain the same.
5. Explain why the same coefficient matrix allows us to reuse the elimination procedure.

## Step 1: Identify the Common Coefficient Matrix

Both systems have the same coefficients for x and y.

The coefficient matrix is:

$$
A=
\begin{pmatrix}
2&1\\
1&-1
\end{pmatrix}
$$

The vector of unknowns is:

$$
\mathbf{x}=
\begin{pmatrix}
x\\
y
\end{pmatrix}
$$

However, the right-hand side vectors are different.

For System 1:

$$
b_1=
\begin{pmatrix}
5\\
1
\end{pmatrix}
$$

For System 2:

$$
b_2=
\begin{pmatrix}
1\\
4
\end{pmatrix}
$$

Therefore, the systems can be written as:

$$
A\mathbf{x}_1=b_1
$$

and:

$$
A\mathbf{x}_2=b_2
$$

The coefficient matrix is identical, but the right-hand side vectors are different.

## Part A: Solve System 1 Using Gaussian Elimination

### Step 2: Construct the Augmented Matrix

System 1 is:

$$
\begin{cases}
2x+y=5\\
x-y=1
\end{cases}
$$

Its augmented matrix is:

$$
[A|b_1]=
\left[
\begin{array}{cc|c}
2&1&5\\
1&-1&1
\end{array}
\right]
$$

### Step 3: Swap the Rows

To obtain a leading coefficient of 1, swap the first and second rows.

Apply:

$$
R_1\leftrightarrow R_2
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{cc|c}
1&-1&1\\
2&1&5
\end{array}
\right]
$$

### Step 4: Eliminate the Entry Below the First Pivot

The first pivot is 1.

We eliminate the coefficient 2 below it.

Apply:

$$
R_2\rightarrow R_2-2R_1
$$

Calculate the new second row:

$$
(2,1,5)-2(1,-1,1)
$$

$$
=(2-2,\ 1+2,\ 5-2)
$$

$$
=(0,3,3)
$$

Therefore:

$$
\left[
\begin{array}{cc|c}
1&-1&1\\
0&3&3
\end{array}
\right]
$$

This is row echelon form.

### Step 5: Solve for y

The second row represents:

$$
3y=3
$$

Divide both sides by 3:

$$
\boxed{y=1}
$$

### Step 6: Solve for x

The first row represents:

$$
x-y=1
$$

Substitute y = 1:

$$
x-1=1
$$

Therefore:

$$
\boxed{x=2}
$$

### Step 7: Write and Verify the Solution

The solution of System 1 is:

$$
\boxed{
\mathbf{x}_1=
\begin{pmatrix}
2\\
1
\end{pmatrix}
}
$$

Verify the first equation:

$$
2(2)+1=5
$$

$$
5=5
$$

Verify the second equation:

$$
2-1=1
$$

$$
1=1
$$

Both equations are satisfied.

Therefore:

$$
\boxed{(x,y)=(2,1)}
$$

## Part B: Solve System 2 Using Gaussian Elimination

### Step 8: Construct the Augmented Matrix

System 2 is:

$$
\begin{cases}
2x+y=1\\
x-y=4
\end{cases}
$$

Its augmented matrix is:

$$
[A|b_2]=
\left[
\begin{array}{cc|c}
2&1&1\\
1&-1&4
\end{array}
\right]
$$

Notice that the coefficient part is identical to the coefficient part of System 1.

### Step 9: Swap the Rows

We use the same row operation as in System 1:

$$
R_1\leftrightarrow R_2
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{cc|c}
1&-1&4\\
2&1&1
\end{array}
\right]
$$

### Step 10: Eliminate the Entry Below the First Pivot

Again, apply:

$$
R_2\rightarrow R_2-2R_1
$$

Calculate the new second row:

$$
(2,1,1)-2(1,-1,4)
$$

$$
=(2-2,\ 1+2,\ 1-8)
$$

$$
=(0,3,-7)
$$

Therefore:

$$
\left[
\begin{array}{cc|c}
1&-1&4\\
0&3&-7
\end{array}
\right]
$$

This is row echelon form.

### Step 11: Solve for y

The second row represents:

$$
3y=-7
$$

Divide both sides by 3:

$$
\boxed{y=-\frac73}
$$

### Step 12: Solve for x

The first row represents:

$$
x-y=4
$$

Substitute:

$$
y=-\frac73
$$

We obtain:

$$
x-\left(-\frac73\right)=4
$$

$$
x+\frac73=4
$$

Subtract $\frac73$:

$$
x=4-\frac73
$$

$$
x=\frac{12}{3}-\frac73
$$

Therefore:

$$
\boxed{x=\frac53}
$$

### Step 13: Write and Verify the Solution

The solution of System 2 is:

$$
\boxed{
\mathbf{x}_2=
\begin{pmatrix}
\frac53\\
-\frac73
\end{pmatrix}
}
$$

Verify the first equation:

$$
2x+y=1
$$

Substitute:

$$
2\left(\frac53\right)-\frac73
$$

$$
=\frac{10}{3}-\frac73
$$

$$
=\frac33=1
$$

The first equation is satisfied.

Verify the second equation:

$$
x-y=4
$$

Substitute:

$$
\frac53-\left(-\frac73\right)
$$

$$
=\frac53+\frac73
$$

$$
=\frac{12}{3}=4
$$

The second equation is satisfied.

Therefore:

$$
\boxed{
(x,y)=\left(\frac53,-\frac73\right)
}
$$

## Part C: Compare the Elimination Steps

### Step 14: Compare the Initial Augmented Matrices

System 1:

$$
\left[
\begin{array}{cc|c}
2&1&5\\
1&-1&1
\end{array}
\right]
$$

System 2:

$$
\left[
\begin{array}{cc|c}
2&1&1\\
1&-1&4
\end{array}
\right]
$$

The coefficient columns are identical:

$$
\begin{pmatrix}
2&1\\
1&-1
\end{pmatrix}
$$

Only the right-hand side columns differ.

### Step 15: Compare the Row Operations

Both systems use exactly the same sequence of row operations.

**First operation:**

$$
R_1\leftrightarrow R_2
$$

**Second operation:**

$$
R_2\rightarrow R_2-2R_1
$$

These operations transform the coefficient matrix in both systems into:

$$
\begin{pmatrix}
1&-1\\
0&3
\end{pmatrix}
$$

However, the right-hand side columns become different.

For System 1:

$$
\left[
\begin{array}{cc|c}
1&-1&1\\
0&3&3
\end{array}
\right]
$$

For System 2:

$$
\left[
\begin{array}{cc|c}
1&-1&4\\
0&3&-7
\end{array}
\right]
$$

The coefficient matrix after elimination is the same in both cases.

The right-hand side values are different because the original constants were different.

## Step 16: Explain Which Calculations Can Be Reused

Gaussian elimination uses row operations determined by the coefficients of the unknown variables.

Because the coefficient matrix A is the same, we can reuse:

1. The choice of pivot positions.
2. The row swap.
3. The elimination multiplier 2.
4. The resulting upper triangular coefficient matrix.
5. The general back-substitution procedure.

The operations must still be applied to each right-hand side.

For System 1, the transformed right-hand side is:

$$
\begin{pmatrix}
1\\
3
\end{pmatrix}
$$

For System 2, the transformed right-hand side is:

$$
\begin{pmatrix}
4\\
-7
\end{pmatrix}
$$

Therefore, the same elimination procedure produces different solution vectors.

The reusable part is the elimination structure, not the numerical solution.

## Step 17: Solve Both Systems Simultaneously

Since both systems have the same coefficient matrix, we can also place their right-hand sides next to each other.

The combined matrix is:

$$
\left[
\begin{array}{cc|cc}
2&1&5&1\\
1&-1&1&4
\end{array}
\right]
$$

The first two columns contain the common coefficient matrix.

The last two columns contain the right-hand sides of System 1 and System 2.

Apply the same row swap:

$$
R_1\leftrightarrow R_2
$$

We obtain:

$$
\left[
\begin{array}{cc|cc}
1&-1&1&4\\
2&1&5&1
\end{array}
\right]
$$

Next, apply:

$$
R_2\rightarrow R_2-2R_1
$$

We obtain:

$$
\left[
\begin{array}{cc|cc}
1&-1&1&4\\
0&3&3&-7
\end{array}
\right]
$$

The second row gives:

$$
3y_1=3
$$

and:

$$
3y_2=-7
$$

Therefore:

$$
y_1=1,\qquad y_2=-\frac73
$$

Using the first row:

$$
x_1-y_1=1
$$

$$
x_2-y_2=4
$$

we obtain:

$$
x_1=2
$$

and:

$$
x_2=\frac53
$$

Thus, both solution vectors are recovered:

$$
\boxed{
\mathbf{x}_1=
\begin{pmatrix}
2\\
1
\end{pmatrix},
\qquad
\mathbf{x}_2=
\begin{pmatrix}
\frac53\\
-\frac73
\end{pmatrix}
}
$$

This combined approach demonstrates how the same row operations can be applied to multiple right-hand sides efficiently.

## Step 18: Explain Why Both Systems Have Unique Solutions

The common coefficient matrix is:

$$
A=
\begin{pmatrix}
2&1\\
1&-1
\end{pmatrix}
$$

Its determinant is:

$$
\det(A)=2(-1)-1(1)
$$

$$
=-2-1
$$

$$
\boxed{\det(A)=-3}
$$

Since:

$$
\det(A)\neq0
$$

the coefficient matrix is invertible.

Therefore, each system has exactly one solution for its given right-hand side.

This agrees with Gaussian elimination, which produced two nonzero pivots.

## Conclusion

We solved two linear systems with the same coefficient matrix using Gaussian elimination.

### System 1

$$
\begin{cases}
2x+y=5\\
x-y=1
\end{cases}
$$

The solution is:

$$
\boxed{
(x,y)=(2,1)
}
$$

### System 2

$$
\begin{cases}
2x+y=1\\
x-y=4
\end{cases}
$$

The solution is:

$$
\boxed{
(x,y)=\left(\frac53,-\frac73\right)
}
$$

Both systems use the same elimination operations:

$$
R_1\leftrightarrow R_2
$$

$$
R_2\rightarrow R_2-2R_1
$$

The resulting coefficient matrix is identical:

$$
\boxed{
\begin{pmatrix}
1&-1\\
0&3
\end{pmatrix}
}
$$

The right-hand side columns are different, producing different solutions.

Therefore, when multiple systems share the same coefficient matrix, the elimination structure can be reused.

This avoids repeating the work needed to determine pivot positions and elimination multipliers.

The calculations involving the right-hand sides must still be performed separately or simultaneously using an augmented matrix with multiple right-hand side columns.
