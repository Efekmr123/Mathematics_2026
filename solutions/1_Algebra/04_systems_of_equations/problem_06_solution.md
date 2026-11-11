
# Exercise 6: A System with a Parameter — Which Cases Actually Occur?

## Given System of Equations

We are given the following system:

$$
\begin{cases}
x+y=2\\
ax+ay=4
\end{cases}
$$

where $a$ is a real parameter.

Our goals are to:

1. Analyze the system using Gaussian elimination.
2. Determine for which values of $a$ the system has exactly one solution.
3. Determine for which values of $a$ the system has infinitely many solutions.
4. Determine for which values of $a$ the system has no solution.
5. Explain why some of these possibilities cannot occur.

## Step 1: Write the System in Matrix Form

The system can be expressed as:

$$
A\mathbf{x}=b
$$

where the coefficient matrix is:

$$
A=
\begin{pmatrix}
1&1\\
a&a
\end{pmatrix}
$$

The vector of unknowns is:

$$
\mathbf{x}=
\begin{pmatrix}
x\\
y
\end{pmatrix}
$$

The right-hand side vector is:

$$
b=
\begin{pmatrix}
2\\
4
\end{pmatrix}
$$

Therefore:

$$
\begin{pmatrix}
1&1\\
a&a
\end{pmatrix}
\begin{pmatrix}
x\\
y
\end{pmatrix}
=
\begin{pmatrix}
2\\
4
\end{pmatrix}
$$

## Step 2: Construct the Augmented Matrix

The augmented matrix is:

$$
[A|b]=
\left[
\begin{array}{cc|c}
1&1&2\\
a&a&4
\end{array}
\right]
$$

We will apply Gaussian elimination to determine the possible solution types.

## Step 3: Apply Gaussian Elimination

The first pivot is the 1 in the first row and first column.

To eliminate the coefficient $a$ below this pivot, apply:

$$
R_2\rightarrow R_2-aR_1
$$

Calculate the new second row:

$$
(a,a,4)-a(1,1,2)
$$

$$
=(a-a,\ a-a,\ 4-2a)
$$

$$
=(0,0,4-2a)
$$

Therefore, the augmented matrix becomes:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&2\\
0&0&4-2a
\end{array}
\right]
}
$$

The second row represents:

$$
0x+0y=4-2a
$$

Therefore:

$$
\boxed{0=4-2a}
$$

The consistency of the system depends on the value of $a$.

## Step 4: Case 1 — When a = 2

First, consider:

$$
a=2
$$

Substitute this value into the second row:

$$
4-2a=4-2(2)
$$

$$
=4-4=0
$$

Therefore, the augmented matrix becomes:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&0&0
\end{array}
\right]
$$

The corresponding equations are:

$$
\begin{cases}
x+y=2\\
0=0
\end{cases}
$$

The second equation is always true.

Thus, the system is consistent.

There are two unknowns but only one pivot variable.

Therefore, one variable is free.

### Find the Parametric Solution

From the first equation:

$$
x+y=2
$$

Solve for $x$:

$$
x=2-y
$$

Let:

$$
y=t,\qquad t\in\mathbb{R}
$$

Then:

$$
x=2-t
$$

Therefore, the general solution is:

