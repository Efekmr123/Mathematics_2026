
# Exercise 5: Row Echelon Form and Number of Solutions

## Given Augmented Matrix

We are given the following augmented matrix:

$$
\left[
\begin{array}{ccc|c}
1 & 2 & -1 & 3\\
0 & 1 & 2 & 1\\
0 & 0 & 0 & 0
\end{array}
\right]
$$

The matrix is already in row echelon form.

Our goals are to:

1. Determine the number of solutions.
2. Identify the pivot variables and free variables.
3. Express all solutions in parametric form.
4. Explain how the row echelon form determines the number of freely chosen variables.
5. Verify the general solution.

## Step 1: Convert the Matrix into Equations

The augmented matrix represents a system with three unknowns:

$$
x,\quad y,\quad z
$$

The first row represents:

$$
x+2y-z=3
$$

The second row represents:

$$
y+2z=1
$$

The third row represents:

$$
0x+0y+0z=0
$$

Therefore, the corresponding system is:

$$
\begin{cases}
x+2y-z=3\\
y+2z=1\\
0=0
\end{cases}
$$

The third equation is always true.

It does not provide any additional restriction on the unknown variables.

## Step 2: Identify the Pivot Positions

The given matrix is:

$$
\left[
\begin{array}{ccc|c}
\boxed{1} & 2 & -1 & 3\\
0 & \boxed{1} & 2 & 1\\
0 & 0 & 0 & 0
\end{array}
\right]
$$

A pivot is the first nonzero entry of a nonzero row in row echelon form.

The first pivot is located in column 1.

The second pivot is located in column 2.

There is no pivot in column 3.

Therefore:

- Column 1 is a pivot column.
- Column 2 is a pivot column.
- Column 3 is a free-variable column.

The corresponding variables are:

**Pivot variables:**

$$
x,\quad y
$$

**Free variable:**

$$
z
$$

## Step 3: Determine the Number of Free Variables

The system contains three unknown variables.

The row echelon form has two pivot columns in the coefficient part.

Therefore:

$$
\text{Number of free variables}
=
\text{Number of unknowns}
-
\text{Number of pivots}
$$

Substituting:

$$
3-2=1
$$

Thus:

$$
\boxed{\text{Number of free variables}=1}
$$

The variable z can be assigned any real value.

The remaining variables x and y will be determined by that choice.

## Step 4: Determine the Number of Solutions

The last row of the augmented matrix is:

$$
\left[
\begin{array}{ccc|c}
0 & 0 & 0 & 0
\end{array}
\right]
$$

This row represents:

$$
0=0
$$

Therefore, it does not create a contradiction.

There is no row of the form:

$$
\left[
\begin{array}{ccc|c}
0 & 0 & 0 & c
\end{array}
\right],
\qquad c\neq 0
$$

Consequently, the system is consistent.

Because the system is consistent and contains one free variable, it has infinitely many solutions over the real numbers.

Therefore:

$$
\boxed{\text{The system has infinitely many solutions.}}
$$

## Step 5: Introduce a Parameter

Since z is a free variable, let:

$$
\boxed{z=t,\qquad t\in\mathbb{R}}
$$

We will express x and y in terms of t.

## Step 6: Solve for y

The second equation is:

$$
y+2z=1
$$

Substitute:

$$
z=t
$$

We obtain:

$$
y+2t=1
$$

Subtract 2t from both sides:

$$
\boxed{y=1-2t}
$$

## Step 7: Solve for x

The first equation is:

$$
x+2y-z=3
$$

Substitute:

$$
y=1-2t
$$

and:

$$
z=t
$$

We obtain:

$$
x+2(1-2t)-t=3
$$

Expand the brackets:

$$
x+2-4t-t=3
$$

Combine like terms:

$$
x+2-5t=3
$$

Subtract 2 from both sides:

$$
x-5t=1
$$

Add 5t:

$$
\boxed{x=1+5t}
$$

## Step 8: Write the Parametric Solution

We have obtained:

