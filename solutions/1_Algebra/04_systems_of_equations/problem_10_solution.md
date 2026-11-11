
# Exercise 10: A Polynomial Through Three Points

## Given Problem

We want to find a quadratic polynomial of the form:

$$
p(x)=ax^2+bx+c
$$

that passes through the following three points:

$$
(0,1),\qquad (1,3),\qquad (2,9)
$$

Our goals are to:

1. Construct a system of linear equations for the unknown coefficients a, b, and c.
2. Express the system in matrix form.
3. Solve the system using Gaussian elimination.
4. Determine the quadratic polynomial.
5. Verify that the polynomial passes through all three given points.
6. Explain why the polynomial is uniquely determined.

## Step 1: Understand the Polynomial

A quadratic polynomial has the general form:

$$
p(x)=ax^2+bx+c
$$

where:

- a is the coefficient of the quadratic term.
- b is the coefficient of the linear term.
- c is the constant term.

For a quadratic polynomial, we require:

$$
a\neq0
$$

We have three unknown coefficients:

$$
a,\quad b,\quad c
$$

Each given point provides one equation.

Therefore, the three points allow us to construct a system of three linear equations.

## Step 2: Use the First Point (0, 1)

Since the polynomial passes through (0, 1), we know:

$$
p(0)=1
$$

Substitute x = 0 into the polynomial:

$$
a(0)^2+b(0)+c=1
$$

Simplify:

$$
0+0+c=1
$$

Therefore:

$$
\boxed{c=1}
$$

This immediately determines the constant coefficient.

## Step 3: Use the Second Point (1, 3)

Since the polynomial passes through (1, 3), we know:

$$
p(1)=3
$$

Substitute x = 1:

$$
a(1)^2+b(1)+c=3
$$

Simplify:

$$
a+b+c=3
$$

Therefore:

$$
\boxed{a+b+c=3}
$$

Since c = 1:

$$
a+b+1=3
$$

Subtract 1:

$$
\boxed{a+b=2}
$$

## Step 4: Use the Third Point (2, 9)

Since the polynomial passes through (2, 9), we know:

$$
p(2)=9
$$

Substitute x = 2:

$$
a(2)^2+b(2)+c=9
$$

Simplify:

$$
4a+2b+c=9
$$

Therefore:

$$
\boxed{4a+2b+c=9}
$$

Since c = 1:

$$
4a+2b+1=9
$$

Subtract 1:

$$
\boxed{4a+2b=8}
$$

## Step 5: Construct the Linear System

Using the three points, we obtained:

$$
\begin{cases}
c=1\\
a+b+c=3\\
4a+2b+c=9
\end{cases}
$$

Reordering the equations in terms of a, b, and c:

$$
\boxed{
\begin{cases}
a+b+c=3\\
4a+2b+c=9\\
c=1
\end{cases}
}
$$

This is a system of three linear equations with three unknowns.

Although the original polynomial is quadratic in x, the equations are linear in the unknown coefficients a, b, and c.

## Step 6: Write the System in Matrix Form

We can express the system as:

$$
A\mathbf{u}=d
$$

where:

$$
A=
\begin{pmatrix}
1&1&1\\
4&2&1\\
0&0&1
\end{pmatrix}
$$

The vector of unknown coefficients is:

$$
\mathbf{u}=
\begin{pmatrix}
a\\
b\\
c
\end{pmatrix}
$$

The right-hand side vector is:

$$
d=
\begin{pmatrix}
3\\
9\\
1
\end{pmatrix}
$$

Therefore:

$$
\begin{pmatrix}
1&1&1\\
4&2&1\\
0&0&1
\end{pmatrix}
\begin{pmatrix}
a\\
b\\
c
\end{pmatrix}
=
\begin{pmatrix}
3\\
9\\
1
\end{pmatrix}
$$

## Step 7: Construct the Augmented Matrix

The augmented matrix is:

$$
[A|d]=
\left[
\begin{array}{ccc|c}
1&1&1&3\\
4&2&1&9\\
0&0&1&1
\end{array}
\right]
$$

We will now solve the system using Gaussian elimination.

## Step 8: Eliminate the First Entry of Row 2

The first pivot is the 1 in the first row.

To eliminate the 4 below it, apply:

$$
R_2\rightarrow R_2-4R_1
$$

Calculate the new second row:

$$
(4,2,1,9)-4(1,1,1,3)
$$

$$
=(4-4,\ 2-4,\ 1-4,\ 9-12)
$$

$$
=(0,-2,-3,-3)
$$

Therefore, the augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1&1&1&3\\
0&-2&-3&-3\\
0&0&1&1
\end{array}
\right]
$$

This matrix is already in row echelon form.

## Step 9: Normalize the Second Pivot

The second pivot is -2.

Divide the second row by -2:

$$
R_2\rightarrow-\frac12R_2
$$

We obtain:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&1&1&3\\
0&1&\frac32&\frac32\\
0&0&1&1
\end{array}
\right]
}
$$

