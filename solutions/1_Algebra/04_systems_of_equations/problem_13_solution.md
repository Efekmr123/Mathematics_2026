
# Exercise 13: Does Every Equation Add New Information?

## Given System of Equations

We are given the following system:

$$
\begin{cases}
x_1+x_2=10\\
x_2+x_3=8\\
x_1-x_3=2
\end{cases}
$$

Our goals are to:

1. Determine whether all three equations provide independent information.
2. Show that one equation can be derived from the other two.
3. Solve the system using Gaussian elimination.
4. Identify the pivot variables and the free variable.
5. Write the general solution in parametric form.
6. Verify the solution in all three original equations.
7. Explain why the system has infinitely many solutions.

## Step 1: Examine the Three Equations

Let us label the equations:

$$
E_1:\quad x_1+x_2=10
$$

$$
E_2:\quad x_2+x_3=8
$$

$$
E_3:\quad x_1-x_3=2
$$

We want to determine whether the third equation adds new information.

Subtract the second equation from the first equation:

$$
E_1-E_2
$$

This gives:

$$
(x_1+x_2)-(x_2+x_3)=10-8
$$

Remove the parentheses:

$$
x_1+x_2-x_2-x_3=2
$$

The terms involving $x_2$ cancel:

$$
x_1-x_3=2
$$

This is exactly the third equation:

$$
E_3:\quad x_1-x_3=2
$$

Therefore:

$$
\boxed{E_3=E_1-E_2}
$$

The third equation is a linear combination of the first two equations.

It does not provide any additional independent information.

## Step 2: Determine the Number of Independent Equations

We have three equations:

$$
E_1,\quad E_2,\quad E_3
$$

However:

$$
E_3=E_1-E_2
$$

Therefore, the third equation depends on the first two.

The first two equations are independent because neither is a scalar multiple of the other.

Thus, the system contains:

- Three equations in total.
- Two independent equations.
- One redundant equation.

Therefore:

$$
\boxed{\text{Number of independent equations}=2}
$$

This suggests that the system may have a free variable.

We will confirm this using Gaussian elimination.

## Step 3: Write the System in Matrix Form

The coefficient matrix is:

$$
A=
\begin{pmatrix}
1&1&0\\
0&1&1\\
1&0&-1
\end{pmatrix}
$$

The unknown vector is:

$$
\mathbf{x}=
\begin{pmatrix}
x_1\\
x_2\\
x_3
\end{pmatrix}
$$

The right-hand side vector is:

$$
b=
\begin{pmatrix}
10\\
8\\
2
\end{pmatrix}
$$

Therefore, the matrix equation is:

$$
A\mathbf{x}=b
$$

or:

$$
\begin{pmatrix}
1&1&0\\
0&1&1\\
1&0&-1
\end{pmatrix}
\begin{pmatrix}
x_1\\
x_2\\
x_3
\end{pmatrix}
=
\begin{pmatrix}
10\\
8\\
2
\end{pmatrix}
$$

## Step 4: Construct the Augmented Matrix

The augmented matrix is:

$$
[A|b]=
\left[
\begin{array}{ccc|c}
1&1&0&10\\
0&1&1&8\\
1&0&-1&2
\end{array}
\right]
$$

We will now use Gaussian elimination to transform this matrix into row echelon form.

## Step 5: Eliminate the First Entry of Row 3

The first pivot is the 1 in the first row and first column.

To eliminate the 1 below it, apply:

$$
R_3\rightarrow R_3-R_1
$$

Calculate the new third row:

$$
(1,0,-1,2)-(1,1,0,10)
$$

$$
=(1-1,\ 0-1,\ -1-0,\ 2-10)
$$

$$
=(0,-1,-1,-8)
$$

Therefore, the augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1&1&0&10\\
0&1&1&8\\
0&-1&-1&-8
\end{array}
\right]
$$

## Step 6: Eliminate the Second Entry of Row 3

The second pivot is the 1 in the second row and second column.

To eliminate the -1 below it, apply:

$$
R_3\rightarrow R_3+R_2
$$

Calculate:

$$
(0,-1,-1,-8)+(0,1,1,8)
$$

$$
=(0,0,0,0)
$$

