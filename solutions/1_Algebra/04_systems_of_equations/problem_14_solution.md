
# Exercise 14: A Small Change in the Right-Hand Side

## Given Problem

We are asked to compare two systems of linear equations that differ only in the right-hand side of their third equation.

### System 1

$$
\begin{cases}
x+y=2\\
2x-y=1\\
3x=3
\end{cases}
$$

### System 2

$$
\begin{cases}
x+y=2\\
2x-y=1\\
3x=3.1
\end{cases}
$$

Our goals are to:

1. Solve or classify both systems using Gaussian elimination.
2. Determine whether each system is consistent.
3. Explain how changing 3 to 3.1 affects the solution.
4. Verify the results using the original equations.
5. Compare the coefficient matrix, augmented matrices, and ranks.
6. Explain why a small change in the right-hand side can change the solution classification.

## Step 1: Identify the Difference Between the Systems

Both systems contain the same left-hand sides:

$$
x+y
$$

$$
2x-y
$$

$$
3x
$$

Therefore, both systems have the same coefficient matrix:

$$
A=
\begin{pmatrix}
1&1\\
2&-1\\
3&0
\end{pmatrix}
$$

However, their right-hand side vectors are different.

For System 1:

$$
b_1=
\begin{pmatrix}
2\\
1\\
3
\end{pmatrix}
$$

For System 2:

$$
b_2=
\begin{pmatrix}
2\\
1\\
3.1
\end{pmatrix}
$$

The difference is:

$$
b_2-b_1=
\begin{pmatrix}
0\\
0\\
0.1
\end{pmatrix}
$$

Thus, only one constant changes, by 0.1.

Although this change is numerically small, it can affect whether all three equations can be satisfied simultaneously.

## Part A: Solve System 1 Using Gaussian Elimination

## Step 2: Construct the Augmented Matrix

System 1 is:

$$
\begin{cases}
x+y=2\\
2x-y=1\\
3x=3
\end{cases}
$$

Its augmented matrix is:

$$
[A|b_1]=
\left[
\begin{array}{cc|c}
1&1&2\\
2&-1&1\\
3&0&3
\end{array}
\right]
$$

We will transform this matrix into row echelon form.

## Step 3: Eliminate the First Entry of Row 2

The first pivot is the 1 in the first row and first column.

Apply:

$$
R_2\rightarrow R_2-2R_1
$$

Calculate the new second row:

$$
(2,-1,1)-2(1,1,2)
$$

$$
=(2-2,\ -1-2,\ 1-4)
$$

$$
=(0,-3,-3)
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
3&0&3
\end{array}
\right]
$$

## Step 4: Eliminate the First Entry of Row 3

Apply:

$$
R_3\rightarrow R_3-3R_1
$$

Calculate:

$$
(3,0,3)-3(1,1,2)
$$

$$
=(3-3,\ 0-3,\ 3-6)
$$

$$
=(0,-3,-3)
$$

Therefore:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&-3&-3
\end{array}
\right]
$$

## Step 5: Eliminate the Second Entry of Row 3

Apply:

$$
R_3\rightarrow R_3-R_2
$$

Calculate:

$$
(0,-3,-3)-(0,-3,-3)
$$

$$
=(0,0,0)
$$

The augmented matrix becomes:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&0&0
\end{array}
\right]
}
$$

This is row echelon form.

The last row represents:

$$
0=0
$$

This is always true and does not create a contradiction.

Therefore, System 1 is consistent.

## Step 6: Solve for y

The second row represents:

$$
-3y=-3
$$

Divide both sides by -3:

$$
\boxed{y=1}
$$

## Step 7: Solve for x

The first row represents:

$$
x+y=2
$$

Substitute y = 1:

$$
x+1=2
$$

Subtract 1:

$$
\boxed{x=1}
$$

Therefore, System 1 has the solution:

$$
\boxed{(x,y)=(1,1)}
$$

There are two pivot variables and no free variables, so the solution is unique.

## Step 8: Verify System 1

We substitute:

$$
x=1,\qquad y=1
$$

into all three original equations.

### First Equation

$$
x+y=2
$$

$$
1+1=2
$$

$$
\boxed{2=2}
$$

### Second Equation

$$
2x-y=1
$$

$$
2(1)-1=1
$$

$$
\boxed{1=1}
$$

### Third Equation

$$
3x=3
$$

$$
3(1)=3
$$

$$
\boxed{3=3}
$$

All three equations are satisfied.

Therefore:

$$
\boxed{\text{System 1 has exactly one solution: }(1,1)}
$$

## Part B: Analyze System 2 Using Gaussian Elimination

## Step 9: Construct the Augmented Matrix

System 2 is:

