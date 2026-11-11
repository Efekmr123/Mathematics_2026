
# Exercise 2: Gaussian Elimination — One Solution

## Given System of Equations

We are given the following system:

$$
\begin{cases}
x+y+z=6 \\
2x-y+z=3 \\
x+2y-z=2
\end{cases}
$$

Our goal is to solve this system using Gaussian elimination and verify the result by substituting the solution into all three original equations.

## Step 1: Write the Augmented Matrix

The coefficient matrix is:

$$
A=
\begin{pmatrix}
1 & 1 & 1 \\
2 & -1 & 1 \\
1 & 2 & -1
\end{pmatrix}
$$

The right-hand side vector is:

$$
b=
\begin{pmatrix}
6 \\
3 \\
2
\end{pmatrix}
$$

Therefore, the augmented matrix is:

$$
[A|b]=
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & -1 & 1 & 3 \\
1 & 2 & -1 & 2
\end{array}
\right]
$$

We will use elementary row operations to transform this matrix into row echelon form.

## Step 2: Eliminate the First Entry of Row 2

The first pivot is the 1 in the first row and first column.

We want to eliminate the 2 below this pivot.

Apply the row operation:

$$
R_2 \rightarrow R_2-2R_1
$$

Calculate the new second row:

$$
(2,-1,1,3)-2(1,1,1,6)
$$

$$
=(2-2,-1-2,1-2,3-12)
$$

$$
=(0,-3,-1,-9)
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
1 & 2 & -1 & 2
\end{array}
\right]
$$

## Step 3: Eliminate the First Entry of Row 3

Next, we eliminate the 1 in the first column of the third row.

Apply:

$$
R_3 \rightarrow R_3-R_1
$$

Calculate the new third row:

$$
(1,2,-1,2)-(1,1,1,6)
$$

$$
=(1-1,2-1,-1-1,2-6)
$$

$$
=(0,1,-2,-4)
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
0 & 1 & -2 & -4
\end{array}
\right]
$$

## Step 4: Swap Rows to Obtain a Simpler Pivot

The third row has a coefficient of 1 in the second column.

To simplify the elimination, we swap the second and third rows.

Apply:

$$
R_2 \leftrightarrow R_3
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & -3 & -1 & -9
\end{array}
\right]
$$

Now the second pivot is 1.

## Step 5: Eliminate the Second Entry of Row 3

We want to eliminate the -3 below the second pivot.

Apply:

$$
R_3 \rightarrow R_3+3R_2
$$

Calculate the new third row:

$$
(0,-3,-1,-9)+3(0,1,-2,-4)
$$

$$
=(0,-3+3,-1-6,-9-12)
$$

$$
=(0,0,-7,-21)
$$

The augmented matrix becomes:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & 0 & -7 & -21
\end{array}
\right]
}
$$

This matrix is now in row echelon form.

All three variable columns contain pivots, so there are no free variables.

## Step 6: Solve for z Using Back Substitution

The third row represents:

$$
-7z=-21
$$

Divide both sides by -7:

$$
z=\frac{-21}{-7}
$$

Therefore:

$$
\boxed{z=3}
$$

## Step 7: Solve for y

The second row represents:

$$
y-2z=-4
$$

Substitute:

$$
z=3
$$

We obtain:

$$
y-2(3)=-4
$$

$$
y-6=-4
$$

Adding 6 to both sides:

$$
y=-4+6
$$

Therefore:

$$
\boxed{y=2}
$$

## Step 8: Solve for x

The first row represents:

$$
x+y+z=6
$$

Substitute the known values:

$$
y=2,\qquad z=3
$$

We obtain:

$$
x+2+3=6
$$

$$
x+5=6
$$

Therefore:

$$
\boxed{x=1}
$$

## Step 9: Write the Solution Vector

The solution is:

$$
x=1,\qquad y=2,\qquad z=3
$$

In vector form:

$$
\boxed{
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
\begin{pmatrix}
1\\
2\\
3
\end{pmatrix}
}
$$

## Step 10: Verify the First Equation

The first equation is:

$$
x+y+z=6
$$

Substitute the calculated values:

$$
1+2+3=6
$$

$$
6=6
$$

The first equation is satisfied.

## Step 11: Verify the Second Equation

The second equation is:

$$
2x-y+z=3
$$

Substitute:

$$
2(1)-2+3=3
$$

Simplifying:

$$
2-2+3=3
$$

$$
3=3
$$

The second equation is satisfied.

## Step 12: Verify the Third Equation

The third equation is:

$$
x+2y-z=2
$$

Substitute:

$$
1+2(2)-3=2
$$

Simplifying:

$$
1+4-3=2
$$

$$
2=2
$$

The third equation is satisfied.

## Step 13: Explain Why the Solution Is Unique

After Gaussian elimination, the augmented matrix is:

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & 0 & -7 & -21
\end{array}
\right]
$$

The coefficient matrix has three nonzero pivots:

$$
1,\quad 1,\quad -7
$$

Each of the three variables has a pivot, so there are no free variables.

There is also no contradictory row of the form:

$$
\left[
\begin{array}{ccc|c}
0 & 0 & 0 & c
\end{array}
\right],
\qquad c\neq 0
$$

Therefore, the system is consistent and has exactly one solution.

## Conclusion

We solved the system:

$$
\begin{cases}
x+y+z=6 \\
2x-y+z=3 \\
x+2y-z=2
\end{cases}
$$

using Gaussian elimination.

After applying elementary row operations and back substitution, we obtained:

$$
\boxed{
x=1,\qquad y=2,\qquad z=3
}
$$

The solution vector is:

$$
\boxed{
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
\begin{pmatrix}
1\\
2\\
3
\end{pmatrix}
}
$$

We verified the result by substituting the values into all three original equations:

$$
1+2+3=6
$$

$$
2(1)-2+3=3
$$

$$
1+2(2)-3=2
$$

All three equations are satisfied.

Since the elimination process produces a pivot for every variable and no contradictory row, the system has exactly one solution.
