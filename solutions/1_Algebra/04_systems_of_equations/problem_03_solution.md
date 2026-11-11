
# Exercise 3: Inconsistent System

## Given System of Equations

We are given the following system:

$$
\begin{cases}
x+2y=3 \\
2x+4y=7
\end{cases}
$$

Our goal is to determine whether this system has a solution.

We will use Gaussian elimination to identify any contradiction and then explain the result using the original equations.

## Step 1: Write the System in Matrix Form

The system can be written as:

$$
Ax=b
$$

where the coefficient matrix is:

$$
A=
\begin{pmatrix}
1 & 2 \\
2 & 4
\end{pmatrix}
$$

The vector of unknowns is:

$$
\mathbf{x}=
\begin{pmatrix}
x \\
y
\end{pmatrix}
$$

The right-hand side vector is:

$$
b=
\begin{pmatrix}
3 \\
7
\end{pmatrix}
$$

Therefore:

$$
\begin{pmatrix}
1 & 2 \\
2 & 4
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=
\begin{pmatrix}
3 \\
7
\end{pmatrix}
$$

## Step 2: Construct the Augmented Matrix

To apply Gaussian elimination, we write the augmented matrix:

$$
[A|b]=
\left[
\begin{array}{cc|c}
1 & 2 & 3 \\
2 & 4 & 7
\end{array}
\right]
$$

Our goal is to eliminate the entry below the first pivot.

The first pivot is 1 in the first row and first column.

## Step 3: Apply Gaussian Elimination

We eliminate the coefficient 2 in the second row.

Apply the row operation:

$$
R_2 \rightarrow R_2-2R_1
$$

First, multiply the first row by 2:

$$
2R_1=(2,4,6)
$$

Now subtract this from the second row:

$$
R_2-2R_1=(2,4,7)-(2,4,6)
$$

Calculating each entry:

$$
=(2-2,\ 4-4,\ 7-6)
$$

$$
=(0,0,1)
$$

Therefore, the augmented matrix becomes:

$$
\boxed{
\left[
\begin{array}{cc|c}
1 & 2 & 3 \\
0 & 0 & 1
\end{array}
\right]
}
$$

This is the row echelon form of the augmented matrix.

## Step 4: Identify the Contradiction

The second row of the augmented matrix represents:

$$
0x+0y=1
$$

Simplifying:

$$
0=1
$$

This statement is mathematically impossible.

Therefore, the system contains a contradiction.

There are no values of x and y that can satisfy both equations simultaneously.

Hence:

$$
\boxed{\text{The system has no solution.}}
$$

The system is called inconsistent.

## Step 5: Explain the Contradiction Using the Original Equations

Consider the original system:

$$
\begin{cases}
x+2y=3 \\
2x+4y=7
\end{cases}
$$

The first equation is:

$$
x+2y=3
$$

Multiply both sides by 2:

$$
2(x+2y)=2(3)
$$

This gives:

$$
2x+4y=6
$$

However, the second equation requires:

$$
2x+4y=7
$$

Therefore, the same expression would have to satisfy:

$$
2x+4y=6
$$

and

$$
2x+4y=7
$$

Subtracting these equations gives:

$$
0=1
$$

This is impossible.

Therefore, the two equations cannot be satisfied at the same time.

## Step 6: Geometric Interpretation

Each equation represents a straight line in the coordinate plane.

The first equation is:

$$
x+2y=3
$$

Solving for y:

$$
2y=3-x
$$

$$
y=-\frac12x+\frac32
$$

The second equation is:

$$
2x+4y=7
$$

Dividing by 2:

$$
x+2y=\frac72
$$

Solving for y:

$$
y=-\frac12x+\frac74
$$

The two lines have the same slope:

$$
m=-\frac12
$$

However, they have different y-intercepts:

$$
\frac32 \neq \frac74
$$

Therefore, the lines are parallel and distinct.

Since parallel distinct lines never intersect, there is no point that satisfies both equations.

This geometrically confirms that the system has no solution.

## Step 7: Explain the General Inconsistency Condition

During Gaussian elimination, a system is inconsistent if the augmented matrix contains a row of the form:

$$
\left[
\begin{array}{cc|c}
0 & 0 & c
\end{array}
\right]
$$

where:

$$
c\neq 0
$$

Such a row represents:

$$
0x+0y=c
$$

or:

$$
0=c
$$

which is impossible for any nonzero c.

In our case, Gaussian elimination produced:

$$
\left[
\begin{array}{cc|c}
0 & 0 & 1
\end{array}
\right]
$$

Therefore, the system is inconsistent.

## Conclusion

We analyzed the system:

$$
\begin{cases}
x+2y=3 \\
2x+4y=7
\end{cases}
$$

Using Gaussian elimination, we obtained:

$$
\left[
\begin{array}{cc|c}
1 & 2 & 3 \\
0 & 0 & 1
\end{array}
\right]
$$

The second row represents:

$$
0=1
$$

which is a contradiction.

We also showed that doubling the first equation gives:

$$
2x+4y=6
$$

while the second equation requires:

$$
2x+4y=7
$$

Geometrically, the equations represent two distinct parallel lines.

Therefore:

$$
\boxed{\text{The system is inconsistent and has no solution.}}
$$