We can now solve the system using back substitution.

## Step 10: Solve for c

The third row represents:

$$
c=1
$$

Therefore:

$$
\boxed{c=1}
$$

## Step 11: Solve for b

The second row represents:

$$
b+\frac32c=\frac32
$$

Substitute c = 1:

$$
b+\frac32(1)=\frac32
$$

Subtract $\frac32$ from both sides:

$$
b=\frac32-\frac32
$$

Therefore:

$$
\boxed{b=0}
$$

## Step 12: Solve for a

The first row represents:

$$
a+b+c=3
$$

Substitute:

$$
b=0,\qquad c=1
$$

We obtain:

$$
a+0+1=3
$$

Subtract 1:

$$
a=3-1
$$

Therefore:

$$
\boxed{a=2}
$$

## Step 13: Write the Coefficient Vector

We have found:

$$
a=2
$$

$$
b=0
$$

$$
c=1
$$

Therefore, the coefficient vector is:

$$
\boxed{
\begin{pmatrix}
a\\
b\\
c
\end{pmatrix}
=
\begin{pmatrix}
2\\
0\\
1
\end{pmatrix}
}
$$

## Step 14: Construct the Polynomial

Recall the general form:

$$
p(x)=ax^2+bx+c
$$

Substitute the calculated coefficients:

$$
p(x)=2x^2+0x+1
$$

Simplify:

$$
\boxed{p(x)=2x^2+1}
$$

This is our quadratic polynomial.

Since:

$$
a=2\neq0
$$

the resulting polynomial is genuinely quadratic.

## Step 15: Verify the First Point (0, 1)

We must verify:

$$
p(0)=1
$$

Using:

$$
p(x)=2x^2+1
$$

Substitute x = 0:

$$
p(0)=2(0)^2+1
$$

$$
p(0)=0+1
$$

$$
\boxed{p(0)=1}
$$

Therefore, the polynomial passes through:

$$
\boxed{(0,1)}
$$

The first point is verified.

## Step 16: Verify the Second Point (1, 3)

We must verify:

$$
p(1)=3
$$

Substitute x = 1:

$$
p(1)=2(1)^2+1
$$

$$
p(1)=2+1
$$

$$
\boxed{p(1)=3}
$$

Therefore, the polynomial passes through:

$$
\boxed{(1,3)}
$$

The second point is verified.

## Step 17: Verify the Third Point (2, 9)

We must verify:

$$
p(2)=9
$$

Substitute x = 2:

$$
p(2)=2(2)^2+1
$$

$$
p(2)=2(4)+1
$$

$$
p(2)=8+1
$$

$$
\boxed{p(2)=9}
$$

Therefore, the polynomial passes through:

$$
\boxed{(2,9)}
$$

The third point is verified.

## Step 18: Summarize the Verification

| Given Point | Calculated Value | Result |
|---|---|---|
| (0, 1) | p(0) = 1 | Correct |
| (1, 3) | p(1) = 3 | Correct |
| (2, 9) | p(2) = 9 | Correct |

All three given points satisfy the polynomial.

Therefore, our result is correct.

## Step 19: Explain Why the Polynomial Is Unique

The coefficient matrix of our linear system is:

$$
A=
\begin{pmatrix}
1&1&1\\
4&2&1\\
0&0&1
\end{pmatrix}
$$

We can calculate its determinant by expanding along the third row:

$$
\det(A)=
1\cdot
\begin{vmatrix}
1&1\\
4&2
\end{vmatrix}
$$

Calculate the 2x2 determinant:

$$
\det(A)=1(2-4)
$$

$$
\boxed{\det(A)=-2}
$$

Since:

$$
\det(A)\neq0
$$

the coefficient matrix is invertible.

Therefore, the linear system has exactly one solution for the coefficients a, b, and c.

This means there is exactly one polynomial of degree at most 2 that passes through all three given points.

Since the quadratic coefficient is nonzero, that polynomial has degree exactly 2.

Thus:

$$
\boxed{p(x)=2x^2+1}
$$

is the unique quadratic polynomial passing through the three given points.

## Conclusion

We were asked to find a quadratic polynomial:

$$
p(x)=ax^2+bx+c
$$

passing through:

$$
(0,1),\qquad(1,3),\qquad(2,9)
$$

Using the three points, we constructed the system:

$$
\begin{cases}
a+b+c=3\\
4a+2b+c=9\\
c=1
\end{cases}
$$

We solved the system using Gaussian elimination and obtained:

$$
\boxed{a=2,\qquad b=0,\qquad c=1}
$$

Therefore, the required polynomial is:

$$
\boxed{p(x)=2x^2+1}
$$

We verified all three points:

$$
p(0)=1
$$

$$
p(1)=3
$$

$$
p(2)=9
$$

The determinant of the coefficient matrix is:

$$
\det(A)=-2\neq0
$$

Therefore, the polynomial is uniquely determined.

Final answer:

$$
\boxed{p(x)=2x^2+1}
$$
