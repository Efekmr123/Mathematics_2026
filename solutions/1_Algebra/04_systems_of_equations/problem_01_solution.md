
# Exercise 1: From a System to a Matrix

## Given System of Equations

We are given the following system of linear equations:

$$
\begin{cases}
2x-y+z=4 \\
x+3y-2z=1 \\
3x+y+z=7
\end{cases}
$$

Our goal is to write this system in matrix form:

$$
Ax=b
$$

We also need to identify:

1. The coefficient matrix A.
2. The vector of unknowns x.
3. The right-hand side vector b.
4. How each row of the matrix corresponds to one equation.

## Step 1: Understand the Matrix Form

A system of linear equations can be represented as:

$$
Ax=b
$$

where:

- A is the coefficient matrix containing the coefficients of the unknowns.
- x is the column vector containing the unknown variables.
- b is the right-hand side column vector containing the constants.

For our system, there are three equations and three unknowns.

Therefore, the coefficient matrix A will have 3 rows and 3 columns.

The vectors x and b will each have 3 rows and 1 column.

## Step 2: Identify the Coefficients

We examine each equation separately.

### First Equation

$$
2x-y+z=4
$$

The coefficients of x, y, and z are:

$$
2,\quad -1,\quad 1
$$

The constant on the right-hand side is:

$$
4
$$

Therefore, the first row of the coefficient matrix is:

$$
\begin{pmatrix}
2 & -1 & 1
\end{pmatrix}
$$

### Second Equation

$$
x+3y-2z=1
$$

The coefficients of x, y, and z are:

$$
1,\quad 3,\quad -2
$$

The constant on the right-hand side is:

$$
1
$$

Therefore, the second row of the coefficient matrix is:

$$
\begin{pmatrix}
1 & 3 & -2
\end{pmatrix}
$$

### Third Equation

$$
3x+y+z=7
$$

The coefficients of x, y, and z are:

$$
3,\quad 1,\quad 1
$$

The constant on the right-hand side is:

$$
7
$$

Therefore, the third row of the coefficient matrix is:

$$
\begin{pmatrix}
3 & 1 & 1
\end{pmatrix}
$$

## Step 3: Construct the Coefficient Matrix A

We place the coefficients of each equation into the corresponding row.

The first column contains the coefficients of x.

The second column contains the coefficients of y.

The third column contains the coefficients of z.

Therefore:

$$
\boxed{
A=
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
}
$$

This is a 3x3 coefficient matrix.

## Step 4: Construct the Vector of Unknowns

The unknown variables are:

$$
x,\quad y,\quad z
$$

We arrange them into a column vector:

$$
\boxed{
\mathbf{x}=
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
}
$$

The order of the variables must match the order of the columns in the coefficient matrix.

## Step 5: Construct the Right-Hand Side Vector

The constants on the right-hand sides of the equations are:

$$
4,\quad 1,\quad 7
$$

We place these constants into a column vector:

$$
\boxed{
b=
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix}
}
$$

Each entry corresponds to the constant in the same row of the original system.

## Step 6: Write the Complete Matrix Equation

Combining the coefficient matrix, the vector of unknowns, and the right-hand side vector gives:

$$
\boxed{
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
=
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix}
}
$$

This is the required matrix representation:

$$
\boxed{A\mathbf{x}=b}
$$

## Step 7: Verify the Matrix Representation

To verify our result, we multiply the coefficient matrix by the vector of unknowns:

$$
A\mathbf{x}=
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
$$

Multiplying each row by the column vector:

$$
A\mathbf{x}=
\begin{pmatrix}
2x+(-1)y+1z \\
1x+3y+(-2)z \\
3x+1y+1z
\end{pmatrix}
$$

Simplifying:

$$
A\mathbf{x}=
\begin{pmatrix}
2x-y+z \\
x+3y-2z \\
3x+y+z
\end{pmatrix}
$$

Since:

$$
A\mathbf{x}=b
$$

we obtain:

$$
\begin{pmatrix}
2x-y+z \\
x+3y-2z \\
3x+y+z
\end{pmatrix}
=
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix}
$$

This gives the original equations:

$$
\begin{cases}
2x-y+z=4 \\
x+3y-2z=1 \\
3x+y+z=7
\end{cases}
$$

Therefore, our matrix representation is correct.

## Step 8: Explain the Relationship Between Rows and Equations

Each row of the coefficient matrix represents exactly one equation.

**Row 1:**

$$
\begin{pmatrix}
2 & -1 & 1
\end{pmatrix}
$$

corresponds to:

$$
2x-y+z=4
$$

**Row 2:**

$$
\begin{pmatrix}
1 & 3 & -2
\end{pmatrix}
$$

corresponds to:

$$
x+3y-2z=1
$$

**Row 3:**

$$
\begin{pmatrix}
3 & 1 & 1
\end{pmatrix}
$$

corresponds to:

$$
3x+y+z=7
$$

The position of each coefficient determines which variable it multiplies.

The corresponding entry of the vector b gives the constant for that equation.

Thus, matrix notation represents the entire system in a compact and organized form.

## Conclusion

The given system:

$$
\begin{cases}
2x-y+z=4 \\
x+3y-2z=1 \\
3x+y+z=7
\end{cases}
$$

can be written in the form:

$$
\boxed{A\mathbf{x}=b}
$$

where the coefficient matrix is:

$$
\boxed{
A=
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
}
$$

the vector of unknowns is:

$$
\boxed{
\mathbf{x}=
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
}
$$

and the right-hand side vector is:

$$
\boxed{
b=
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix}
}
$$

We verified that multiplying A by the unknown vector reproduces all three original equations.

Each row of A corresponds to one equation, and each column corresponds to one unknown variable.

Therefore, the system has been correctly converted into matrix notation.