Therefore, the augmented matrix becomes:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&1&0&10\\
0&1&1&8\\
0&0&0&0
\end{array}
\right]
}
$$

This is row echelon form.

The last row contains only zeros.

It represents:

$$
0=0
$$

This is always true and does not introduce any new condition.

The zero row confirms that the third original equation is redundant.

## Step 7: Identify the Pivot Variables and Free Variable

The row echelon matrix is:

$$
\left[
\begin{array}{ccc|c}
1&1&0&10\\
0&1&1&8\\
0&0&0&0
\end{array}
\right]
$$

The first pivot is in column 1.

The second pivot is in column 2.

There is no pivot in column 3.

Therefore:

**Pivot variables:**

$$
x_1,\quad x_2
$$

**Free variable:**

$$
x_3
$$

There are three unknowns and two pivots.

Thus:

$$
\text{Number of free variables}=3-2
$$

$$
\boxed{\text{Number of free variables}=1}
$$

Since the system is consistent and contains one free variable, it has infinitely many solutions.

## Step 8: Introduce a Parameter

Since $x_3$ is free, let:

$$
x_3=t,\qquad t\in\mathbb{R}
$$

We will express the remaining variables in terms of t.

## Step 9: Solve for x_2

The second row represents:

$$
x_2+x_3=8
$$

Substitute:

$$
x_3=t
$$

We obtain:

$$
x_2+t=8
$$

Subtract t:

$$
\boxed{x_2=8-t}
$$

## Step 10: Solve for x_1

The first row represents:

$$
x_1+x_2=10
$$

Substitute:

$$
x_2=8-t
$$

We obtain:

$$
x_1+(8-t)=10
$$

Remove the parentheses:

$$
x_1+8-t=10
$$

Subtract 8:

$$
x_1-t=2
$$

Add t:

$$
\boxed{x_1=2+t}
$$

## Step 11: Write the General Parametric Solution

We have obtained:

$$
x_1=2+t
$$

$$
x_2=8-t
$$

$$
x_3=t
$$

Therefore, the general solution is:

$$
\boxed{
\begin{cases}
x_1=2+t\\
x_2=8-t\\
x_3=t
\end{cases}
\qquad t\in\mathbb{R}
}
$$

In vector form:

