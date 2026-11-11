
# Exercise 12: Homogeneous System

## Given System of Equations

We are given the following homogeneous linear system:

$$
\begin{cases}
x+2y-z=0\\
2x+4y-2z=0\\
x-y+2z=0
\end{cases}
$$

Our goals are to:

1. Solve the system using Gaussian elimination.
2. Identify the pivot variables and free variables.
3. Express the general solution in parametric form.
4. Explain why the zero solution always exists for a homogeneous system.
5. Determine whether nonzero solutions exist.
6. Verify the general solution in all three original equations.

## Step 1: Understand Homogeneous Linear Systems

A homogeneous linear system is a system in which every equation has zero on the right-hand side.

Its matrix form is:

$$
A\mathbf{x}=\mathbf{0}
$$

where A is the coefficient matrix, $\mathbf{x}$ is the vector of unknowns, and $\mathbf{0}$ is the zero vector.

For the given system:

$$
A=
\begin{pmatrix}
1&2&-1\\
2&4&-2\\
1&-1&2
\end{pmatrix}
$$

The unknown vector is:

$$
\mathbf{x}=
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
$$

The right-hand side is:

$$
\mathbf{0}=
\begin{pmatrix}
0\\
0\\
0
\end{pmatrix}
$$

Therefore:

$$
\begin{pmatrix}
1&2&-1\\
2&4&-2\\
1&-1&2
\end{pmatrix}
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
\begin{pmatrix}
0\\
0\\
0
\end{pmatrix}
$$

## Step 2: Construct the Augmented Matrix

The augmented matrix is:

$$
[A|\mathbf{0}]=
\left[
\begin{array}{ccc|c}
1&2&-1&0\\
2&4&-2&0\\
1&-1&2&0
\end{array}
\right]
$$

We will use elementary row operations to transform this matrix into row echelon form.

## Step 3: Eliminate the First Entry of Row 2

The first pivot is the 1 in the first row and first column.

To eliminate the 2 below this pivot, apply:

$$
R_2\rightarrow R_2-2R_1
$$

Calculate:

$$
(2,4,-2,0)-2(1,2,-1,0)
$$

$$
=(2-2,\ 4-4,\ -2+2,\ 0-0)
$$

$$
=(0,0,0,0)
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1&2&-1&0\\
0&0&0&0\\
1&-1&2&0
\end{array}
\right]
$$

The second row is entirely zero.

This means that the second original equation is redundant.

Indeed, multiplying the first equation by 2 gives:

$$
2(x+2y-z)=2(0)
$$

which simplifies to:

$$
2x+4y-2z=0
$$

This is exactly the second original equation.

Therefore, the second equation does not provide any new information.

## Step 4: Eliminate the First Entry of Row 3

Apply:

$$
R_3\rightarrow R_3-R_1
$$

Calculate:

$$
(1,-1,2,0)-(1,2,-1,0)
$$

$$
=(1-1,\ -1-2,\ 2+1,\ 0-0)
$$

$$
=(0,-3,3,0)
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1&2&-1&0\\
0&0&0&0\\
0&-3&3&0
\end{array}
\right]
$$

## Step 5: Swap Rows to Obtain Row Echelon Form

The second row is zero, while the third row is nonzero.

To place the zero row at the bottom, swap rows 2 and 3:

$$
R_2\leftrightarrow R_3
$$

We obtain:

$$
\left[
\begin{array}{ccc|c}
1&2&-1&0\\
0&-3&3&0\\
0&0&0&0
\end{array}
\right]
$$

Now divide the second row by -3:

$$
R_2\rightarrow-\frac13R_2
$$

The augmented matrix becomes:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&2&-1&0\\
0&1&-1&0\\
0&0&0&0
\end{array}
\right]
}
$$

This is row echelon form.

## Step 6: Identify the Pivot Variables and Free Variable

The row echelon matrix is:

$$
\left[
\begin{array}{ccc|c}
1&2&-1&0\\
0&1&-1&0\\
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
x,\quad y
$$

**Free variable:**

$$
z
$$

There are three unknowns and two pivots.

Thus:

$$
\text{Number of free variables}=3-2
$$

$$
\boxed{\text{Number of free variables}=1}
$$

Because the system is homogeneous, it is always consistent.

Since there is one free variable, the system has infinitely many solutions.

## Step 7: Solve for y

The second row represents:

$$
y-z=0
$$

Rearrange:

$$
y=z
$$

Therefore:

$$
\boxed{y=z}
$$

## Step 8: Solve for x Using Back Substitution

The first row represents:

$$
x+2y-z=0
$$

Substitute:

$$
y=z
$$

We obtain:

$$
x+2z-z=0
$$

Simplify:

$$
x+z=0
$$

Therefore:

$$
\boxed{x=-z}
$$

## Step 9: Introduce a Parameter

Since z is a free variable, let:

$$
z=t,\qquad t\in\mathbb{R}
$$

Then:

$$
y=t
$$

and:

$$
x=-t
$$

Therefore, the general solution is:

$$
\boxed{
\begin{cases}
x=-t\\
y=t\\
z=t
\end{cases}
\qquad t\in\mathbb{R}
}
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
-t\\
t\\
t
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

We can factor out t:

$$
\boxed{
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
t
\begin{pmatrix}
-1\\
1\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

This is the complete parametric solution.

## Step 10: Explain Why the Zero Solution Always Exists

For every homogeneous system:

$$
A\mathbf{x}=\mathbf{0}
$$

the zero vector is always a solution.

Let:

$$
\mathbf{x}=
\begin{pmatrix}
0\\
0\\
0
\end{pmatrix}
$$

Multiplying any matrix A by the zero vector gives:

$$
A\mathbf{0}=\mathbf{0}
$$

Therefore, the zero vector always satisfies a homogeneous system.

For our particular system, choose:

$$
t=0
$$

The parametric solution becomes:

$$
x=-0=0
$$

$$
y=0
$$

$$
z=0
$$

Thus:

$$
\boxed{(x,y,z)=(0,0,0)}
$$

This is called the trivial solution.

### Verify the Trivial Solution

First equation:

$$
0+2(0)-0=0
$$

Second equation:

$$
2(0)+4(0)-2(0)=0
$$

Third equation:

$$
0-0+2(0)=0
$$

All three equations are satisfied.

Therefore, the trivial solution exists.

## Step 11: Determine Whether Nontrivial Solutions Exist

A nontrivial solution is a solution in which at least one variable is nonzero.

Our general solution is:

$$
(x,y,z)=(-t,t,t)
$$

If we choose:

$$
t=1
$$

we obtain:

$$
x=-1
$$

$$
y=1
$$

$$
z=1
$$

Therefore:

$$
\boxed{(x,y,z)=(-1,1,1)}
$$

This is a nontrivial solution because it is not the zero vector.

### Verify the Nontrivial Solution

First equation:

$$
x+2y-z=-1+2(1)-1
$$

$$
=-1+2-1=0
$$

Second equation:

$$
2x+4y-2z=2(-1)+4(1)-2(1)
$$

$$
=-2+4-2=0
$$

Third equation:

$$
x-y+2z=-1-1+2(1)
$$

$$
=-1-1+2=0
$$

All three equations are satisfied.

Therefore, the system has nontrivial solutions.

## Step 12: Verify the General Parametric Solution

We now verify that the solution works for every real value of t.

Recall:

$$
x=-t,\qquad y=t,\qquad z=t
$$

### First Equation

$$
x+2y-z=0
$$

Substitute:

$$
(-t)+2(t)-t
$$

Simplify:

$$
=-t+2t-t
$$

$$
=0
$$

Therefore, the first equation is satisfied for every real t.

### Second Equation

$$
2x+4y-2z=0
$$

Substitute:

$$
2(-t)+4(t)-2(t)
$$

Simplify:

$$
=-2t+4t-2t
$$

$$
=0
$$

Therefore, the second equation is satisfied for every real t.

### Third Equation

$$
x-y+2z=0
$$

Substitute:

$$
(-t)-t+2(t)
$$

Simplify:

$$
=-t-t+2t
$$

$$
=0
$$

Therefore, the third equation is satisfied for every real t.

Thus, the parametric solution satisfies all three original equations for every real parameter value.

## Step 13: Explain Why the System Has Infinitely Many Solutions

The row echelon matrix is:

$$
\left[
\begin{array}{ccc|c}
1&2&-1&0\\
0&1&-1&0\\
0&0&0&0
\end{array}
\right]
$$

There are:

- Three unknown variables.
- Two pivot variables.
- One free variable.
- No contradictory equations.

The free variable z can take any real value.

Each choice of z determines corresponding values of x and y.

For example:

If t = 0:

$$
(x,y,z)=(0,0,0)
$$

If t = 1:

$$
(x,y,z)=(-1,1,1)
$$

If t = 2:

$$
(x,y,z)=(-2,2,2)
$$

If t = -1:

$$
(x,y,z)=(1,-1,-1)
$$

These are all different solutions of the same system.

Since t can take infinitely many real values, the system has infinitely many solutions.

## Step 14: Interpret the Solution Geometrically

The general solution is:

$$
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
t
\begin{pmatrix}
-1\\
1\\
1
\end{pmatrix}
$$

This describes a straight line in three-dimensional space.

The line passes through the origin because t = 0 gives:

$$
(0,0,0)
$$

Its direction vector is:

$$
\begin{pmatrix}
-1\\
1\\
1
\end{pmatrix}
$$

Every point on this line satisfies all three equations.

Therefore, the solution set is a line through the origin.

This is consistent with the fact that the system has one free variable.

## Step 15: Confirm the Result Using the Rank

The coefficient matrix is:

$$
A=
\begin{pmatrix}
1&2&-1\\
2&4&-2\\
1&-1&2
\end{pmatrix}
$$

After Gaussian elimination, its row echelon form is:

$$
\begin{pmatrix}
1&2&-1\\
0&1&-1\\
0&0&0
\end{pmatrix}
$$

There are two nonzero rows.

Therefore:

$$
\boxed{\operatorname{rank}(A)=2}
$$

There are three unknowns.

By the rank-nullity theorem:

$$
\operatorname{nullity}(A)
=
3-\operatorname{rank}(A)
$$

Thus:

$$
\operatorname{nullity}(A)=3-2
$$

$$
\boxed{\operatorname{nullity}(A)=1}
$$

The nullity is the dimension of the solution space of the homogeneous system.

Therefore, the solution space has dimension 1.

This agrees with our parametric solution, which describes a line through the origin.

## Conclusion

We solved the homogeneous system:

$$
\begin{cases}
x+2y-z=0\\
2x+4y-2z=0\\
x-y+2z=0
\end{cases}
$$

using Gaussian elimination.

The row echelon form is:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&2&-1&0\\
0&1&-1&0\\
0&0&0&0
\end{array}
\right]
}
$$

The pivot variables are x and y.

The free variable is z.

Letting:

$$
z=t,\qquad t\in\mathbb{R}
$$

we obtained:

$$
\boxed{
(x,y,z)=(-t,t,t),
\qquad t\in\mathbb{R}
}
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
t
\begin{pmatrix}
-1\\
1\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

The trivial solution:

$$
(0,0,0)
$$

always exists because the system is homogeneous.

Nontrivial solutions also exist, such as:

$$
(-1,1,1)
$$

We verified the general solution in all three original equations.

Since the system contains one free variable, it has infinitely many solutions.

The solution set is a one-dimensional line through the origin.