$$
\begin{cases}
x+y=2\\
2x-y=1\\
3x=3.1
\end{cases}
$$

Its augmented matrix is:

$$
[A|b_2]=
\left[
\begin{array}{cc|c}
1&1&2\\
2&-1&1\\
3&0&3.1
\end{array}
\right]
$$

The coefficient columns are identical to those of System 1.

Only the last entry in the right-hand side column has changed.

## Step 10: Apply the Same First Row Operation

Apply:

$$
R_2\rightarrow R_2-2R_1
$$

Calculate:

$$
(2,-1,1)-2(1,1,2)
$$

$$
=(0,-3,-3)
$$

Therefore:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
3&0&3.1
\end{array}
\right]
$$

## Step 11: Eliminate the First Entry of Row 3

Apply:

$$
R_3\rightarrow R_3-3R_1
$$

Calculate:

$$
(3,0,3.1)-3(1,1,2)
$$

$$
=(3-3,\ 0-3,\ 3.1-6)
$$

$$
=(0,-3,-2.9)
$$

Therefore:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&-3&-2.9
\end{array}
\right]
$$

## Step 12: Eliminate the Second Entry of Row 3

Apply:

$$
R_3\rightarrow R_3-R_2
$$

Calculate:

$$
(0,-3,-2.9)-(0,-3,-3)
$$

$$
=(0,0,0.1)
$$

The augmented matrix becomes:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&0&0.1
\end{array}
\right]
}
$$

The third row represents:

$$
0x+0y=0.1
$$

Therefore:

$$
\boxed{0=0.1}
$$

This is impossible.

The augmented matrix contains a contradictory row.

Therefore, System 2 is inconsistent.

Hence:

$$
\boxed{\text{System 2 has no solution}}
$$

## Step 13: Verify the Inconsistency Directly

The first two equations of System 2 are:

$$
x+y=2
$$

$$
2x-y=1
$$

Add these equations:

$$
(x+y)+(2x-y)=2+1
$$

Simplify:

$$
3x=3
$$

Therefore:

$$
x=1
$$

Substitute into the first equation:

$$
1+y=2
$$

Thus:

$$
y=1
$$

The first two equations force the values:

$$
\boxed{x=1,\qquad y=1}
$$

However, the third equation of System 2 requires:

$$
3x=3.1
$$

Substitute x = 1:

$$
3(1)=3.1
$$

This gives:

$$
\boxed{3=3.1}
$$

which is false.

Therefore, the values required by the first two equations cannot satisfy the third equation.

Since the first two equations already determine x and y uniquely, no other pair can satisfy all three equations.

Thus, System 2 has no solution.

## Part C: Compare the Two Systems

## Step 14: Compare Their Row Echelon Forms

For System 1, Gaussian elimination gives:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&0&0
\end{array}
\right]
}
$$

The last row represents:

$$
0=0
$$

Therefore, the system is consistent.

For System 2, Gaussian elimination gives:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&0&0.1
\end{array}
\right]
}
$$

The last row represents:

$$
0=0.1
$$

Therefore, the system is inconsistent.

The only difference between the final augmented matrices is the last entry.

However, this difference changes the solution classification completely.

## Step 15: Explain Which Row Operations Remain the Same

Both systems have the same coefficient matrix.

Therefore, we can use the same Gaussian elimination operations:

$$
R_2\rightarrow R_2-2R_1
$$

$$
R_3\rightarrow R_3-3R_1
$$

$$
R_3\rightarrow R_3-R_2
$$

These operations transform the coefficient columns into the same row echelon form:

$$
\begin{pmatrix}
1&1\\
0&-3\\
0&0
\end{pmatrix}
$$

The right-hand side columns transform differently because their original third entries are different.

For System 1, the transformed right-hand side is:

$$
\begin{pmatrix}
2\\
-3\\
0
\end{pmatrix}
$$

For System 2, it is:

$$
\begin{pmatrix}
2\\
-3\\
0.1
\end{pmatrix}
$$

The coefficient matrix is unchanged, but the consistency condition is different.

## Step 16: Compare the Ranks

The common coefficient matrix is:

$$
A=
\begin{pmatrix}
1&1\\
2&-1\\
3&0
\end{pmatrix}
$$

Its row echelon form is:

$$
\begin{pmatrix}
1&1\\
0&-3\\
0&0
\end{pmatrix}
$$

There are two nonzero rows.

Therefore:

$$
\boxed{\operatorname{rank}(A)=2}
$$

### Rank of the Augmented Matrix for System 1

The row echelon form is:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&0&0
\end{array}
\right]
$$

There are two nonzero rows.

Therefore:

$$
\boxed{\operatorname{rank}([A|b_1])=2}
$$

