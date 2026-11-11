
# Exercise 4: Infinitely Many Solutions

## Given System of Equations

We are given the following system:

$$
\begin{cases}
x+y+z=2\\
2x+2y+2z=4\\
x-y+z=0
\end{cases}
$$

Our goals are to:

1. Solve the system using Gaussian elimination.
2. Determine why the system has infinitely many solutions.
3. Express all solutions in parametric form.
4. Identify a free variable.
5. Choose a parameter value and verify the resulting solution in all three original equations.

## Step 1: Construct the Augmented Matrix

The coefficient matrix is:

$$
A=
\begin{pmatrix}
1&1&1\\
2&2&2\\
1&-1&1
\end{pmatrix}
$$

The right-hand side vector is:

$$
b=
\begin{pmatrix}
2\\
4\\
0
\end{pmatrix}
$$

Therefore, the augmented matrix is:

$$
[A|b]=
\left[
\begin{array}{ccc|c}
1&1&1&2\\
2&2&2&4\\
1&-1&1&0
\end{array}
\right]
$$

We will use elementary row operations to transform this matrix into row echelon form.

## Step 2: Eliminate the First Entry of Row 2

The first pivot is the 1 in the first row and first column.

To eliminate the 2 below this pivot, apply:

$$
R_2\rightarrow R_2-2R_1
$$

Calculate the new second row:

$$
(2,2,2,4)-2(1,1,1,2)
$$

$$
=(2-2,\ 2-2,\ 2-2,\ 4-4)
$$

$$
=(0,0,0,0)
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1&1&1&2\\
0&0&0&0\\
1&-1&1&0
\end{array}
\right]
$$

The second row is now entirely zero.

This means that the second original equation does not provide any new information beyond the first equation.

Indeed:

$$
2(x+y+z)=2(2)
$$

which gives:

$$
2x+2y+2z=4
$$

Therefore, the second equation is simply twice the first equation.

## Step 3: Eliminate the First Entry of Row 3

We now eliminate the 1 in the first column of the third row.

Apply:

$$
R_3\rightarrow R_3-R_1
$$

Calculate:

$$
(1,-1,1,0)-(1,1,1,2)
$$

$$
=(1-1,\ -1-1,\ 1-1,\ 0-2)
$$

$$
=(0,-2,0,-2)
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1&1&1&2\\
0&0&0&0\\
0&-2&0&-2
\end{array}
\right]
$$

## Step 4: Swap Rows to Obtain Row Echelon Form

The second row is zero, while the third row is nonzero.

We swap these rows:

$$
R_2\leftrightarrow R_3
$$

The augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1&1&1&2\\
0&-2&0&-2\\
0&0&0&0
\end{array}
\right]
$$

Next, divide the second row by -2:

$$
R_2\rightarrow -\frac12R_2
$$

We obtain:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&1&1&2\\
0&1&0&1\\
0&0&0&0
\end{array}
\right]
}
$$

This matrix is in row echelon form.

## Step 5: Identify the Pivot Variables and Free Variable

The row echelon matrix is:

$$
\left[
\begin{array}{ccc|c}
1&1&1&2\\
0&1&0&1\\
0&0&0&0
\end{array}
\right]
$$

There are two pivot columns:

- Column 1, corresponding to x.
- Column 2, corresponding to y.

The third column has no pivot.

Therefore:

- x is a pivot variable.
- y is a pivot variable.
- z is a free variable.

We have three unknowns but only two independent equations.

The final row represents:

$$
0=0
$$

This is always true and does not introduce a contradiction.

Therefore, the system is consistent and contains one free variable.

Since the free variable can take any real value, the system has infinitely many solutions.

## Step 6: Solve Using Back Substitution

The second row represents:

$$
y=1
$$

Therefore:

$$
\boxed{y=1}
$$

The first row represents:

$$
x+y+z=2
$$

Substitute y = 1:

$$
x+1+z=2
$$

Subtract 1:

$$
x+z=1
$$

Therefore:

$$
\boxed{x=1-z}
$$

Because z is a free variable, we can choose its value freely.

## Step 7: Introduce a Parameter

Let:

$$
z=t,\qquad t\in\mathbb{R}
$$

Substituting into the expressions for x and y:

$$
x=1-t
$$

$$
y=1
$$

$$
z=t
$$

Therefore, the general solution is:

$$
\boxed{
\begin{cases}
x=1-t\\
y=1\\
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
1-t\\
1\\
t
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

We can also express the solution as:

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
-1\\
0\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

This is the parametric vector form of the complete solution set.

## Step 8: Choose a Parameter Value

To verify the solution, choose:

$$
t=2
$$

Using the parametric equations:

$$
x=1-t=1-2=-1
$$

$$
y=1
$$

$$
z=t=2
$$

Therefore, one particular solution is:

$$
\boxed{(x,y,z)=(-1,1,2)}
$$

We will substitute this point into all three original equations.

## Step 9: Verify the First Equation

The first equation is:

$$
x+y+z=2
$$

Substituting:

$$
-1+1+2=2
$$

Simplifying:

$$
2=2
$$

The first equation is satisfied.

## Step 10: Verify the Second Equation

The second equation is:

$$
2x+2y+2z=4
$$

Substituting:

$$
2(-1)+2(1)+2(2)=4
$$

Simplifying:

$$
-2+2+4=4
$$

$$
4=4
$$

The second equation is satisfied.

## Step 11: Verify the Third Equation

The third equation is:

$$
x-y+z=0
$$

Substituting:

$$
-1-1+2=0
$$

Simplifying:

$$
0=0
$$

The third equation is satisfied.

Therefore, the point:

$$
(-1,1,2)
$$

is a valid solution.

## Step 12: Verify the General Parametric Solution

We can also check that the solution works for every real value of t.

Recall:

$$
x=1-t,\qquad y=1,\qquad z=t
$$

### First Equation

$$
x+y+z=(1-t)+1+t
$$

$$
=2
$$

Therefore, the first equation is satisfied for every real t.

### Second Equation

$$
2x+2y+2z=2(1-t)+2(1)+2t
$$

$$
=2-2t+2+2t
$$

$$
=4
$$

Therefore, the second equation is satisfied for every real t.

### Third Equation

$$
x-y+z=(1-t)-1+t
$$

$$
=1-t-1+t
$$

$$
=0
$$

Therefore, the third equation is satisfied for every real t.

This confirms that the parametric solution describes infinitely many valid solutions.

## Step 13: Explain Why There Are Infinitely Many Solutions

After Gaussian elimination, the augmented matrix is:

$$
\left[
\begin{array}{ccc|c}
1&1&1&2\\
0&1&0&1\\
0&0&0&0
\end{array}
\right]
$$

There are:

- Three unknown variables.
- Two pivot columns.
- One free variable.
- No contradictory row.

The free variable z can take any real value.

Each choice of z determines a corresponding value of x, while y remains equal to 1.

For example:

If t = 0:

$$
(x,y,z)=(1,1,0)
$$

If t = 1:

$$
(x,y,z)=(0,1,1)
$$

If t = 2:

$$
(x,y,z)=(-1,1,2)
$$

These are different solutions of the same system.

Since there are infinitely many real values of t, the system has infinitely many solutions.

## Conclusion

We solved the system:

$$
\begin{cases}
x+y+z=2\\
2x+2y+2z=4\\
x-y+z=0
\end{cases}
$$

using Gaussian elimination.

The row echelon form is:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&1&1&2\\
0&1&0&1\\
0&0&0&0
\end{array}
\right]
}
$$

The pivot variables are x and y, while z is a free variable.

Letting z = t gives the general solution:

$$
\boxed{
(x,y,z)=(1-t,1,t),
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
1\\
1\\
0
\end{pmatrix}
+
t
\begin{pmatrix}
-1\\
0\\
1
\end{pmatrix},
\qquad t\in\mathbb{R}
}
$$

For t = 2, we obtained:

$$
(x,y,z)=(-1,1,2)
$$

We verified that this point satisfies all three original equations.

We also checked that the parametric solution satisfies the system for every real value of t.

Therefore:

$$
\boxed{\text{The system has infinitely many solutions.}}
$$
