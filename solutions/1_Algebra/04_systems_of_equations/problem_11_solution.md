
# Exercise 11: A Parameter in a System of Three Equations

## Given System of Equations

We are given the following system:

$$
\begin{cases}
x+y+z=1\\
x+ty+z=2\\
x+y+tz=3
\end{cases}
$$

where $t\in\mathbb{R}$ is a parameter.

Our goals are to:

1. Analyze the system using Gaussian elimination.
2. Determine the values of t for which the system has exactly one solution.
3. Determine the values of t for which the system has no solution.
4. Investigate whether infinitely many solutions are possible.
5. Find the solution when it exists.
6. Verify the solution by substituting it into all three original equations.

## Step 1: Write the System in Matrix Form

The system can be expressed as:

$$
A\mathbf{u}=b
$$

where the coefficient matrix is:

$$
A=
\begin{pmatrix}
1&1&1\\
1&t&1\\
1&1&t
\end{pmatrix}
$$

The vector of unknowns is:

$$
\mathbf{u}=
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}
$$

The right-hand side vector is:

$$
b=
\begin{pmatrix}
1\\
2\\
3
\end{pmatrix}
$$

Therefore:

$$
\begin{pmatrix}
1&1&1\\
1&t&1\\
1&1&t
\end{pmatrix}
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
$$

## Step 2: Construct the Augmented Matrix

The augmented matrix is:

$$
[A|b]=
\left[
\begin{array}{ccc|c}
1&1&1&1\\
1&t&1&2\\
1&1&t&3
\end{array}
\right]
$$

We will apply Gaussian elimination to identify the possible solution types.

## Step 3: Eliminate the First Entry of Row 2

The first pivot is the 1 in the first row and first column.

Apply:

$$
R_2\rightarrow R_2-R_1
$$

Calculate the new second row:

$$
(1,t,1,2)-(1,1,1,1)
$$

$$
=(0,t-1,0,1)
$$

Therefore, the augmented matrix becomes:

$$
\left[
\begin{array}{ccc|c}
1&1&1&1\\
0&t-1&0&1\\
1&1&t&3
\end{array}
\right]
$$

## Step 4: Eliminate the First Entry of Row 3

Apply:

$$
R_3\rightarrow R_3-R_1
$$

Calculate the new third row:

$$
(1,1,t,3)-(1,1,1,1)
$$

$$
=(0,0,t-1,2)
$$

Therefore, the augmented matrix becomes:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&1&1&1\\
0&t-1&0&1\\
0&0&t-1&2
\end{array}
\right]
}
$$

The system is now in a form that allows us to analyze the parameter.

The corresponding equations are:

$$
\begin{cases}
x+y+z=1\\
(t-1)y=1\\
(t-1)z=2
\end{cases}
$$

The solution type depends on whether $t-1$ is zero.

## Step 5: Case 1 — When t Is Not Equal to 1

Consider:

$$
t\neq1
$$

Then:

$$
t-1\neq0
$$

Therefore, we can divide by $t-1$.

The second and third rows both contain nonzero pivots.

Together with the first pivot, this gives three pivot variables and no free variables.

The system has exactly one solution.

### Step 5.1: Solve for y

The second equation is:

$$
(t-1)y=1
$$

Divide by $t-1$:

$$
\boxed{y=\frac{1}{t-1}}
$$

This expression is valid only when:

$$
t\neq1
$$

### Step 5.2: Solve for z

The third equation is:

$$
(t-1)z=2
$$

Divide by $t-1$:

$$
\boxed{z=\frac{2}{t-1}}
$$

### Step 5.3: Solve for x

The first equation is:

$$
x+y+z=1
$$

Substitute the expressions for y and z:

$$
x+\frac{1}{t-1}+\frac{2}{t-1}=1
$$

Combine the fractions:

$$
x+\frac{3}{t-1}=1
$$

Subtract the fraction:

$$
x=1-\frac{3}{t-1}
$$

Express 1 using the common denominator:

$$
x=\frac{t-1}{t-1}-\frac{3}{t-1}
$$

Simplify:

$$
\boxed{x=\frac{t-4}{t-1}}
$$

### Step 5.4: Write the General Solution

For every:

$$
t\neq1
$$

the system has the unique solution:

$$
\boxed{
\begin{cases}
x=\frac{t-4}{t-1}\\
y=\frac{1}{t-1}\\
z=\frac{2}{t-1}
\end{cases}
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
\frac{1}{t-1}
\begin{pmatrix}
t-4\\
1\\
2
\end{pmatrix},
\qquad t\neq1
}
$$

## Step 6: Verify the Solution for t Not Equal to 1

We will substitute the solution into all three original equations.

Recall:

$$
x=\frac{t-4}{t-1}
$$

$$
y=\frac{1}{t-1}
$$

$$
z=\frac{2}{t-1}
$$

### Verification of the First Equation

The first equation is:

$$
x+y+z=1
$$

Substitute:

$$
\frac{t-4}{t-1}
+
\frac{1}{t-1}
+
\frac{2}{t-1}
$$

Combine the numerators:

$$
=\frac{t-4+1+2}{t-1}
$$

$$
=\frac{t-1}{t-1}
$$

Since $t\neq1$:

$$
\boxed{1=1}
$$

The first equation is satisfied.

### Verification of the Second Equation

The second equation is:

$$
x+ty+z=2
$$

Substitute:

$$
\frac{t-4}{t-1}
+
t\left(\frac{1}{t-1}\right)
+
\frac{2}{t-1}
$$

Combine the numerators:

$$
=\frac{t-4+t+2}{t-1}
$$

Simplify:

$$
=\frac{2t-2}{t-1}
$$

Factor out 2:

$$
=\frac{2(t-1)}{t-1}
$$

Since $t\neq1$:

$$
\boxed{2=2}
$$

The second equation is satisfied.

### Verification of the Third Equation

The third equation is:

$$
x+y+tz=3
$$

Substitute:

$$
\frac{t-4}{t-1}
+
\frac{1}{t-1}
+
t\left(\frac{2}{t-1}\right)
$$

Combine the numerators:

$$
=\frac{t-4+1+2t}{t-1}
$$

Simplify:

$$
=\frac{3t-3}{t-1}
$$

Factor out 3:

$$
=\frac{3(t-1)}{t-1}
$$

Since $t\neq1$:

$$
\boxed{3=3}
$$

The third equation is satisfied.

Therefore, the unique solution is valid for every real parameter value except t = 1.

## Step 7: Case 2 — When t = 1

Now consider:

$$
t=1
$$

Substitute this value into the row echelon matrix:

$$
\left[
\begin{array}{ccc|c}
1&1&1&1\\
0&t-1&0&1\\
0&0&t-1&2
\end{array}
\right]
$$

Since:

$$
t-1=0
$$

we obtain:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&1&1&1\\
0&0&0&1\\
0&0&0&2
\end{array}
\right]
}
$$

The second row represents:

$$
0x+0y+0z=1
$$

Therefore:

$$
\boxed{0=1}
$$

This is a contradiction.

The third row represents:

$$
0x+0y+0z=2
$$

Therefore:

$$
\boxed{0=2}
$$

This is also a contradiction.

Thus, the system is inconsistent when t = 1.

Therefore:

$$
\boxed{t=1\Rightarrow\text{No solution}}
$$

## Step 8: Verify the Inconsistency Directly

We can also substitute t = 1 into the original system:

$$
\begin{cases}
x+y+z=1\\
x+1y+z=2\\
x+y+1z=3
\end{cases}
$$

Simplify:

$$
\begin{cases}
x+y+z=1\\
x+y+z=2\\
x+y+z=3
\end{cases}
$$

The same expression cannot simultaneously equal 1, 2, and 3.

Therefore, there is no triple $(x,y,z)$ satisfying all three equations.

This confirms the contradiction found using Gaussian elimination.

## Step 9: Can the System Have Infinitely Many Solutions?

A system of linear equations has infinitely many solutions when it is consistent and contains at least one free variable.

We examine the two possible parameter cases.

### When t Is Not Equal to 1

The row echelon matrix is:

$$
\left[
\begin{array}{ccc|c}
1&1&1&1\\
0&t-1&0&1\\
0&0&t-1&2
\end{array}
\right]
$$

Since:

$$
t-1\neq0
$$

all three coefficient columns contain pivots.

Therefore:

- There are three unknowns.
- There are three pivot variables.
- There are zero free variables.
- There is no contradiction.

Thus, the system has exactly one solution.

It cannot have infinitely many solutions.

### When t = 1

The augmented matrix contains contradictory rows:

