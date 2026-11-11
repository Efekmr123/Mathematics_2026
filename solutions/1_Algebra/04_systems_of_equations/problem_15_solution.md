
# Exercise 15: Classifying Three Systems

## Given Problem

We are given three systems of linear equations.

Our task is to classify each system as having:

1. Exactly one solution.
2. Infinitely many solutions.
3. No solution.

We should use Gaussian elimination and perform only the row operations necessary to justify each classification.

We will also verify the results.

## System 1

Consider the system:

$$
\begin{cases}
x+y=2\\
x-y=0
\end{cases}
$$

### Step 1: Construct the Augmented Matrix

The augmented matrix is:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
1&-1&0
\end{array}
\right]
$$

### Step 2: Apply Gaussian Elimination

To eliminate the first entry of the second row, apply:

$$
R_2\rightarrow R_2-R_1
$$

Calculate:

$$
(1,-1,0)-(1,1,2)=(0,-2,-2)
$$

Therefore:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&2\\
0&-2&-2
\end{array}
\right]
}
$$

This matrix is in row echelon form.

### Step 3: Solve the System

The second row represents:

$$
-2y=-2
$$

Therefore:

$$
\boxed{y=1}
$$

The first row represents:

$$
x+y=2
$$

Substitute y = 1:

$$
x+1=2
$$

Therefore:

$$
\boxed{x=1}
$$

The solution is:

$$
\boxed{(x,y)=(1,1)}
$$

### Step 4: Verify the Solution

First equation:

$$
1+1=2
$$

Second equation:

$$
1-1=0
$$

Both equations are satisfied.

### Step 5: Classify System 1

The row echelon matrix contains two nonzero pivots:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-2&-2
\end{array}
\right]
$$

There are two unknowns and two pivot variables.

Therefore, there are no free variables.

There is also no contradictory row.

Thus, the system has exactly one solution.

$$
\boxed{\text{System 1: Exactly one solution}}
$$

## System 2

Consider the system:

$$
\begin{cases}
x+y=2\\
2x+2y=4
\end{cases}
$$

### Step 1: Construct the Augmented Matrix

The augmented matrix is:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
2&2&4
\end{array}
\right]
$$

### Step 2: Apply Gaussian Elimination

To eliminate the first entry of the second row, apply:

$$
R_2\rightarrow R_2-2R_1
$$

Calculate:

$$
(2,2,4)-2(1,1,2)=(0,0,0)
$$

Therefore:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&2\\
0&0&0
\end{array}
\right]
}
$$

The second row represents:

$$
0=0
$$

This is always true.

Therefore, the second equation does not provide additional independent information.

Indeed:

$$
2(x+y)=2(2)
$$

gives:

$$
2x+2y=4
$$

which is exactly the second original equation.

### Step 3: Identify the Free Variable

The row echelon matrix contains only one pivot, in the first column.

Therefore:

- x is a pivot variable.
- y is a free variable.

Let:

$$
y=t,\qquad t\in\mathbb{R}
$$

From the first equation:

$$
x+y=2
$$

we obtain:

$$
x+t=2
$$

Therefore:

$$
\boxed{x=2-t}
$$

### Step 4: Write the General Solution

The complete solution set is:

$$
\boxed{
(x,y)=(2-t,t),
\qquad t\in\mathbb{R}
}
$$

In vector form:

$$
\boxed{
\begin{pmatrix}
x\\
y
\end{pmatrix}
=
\begin{pmatrix}
2\\
0
\end{pmatrix}
+
t
\begin{pmatrix}
-1\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

### Step 5: Verify the General Solution

First equation:

$$
x+y=2
$$

Substitute:

$$
(2-t)+t=2
$$

Therefore:

$$
\boxed{2=2}
$$

Second equation:

$$
2x+2y=4
$$

Substitute:

$$
2(2-t)+2t
$$

Simplify:

$$
4-2t+2t=4
$$

Therefore:

$$
\boxed{4=4}
$$

Both equations are satisfied for every real value of t.

### Step 6: Classify System 2

There are two unknowns but only one pivot.

The system is consistent because it contains no contradictory row.

Since y is a free variable, it can take any real value.

Each value of t gives a solution.

For example:

$$
t=0\Rightarrow(x,y)=(2,0)
$$

$$
t=1\Rightarrow(x,y)=(1,1)
$$

$$
t=2\Rightarrow(x,y)=(0,2)
$$

Therefore, the system has infinitely many solutions.

$$
\boxed{\text{System 2: Infinitely many solutions}}
$$

## System 3

Consider the system:

$$
\begin{cases}
x+y=2\\
2x+2y=5
\end{cases}
$$

### Step 1: Construct the Augmented Matrix

The augmented matrix is:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
2&2&5
\end{array}
\right]
$$

### Step 2: Apply Gaussian Elimination

To eliminate the first entry of the second row, apply:

$$
R_2\rightarrow R_2-2R_1
$$

Calculate:

$$
(2,2,5)-2(1,1,2)=(0,0,1)
$$

Therefore:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&2\\
0&0&1
\end{array}
\right]
}
$$

### Step 3: Identify the Contradiction

The second row represents:

$$
0x+0y=1
$$

Therefore:

$$
\boxed{0=1}
$$

This statement is impossible.

Thus, the system is inconsistent.

### Step 4: Verify the Inconsistency Directly

The first equation is:

$$
x+y=2
$$

Multiply both sides by 2:

$$
2x+2y=4
$$

However, the second equation requires:

$$
2x+2y=5
$$

The same expression cannot equal both 4 and 5.

Subtracting these conditions gives:

$$
0=1
$$

Therefore, no pair (x,y) can satisfy both equations simultaneously.

### Step 5: Classify System 3

Gaussian elimination produces a contradictory row.

Therefore, the system has no solution.

$$
\boxed{\text{System 3: No solution}}
$$

## Comparison of the Three Systems

We can summarize the results using their row echelon forms.

### System 1

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&-2&-2
\end{array}
\right]
$$

There are two pivots and no contradiction.

Therefore:

$$
\boxed{\text{Exactly one solution}}
$$

### System 2

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&0&0
\end{array}
\right]
$$

There is one pivot, one free variable, and no contradiction.

Therefore:

$$
\boxed{\text{Infinitely many solutions}}
$$

### System 3

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&0&1
\end{array}
\right]
$$

There is a contradictory row:

$$
0=1
$$

Therefore:

$$
\boxed{\text{No solution}}
$$

## Summary Table

| System | Result of Elimination | Classification | Solution |
|---|---|---|---|
| System 1 | Two pivots, no contradiction | Exactly one solution | (1,1) |
| System 2 | One pivot, one free variable | Infinitely many solutions | (2-t,t), t in R |
| System 3 | Contradictory row 0=1 | No solution | No solution exists |

## Geometric Interpretation

Each equation in two variables represents a straight line in the plane.

### System 1: Intersecting Lines

The equations are:

$$
x+y=2
$$

$$
x-y=0
$$

Rewrite them as:

$$
y=2-x
$$

$$
y=x
$$

The slopes are different:

$$
-1\neq1
$$

Therefore, the lines intersect at exactly one point:

$$
\boxed{(1,1)}
$$

This corresponds to exactly one solution.

### System 2: Coincident Lines

The equations are:

$$
x+y=2
$$

$$
2x+2y=4
$$

Dividing the second equation by 2 gives:

$$
x+y=2
$$

Both equations represent the same line.

Therefore, every point on that line satisfies both equations.

This corresponds to infinitely many solutions.

### System 3: Parallel Distinct Lines

The equations are:

$$
x+y=2
$$

$$
2x+2y=5
$$

Rewrite the first equation:

$$
y=2-x
$$

Divide the second equation by 2:

$$
x+y=\frac52
$$

Therefore:

$$
y=\frac52-x
$$

Both lines have slope -1.

However, their y-intercepts are different:

$$
2\neq\frac52
$$

Therefore, the lines are parallel and distinct.

They never intersect.

This corresponds to no solution.

## General Classification Rule

Gaussian elimination allows us to classify a linear system by examining its row echelon form.

### Exactly One Solution

A system has exactly one solution when:

1. It is consistent.
2. Every variable is a pivot variable.
3. There are no free variables.

### Infinitely Many Solutions

A system has infinitely many solutions when:

1. It is consistent.
2. At least one variable is free.

### No Solution

A system has no solution when Gaussian elimination produces a row of the form:

$$
\left[
\begin{array}{ccc|c}
0&0&\cdots&c
\end{array}
\right]
$$

where:

$$
c\neq0
$$

Such a row represents the contradiction:

$$
0=c
$$

Therefore, the system is inconsistent.

## Conclusion

We classified three systems of linear equations using Gaussian elimination.

### System 1

$$
\begin{cases}
x+y=2\\
x-y=0
\end{cases}
$$

The system has exactly one solution:

$$
\boxed{(x,y)=(1,1)}
$$

### System 2

$$
\begin{cases}
x+y=2\\
2x+2y=4
\end{cases}
$$

The system has infinitely many solutions:

$$
\boxed{(x,y)=(2-t,t),\qquad t\in\mathbb{R}}
$$

### System 3

$$
\begin{cases}
x+y=2\\
2x+2y=5
\end{cases}
$$

The system has no solution because Gaussian elimination gives:

$$
\boxed{0=1}
$$

These examples demonstrate the three possible solution classifications for linear systems:

- Exactly one solution.
- Infinitely many solutions.
- No solution.

Gaussian elimination provides a systematic method for identifying each case.

This completes Exercise 15 and the Systems of Linear Equations exercise set.