$$
\boxed{
\begin{pmatrix}
x_1\\
x_2\\
x_3
\end{pmatrix}
=
\begin{pmatrix}
2+t\\
8-t\\
t
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

We can also separate the constant and parameter-dependent parts:

$$
\begin{pmatrix}
x_1\\
x_2\\
x_3
\end{pmatrix}
=
\begin{pmatrix}
2\\
8\\
0
\end{pmatrix}
+
t
\begin{pmatrix}
1\\
-1\\
1
\end{pmatrix}
$$

Thus:

$$
\boxed{
\mathbf{x}=
\begin{pmatrix}
2\\
8\\
0
\end{pmatrix}
+
t
\begin{pmatrix}
1\\
-1\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

This describes the complete solution set.

## Step 12: Verify the First Equation

The first equation is:

$$
x_1+x_2=10
$$

Substitute the general solution:

$$
(2+t)+(8-t)
$$

Remove the parentheses:

$$
=2+t+8-t
$$

The parameter terms cancel:

$$
=10
$$

Therefore:

$$
\boxed{10=10}
$$

The first equation is satisfied for every real t.

## Step 13: Verify the Second Equation

The second equation is:

$$
x_2+x_3=8
$$

Substitute:

$$
(8-t)+t
$$

Simplify:

$$
=8-t+t
$$

$$
=8
$$

Therefore:

$$
\boxed{8=8}
$$

The second equation is satisfied for every real t.

## Step 14: Verify the Third Equation

The third equation is:

$$
x_1-x_3=2
$$

Substitute:

$$
(2+t)-t
$$

Simplify:

$$
=2+t-t
$$

$$
=2
$$

Therefore:

$$
\boxed{2=2}
$$

The third equation is satisfied for every real t.

All three original equations are satisfied.

Thus, the parametric solution is correct.

## Step 15: Verify a Numerical Example

Choose:

$$
t=3
$$

Then:

$$
x_1=2+3=5
$$

$$
x_2=8-3=5
$$

$$
x_3=3
$$

Therefore:

$$
\boxed{(x_1,x_2,x_3)=(5,5,3)}
$$

Check the first equation:

$$
5+5=10
$$

Check the second equation:

$$
5+3=8
$$

Check the third equation:

$$
5-3=2
$$

All three equations are satisfied.

Therefore, $(5,5,3)$ is one valid solution.

## Step 16: Explain Why There Are Infinitely Many Solutions

The system has three unknown variables:

$$
x_1,\quad x_2,\quad x_3
$$

However, only two equations are independent.

Gaussian elimination produced:

$$
\left[
\begin{array}{ccc|c}
1&1&0&10\\
0&1&1&8\\
0&0&0&0
\end{array}
\right]
$$

There are two pivots and one free variable.

The free variable can take any real value:

$$
x_3=t,\qquad t\in\mathbb{R}
$$

For every choice of t, we obtain a solution.

For example:

| Parameter t | x_1 | x_2 | x_3 |
|---|---|---|---|
| 0 | 2 | 8 | 0 |
| 1 | 3 | 7 | 1 |
| 2 | 4 | 6 | 2 |
| 3 | 5 | 5 | 3 |
| -1 | 1 | 9 | -1 |

Each row represents a different valid solution.

Since t can take infinitely many real values, the system has infinitely many solutions.

## Step 17: Confirm the Number of Independent Equations Using Rank

The coefficient matrix is:

$$
A=
\begin{pmatrix}
1&1&0\\
0&1&1\\
1&0&-1
\end{pmatrix}
$$

After Gaussian elimination, we obtained:

$$
\begin{pmatrix}
1&1&0\\
0&1&1\\
0&0&0
\end{pmatrix}
$$

There are two nonzero rows.

Therefore:

$$
\boxed{\operatorname{rank}(A)=2}
$$

The augmented matrix also has two nonzero rows and no contradictory row.

Therefore:

$$
\boxed{\operatorname{rank}([A|b])=2}
$$

Since:

$$
\operatorname{rank}(A)=\operatorname{rank}([A|b])
$$

the system is consistent.

There are three unknowns, but the rank is only 2.

Therefore:

$$
3-\operatorname{rank}(A)=3-2=1
$$

The system has one free variable.

This confirms that the system has infinitely many solutions.

## Step 18: Geometric Interpretation

Each linear equation in three variables represents a plane in three-dimensional space.

The first equation represents:

$$
x_1+x_2=10
$$

The second equation represents:

$$
x_2+x_3=8
$$

The third equation represents:

$$
x_1-x_3=2
$$

Since the third equation follows from the first two, it does not introduce an additional independent restriction.

The first two planes intersect along a straight line.

Every point on that line also satisfies the third equation.

The solution line is:

$$
\boxed{
\mathbf{x}=
\begin{pmatrix}
2\\
8\\
0
\end{pmatrix}
+
t
\begin{pmatrix}
1\\
-1\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

The point:

$$
(2,8,0)
$$

lies on the line.

The direction vector is:

$$
\begin{pmatrix}
1\\
-1\\
1
\end{pmatrix}
$$

Therefore, the solution set is a line in three-dimensional space.

## Conclusion

We analyzed the system:

$$
\begin{cases}
x_1+x_2=10\\
x_2+x_3=8\\
x_1-x_3=2
\end{cases}
$$

First, we showed that the third equation can be obtained by subtracting the second equation from the first:

$$
\boxed{E_3=E_1-E_2}
$$

Therefore, only two equations are independent.

Using Gaussian elimination, we obtained:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&1&0&10\\
0&1&1&8\\
0&0&0&0
\end{array}
\right]
}
$$

The pivot variables are:

$$
x_1,\quad x_2
$$

The free variable is:

$$
x_3=t
$$

The general solution is:

$$
\boxed{
(x_1,x_2,x_3)=(2+t,8-t,t),
\qquad t\in\mathbb{R}
}
$$

We verified the solution in all three original equations.

The coefficient matrix has rank 2, and the system has one free variable.

Therefore, the system has infinitely many solutions.

Geometrically, the solution set is a straight line in three-dimensional space.