$$
0=1
$$

and:

$$
0=2
$$

Therefore, the system is inconsistent.

An inconsistent system cannot have infinitely many solutions.

### Final Conclusion About Infinite Solutions

For t not equal to 1, the system has exactly one solution.

For t equal to 1, the system has no solution.

Therefore:

$$
\boxed{\text{There is no real value of }t\text{ for which infinitely many solutions exist.}}
$$

## Step 10: Confirm the Result Using the Determinant

The coefficient matrix is:

$$
A=
\begin{pmatrix}
1&1&1\\
1&t&1\\
1&1&t
\end{pmatrix}
$$

Apply the determinant-preserving row operations:

$$
R_2\rightarrow R_2-R_1
$$

$$
R_3\rightarrow R_3-R_1
$$

The resulting matrix is:

$$
\begin{pmatrix}
1&1&1\\
0&t-1&0\\
0&0&t-1
\end{pmatrix}
$$

This is an upper triangular matrix.

The determinant of an upper triangular matrix equals the product of its diagonal entries.

Therefore:

$$
\det(A)=1(t-1)(t-1)
$$

Thus:

$$
\boxed{\det(A)=(t-1)^2}
$$

### When t Is Not Equal to 1

$$
(t-1)^2\neq0
$$

Therefore, A is invertible.

An invertible coefficient matrix guarantees exactly one solution.

### When t = 1

$$
\det(A)=0
$$

The matrix is singular.

A zero determinant alone does not determine whether the system has no solution or infinitely many solutions.

However, Gaussian elimination already showed that the augmented matrix contains contradictions.

Therefore, the system has no solution when t = 1.

The determinant analysis agrees with our earlier classification.

## Step 11: Check a Numerical Example

To illustrate the unique-solution case, choose:

$$
t=2
$$

The solution formulas become:

$$
x=\frac{2-4}{2-1}=-2
$$

$$
y=\frac{1}{2-1}=1
$$

$$
z=\frac{2}{2-1}=2
$$

Therefore:

$$
\boxed{(x,y,z)=(-2,1,2)}
$$

The original system for t = 2 is:

$$
\begin{cases}
x+y+z=1\\
x+2y+z=2\\
x+y+2z=3
\end{cases}
$$

Verify the first equation:

$$
-2+1+2=1
$$

Verify the second equation:

$$
-2+2(1)+2=2
$$

Verify the third equation:

$$
-2+1+2(2)=3
$$

All three equations are satisfied.

This example confirms the general solution formula.

## Step 12: Summarize the Parameter Cases

| Parameter Value | Solution Type | Explanation |
|---|---|---|
| t != 1 | Exactly one solution | Three nonzero pivots; coefficient matrix is invertible |
| t = 1 | No solution | Gaussian elimination produces contradictions |
| No value of t | Infinitely many solutions | The system is either uniquely solvable or inconsistent |

The complete classification is:

$$
\boxed{
\begin{cases}
t\neq1 & \text{Exactly one solution}\\
t=1 & \text{No solution}
\end{cases}
}
$$

Infinitely many solutions never occur.

## Conclusion

We analyzed the parameter-dependent system:

$$
\begin{cases}
x+y+z=1\\
x+ty+z=2\\
x+y+tz=3
\end{cases}
$$

Using Gaussian elimination, we obtained:

$$
\boxed{
\left[
\begin{array}{ccc|c}
1&1&1&1\\
0&t-1&0&1\\
0&0&t-1&2
\end{array}
\right]
}
$$

For t not equal to 1, all three pivots are nonzero and the system has exactly one solution:

$$
\boxed{
\begin{cases}
x=\frac{t-4}{t-1}\\
y=\frac{1}{t-1}\\
z=\frac{2}{t-1}
\end{cases}
\qquad t\neq1
}
$$

We verified this solution in all three original equations.

For t = 1, Gaussian elimination produces the contradictions:

$$
0=1
$$

and:

$$
0=2
$$

Therefore, the system has no solution.

The determinant is:

$$
\boxed{\det(A)=(t-1)^2}
$$

This confirms that the coefficient matrix is invertible exactly when t is not equal to 1.

The final classification is:

$$
\boxed{
\begin{cases}
t\neq1 & \text{Exactly one solution}\\
t=1 & \text{No solution}
\end{cases}
}
$$

There is no value of t for which the system has infinitely many solutions.