$$
x=1+5t
$$

$$
y=1-2t
$$

$$
z=t
$$

Therefore, the complete solution set is:

$$
\boxed{
\begin{cases}
x=1+5t\\
y=1-2t\\
z=t
\end{cases}
\qquad t\in\mathbb{R}
}
$$

Equivalently, in vector form:

$$
\boxed{
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
\begin{pmatrix}
1+5t\\
1-2t\\
t
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

We can separate the constant vector and the parameter-dependent vector:

$$
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
\begin{pmatrix}
1\\
1\\
0
\end{pmatrix}
+
t
\begin{pmatrix}
5\\
-2\\
1
\end{pmatrix}
$$

Thus, the parametric vector form is:

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
1\\
0
\end{pmatrix}
+
t
\begin{pmatrix}
5\\
-2\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

## Step 9: Verify the General Solution

We verify that our parametric solution satisfies the equations for every real value of t.

Recall:

$$
x=1+5t,\qquad y=1-2t,\qquad z=t
$$

### First Equation

The first equation is:

$$
x+2y-z=3
$$

Substitute the parametric expressions:

$$
(1+5t)+2(1-2t)-t
$$

Expand:

$$
=1+5t+2-4t-t
$$

Combine terms:

$$
=3+(5t-4t-t)
$$

$$
=3
$$

Therefore, the first equation is satisfied for every real t.

### Second Equation

The second equation is:

$$
y+2z=1
$$

Substitute:

$$
(1-2t)+2t
$$

Simplify:

$$
=1-2t+2t
$$

$$
=1
$$

Therefore, the second equation is also satisfied for every real t.

### Third Equation

The third equation is:

$$
0=0
$$

This is always true, regardless of the parameter value.

Thus, the general parametric solution satisfies every row of the augmented matrix.

## Step 10: Check a Particular Parameter Value

As an additional verification, choose:

$$
t=1
$$

Then:

$$
x=1+5(1)=6
$$

$$
y=1-2(1)=-1
$$

$$
z=1
$$

Therefore, one particular solution is:

$$
\boxed{(x,y,z)=(6,-1,1)}
$$

Check the first equation:

$$
x+2y-z=6+2(-1)-1
$$

$$
=6-2-1=3
$$

Check the second equation:

$$
y+2z=-1+2(1)
$$

$$
=-1+2=1
$$

Both equations are satisfied.

## Step 11: Explain the Relationship Between Pivots and Free Variables

In row echelon form, each pivot in the coefficient matrix determines a pivot variable.

Variables whose columns do not contain pivots are free variables.

In this problem:

- There are 3 unknown variables.
- There are 2 pivot columns.
- There is 1 free-variable column.
- The system contains no contradictory row.

The number of free variables is:

$$
3-2=1
$$

Since the free variable can take any real value, the solution set contains infinitely many points.

The solution set can be represented as a line in three-dimensional space:

$$
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
=
\begin{pmatrix}
1\\
1\\
0
\end{pmatrix}
+
t
\begin{pmatrix}
5\\
-2\\
1
\end{pmatrix}
$$

The point $(1,1,0)$ lies on this line, and the vector $(5,-2,1)$ gives its direction.

## Conclusion

We analyzed the augmented matrix:

$$
\left[
\begin{array}{ccc|c}
1 & 2 & -1 & 3\\
0 & 1 & 2 & 1\\
0 & 0 & 0 & 0
\end{array}
\right]
$$

The system has two pivot variables:

$$
x,\quad y
$$

and one free variable:

$$
z=t,\qquad t\in\mathbb{R}
$$

Using back substitution, we obtained:

$$
\boxed{
x=1+5t,\qquad y=1-2t,\qquad z=t
}
$$

The complete solution in parametric vector form is:

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
1\\
0
\end{pmatrix}
+
t
\begin{pmatrix}
5\\
-2\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

We verified the solution by substitution into the equations.

Because the system is consistent and contains one free variable:

$$
\boxed{\text{The system has infinitely many solutions.}}
$$