Thus:

$$
\operatorname{rank}(A)=\operatorname{rank}([A|b_1])=2
$$

The system is consistent.

Since there are two unknowns and the rank is 2, the solution is unique.

### Rank of the Augmented Matrix for System 2

The row echelon form is:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&0&0.1
\end{array}
\right]
$$

There are three nonzero rows.

Therefore:

$$
\boxed{\operatorname{rank}([A|b_2])=3}
$$

Thus:

$$
\operatorname{rank}(A)=2
$$

but:

$$
\operatorname{rank}([A|b_2])=3
$$

Since:

$$
\operatorname{rank}(A)\neq\operatorname{rank}([A|b_2])
$$

the system is inconsistent.

This confirms that System 2 has no solution.

## Step 17: Explain Why a Small Change Has a Large Effect

In System 1, the third equation is:

$$
3x=3
$$

The first two equations imply:

$$
3x=3
$$

Therefore, the third equation is redundant.

It does not introduce a new restriction.

In System 2, the third equation is:

$$
3x=3.1
$$

However, the first two equations still imply:

$$
3x=3
$$

Therefore, the system requires:

$$
3x=3
$$

and:

$$
3x=3.1
$$

simultaneously.

Subtracting these conditions gives:

$$
0=0.1
$$

This contradiction makes the system inconsistent.

The important point is that exact consistency is not determined by how small a change is.

Even a small nonzero change can destroy consistency when the original equations impose an exact relationship.

## Step 18: Generalize the Third Equation

To understand the effect of the right-hand side, consider the more general system:

$$
\begin{cases}
x+y=2\\
2x-y=1\\
3x=c
\end{cases}
$$

where c is a real parameter.

The first two equations imply:

$$
3x=3
$$

Therefore, the third equation can be satisfied only when:

$$
c=3
$$

We can classify the system as follows:

### When c = 3

The third equation agrees with the first two.

The system has exactly one solution:

$$
\boxed{(x,y)=(1,1)}
$$

### When c Is Not Equal to 3

The third equation contradicts the condition obtained from the first two equations.

The system has no solution.

Therefore:

$$
\boxed{
\begin{cases}
c=3 & \text{Exactly one solution}\\
c\neq3 & \text{No solution}
\end{cases}
}
$$

This generalization explains why changing 3 to 3.1 changes the system from consistent to inconsistent.

## Step 19: Geometric Interpretation

Each equation in two variables represents a straight line in the plane.

For both systems, the first two equations are:

$$
x+y=2
$$

and:

$$
2x-y=1
$$

These lines intersect at:

$$
(1,1)
$$

The third equation of System 1 is:

$$
3x=3
$$

which simplifies to:

$$
x=1
$$

This is a vertical line passing through the point (1,1).

Therefore, all three lines have a common intersection point.

System 1 is consistent.

The third equation of System 2 is:

$$
3x=3.1
$$

which simplifies to:

$$
x=\frac{3.1}{3}=\frac{31}{30}
$$

This is a different vertical line.

It does not pass through (1,1).

Since the first two lines intersect only at (1,1), the three lines do not share a common point.

Therefore, System 2 is inconsistent.

## Step 20: Final Comparison

| Property | System 1 | System 2 |
|---|---|---|
| Third equation | 3x = 3 | 3x = 3.1 |
| Coefficient matrix | Same | Same |
| First two equations | Same | Same |
| Last row after elimination | 0 = 0 | 0 = 0.1 |
| Rank of A | 2 | 2 |
| Rank of augmented matrix | 2 | 3 |
| Consistent? | Yes | No |
| Number of solutions | Exactly one | Zero |
| Solution | (1, 1) | No solution |

## Conclusion

We compared the two systems:

**System 1:**

$$
\begin{cases}
x+y=2\\
2x-y=1\\
3x=3
\end{cases}
$$

Using Gaussian elimination, we obtained:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&0&0
\end{array}
\right]
$$

The system is consistent and has exactly one solution:

$$
\boxed{(x,y)=(1,1)}
$$

We verified that this pair satisfies all three equations.

**System 2:**

$$
\begin{cases}
x+y=2\\
2x-y=1\\
3x=3.1
\end{cases}
$$

Using the same row operations, we obtained:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-3&-3\\
0&0&0.1
\end{array}
\right]
$$

The last row gives:

$$
\boxed{0=0.1}
$$

This is a contradiction.

Therefore:

$$
\boxed{\text{System 2 has no solution}}
$$

The coefficient matrix is identical in both systems, but the right-hand side vectors are different.

Changing the third constant from 3 to 3.1 destroys the exact relationship between the equations.

Thus, even a small change in the right-hand side can change a linear system from consistent to inconsistent.