$$
\boxed{
\begin{cases}
x=2-t\\
y=t
\end{cases}
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

Since $t$ can be any real number, the system has infinitely many solutions.

Therefore:

$$
\boxed{a=2\Rightarrow\text{Infinitely many solutions}}
$$

### Verification

When $a=2$, the original system becomes:

$$
\begin{cases}
x+y=2\\
2x+2y=4
\end{cases}
$$

Substitute:

$$
x=2-t,\qquad y=t
$$

First equation:

$$
(2-t)+t=2
$$

$$
2=2
$$

Second equation:

$$
2(2-t)+2t=4
$$

$$
4-2t+2t=4
$$

$$
4=4
$$

Both equations are satisfied for every real value of $t$.

## Step 5: Case 2 — When a Is Not Equal to 2

Now consider:

$$
a\neq2
$$

From Gaussian elimination, the second row represents:

$$
0=4-2a
$$

Since:

$$
a\neq2
$$

we have:

$$
4-2a\neq0
$$

Therefore, the equation becomes:

$$
0=\text{a nonzero number}
$$

This is impossible.

The augmented matrix contains a contradictory row:

$$
\left[
\begin{array}{cc|c}
0&0&4-2a
\end{array}
\right]
$$

where:

$$
4-2a\neq0
$$

Consequently, the system is inconsistent.

Thus:

$$
\boxed{a\neq2\Rightarrow\text{No solution}}
$$

### Example: a = 1

For $a=1$, the system becomes:

$$
\begin{cases}
x+y=2\\
x+y=4
\end{cases}
$$

The same expression cannot be equal to both 2 and 4.

Therefore, no solution exists.

### Example: a = 0

For $a=0$, the system becomes:

$$
\begin{cases}
x+y=2\\
0x+0y=4
\end{cases}
$$

The second equation simplifies to:

$$
0=4
$$

This is impossible.

Therefore, the system also has no solution when $a=0$.

## Step 6: Can the System Have Exactly One Solution?

We now investigate whether any value of $a$ can produce exactly one solution.

The coefficient matrix is:

$$
A=
\begin{pmatrix}
1&1\\
a&a
\end{pmatrix}
$$

Calculate its determinant:

$$
\det(A)=1(a)-1(a)
$$

$$
\det(A)=a-a
$$

Therefore:

$$
\boxed{\det(A)=0}
$$

This is true for every real value of $a$.

Consequently, the coefficient matrix is singular for every value of the parameter.

A square system with a unique solution must have an invertible coefficient matrix.

Since the determinant is always zero, this system cannot have exactly one solution.

We can also see this directly from Gaussian elimination:

$$
\left[
\begin{array}{cc|c}
1&1&2\\
0&0&4-2a
\end{array}
\right]
$$

The coefficient part has only one pivot column.

There is never a second pivot for the second variable.

Therefore:

- If the system is consistent, it has one free variable and infinitely many solutions.
- If the system is inconsistent, it has no solution.

A unique solution is impossible.

Thus:

$$
\boxed{\text{Exactly one solution is impossible for every }a\in\mathbb{R}.}
$$

## Step 7: Interpret the Original Equations

The first equation is:

$$
x+y=2
$$

The second equation is:

$$
ax+ay=4
$$

Factor out $a$:

$$
a(x+y)=4
$$

However, the first equation requires:

$$
x+y=2
$$

Substituting this into the second equation gives:

$$
a(2)=4
$$

Therefore:

$$
2a=4
$$

$$
\boxed{a=2}
$$

This shows that the equations are compatible only when $a=2$.

If $a=2$, the second equation is simply twice the first equation.

If $a\neq2$, the equations impose incompatible conditions.

This agrees with the result obtained using Gaussian elimination.

## Step 8: Geometric Interpretation

The first equation represents the line:

$$
x+y=2
$$

or:

$$
y=-x+2
$$

For $a\neq0$, the second equation can be divided by $a$:

$$
x+y=\frac4a
$$

or:

$$
y=-x+\frac4a
$$

Both lines have slope:

$$
m=-1
$$

If $a=2$, their intercepts are equal:

$$
\frac4a=2
$$

The two lines coincide, producing infinitely many solutions.

If $a\neq0$ and $a\neq2$, their intercepts are different.

The lines are distinct and parallel, producing no solution.

If $a=0$, the second equation becomes:

$$
0=4
$$

which is impossible and does not describe a line.

Therefore, this case also has no solution.

There is no parameter value for which the two equations represent distinct intersecting lines.

Hence, a unique solution never occurs.

## Step 9: Summarize the Three Possible Cases

| Solution Type | Parameter Values | Explanation |
|---|---|---|
| Exactly one solution | None | The coefficient matrix is singular for every a |
| Infinitely many solutions | a = 2 | The equations are equivalent and one variable is free |
| No solution | a != 2 | Gaussian elimination produces a contradiction |

Only two of the three theoretically possible solution types actually occur in this system.

## Conclusion

We analyzed the parameter-dependent system:

$$
\begin{cases}
x+y=2\\
ax+ay=4
\end{cases}
$$

Using Gaussian elimination, we obtained:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&2\\
0&0&4-2a
\end{array}
\right]
}
$$

The system is consistent only when:

$$
4-2a=0
$$

which gives:

$$
a=2
$$

For $a=2$, the system has infinitely many solutions:

$$
\boxed{
(x,y)=(2-t,t),
\qquad t\in\mathbb{R}
}
$$

For $a\neq2$, the system is inconsistent and has no solution.

The coefficient matrix always satisfies:

$$
\det(A)=0
$$

Therefore, the system cannot have exactly one solution for any real value of $a$.

The final classification is:

$$
\boxed{
\begin{cases}
a=2 & \text{Infinitely many solutions}\\
a\neq2 & \text{No solution}
\end{cases}
}
$$

Exactly one solution never occurs.
