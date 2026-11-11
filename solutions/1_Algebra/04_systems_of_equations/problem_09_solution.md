
# Exercise 9: A System from a Sum Condition

## Given System of Equations

We are given the following system:

$$
\begin{cases}
x+y=10\\
2x+5y=32
\end{cases}
$$

Our goals are to:

1. Find the values of x and y.
2. Solve the system using Gaussian elimination.
3. Verify the solution in both original equations.
4. Explain geometrically why the solution is unique.

## Step 1: Interpret the Given Conditions

The first equation is:

$$
x+y=10
$$

This means that the sum of the two unknown numbers is 10.

The second equation is:

$$
2x+5y=32
$$

This gives an additional linear condition on the same two numbers.

We must find a pair $(x,y)$ satisfying both conditions simultaneously.

## Step 2: Write the System in Matrix Form

The system can be written as:

$$
A\mathbf{x}=b
$$

where the coefficient matrix is:

$$
A=
\begin{pmatrix}
1&1\\
2&5
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
10\\
32
\end{pmatrix}
$$

Therefore:

$$
\begin{pmatrix}
1&1\\
2&5
\end{pmatrix}
\begin{pmatrix}
x\\
y
\end{pmatrix}
=
\begin{pmatrix}
10\\
32
\end{pmatrix}
$$

## Step 3: Construct the Augmented Matrix

The augmented matrix is:

$$
[A|b]=
\left[
\begin{array}{cc|c}
1&1&10\\
2&5&32
\end{array}
\right]
$$

We will use Gaussian elimination to solve the system.

## Step 4: Eliminate the First Entry of Row 2

The first pivot is the 1 in the first row.

To eliminate the 2 below this pivot, apply:

$$
R_2\rightarrow R_2-2R_1
$$

Calculate the new second row:

$$
(2,5,32)-2(1,1,10)
$$

$$
=(2-2,\ 5-2,\ 32-20)
$$

$$
=(0,3,12)
$$

Therefore, the augmented matrix becomes:

$$
\boxed{
\left[
\begin{array}{cc|c}
1&1&10\\
0&3&12
\end{array}
\right]
}
$$

This matrix is in row echelon form.

## Step 5: Solve for y

The second row represents:

$$
3y=12
$$

Divide both sides by 3:

$$
y=\frac{12}{3}
$$

Therefore:

$$
\boxed{y=4}
$$

## Step 6: Solve for x Using Back Substitution

The first row represents:

$$
x+y=10
$$

Substitute:

$$
y=4
$$

We obtain:

$$
x+4=10
$$

Subtract 4 from both sides:

$$
x=10-4
$$

Therefore:

$$
\boxed{x=6}
$$

## Step 7: Write the Solution

We have obtained:

$$
x=6,\qquad y=4
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
6\\
4
\end{pmatrix}
}
$$

Therefore, the solution is:

$$
\boxed{(x,y)=(6,4)}
$$

## Step 8: Verify the First Equation

The first equation is:

$$
x+y=10
$$

Substitute the calculated values:

$$
6+4=10
$$

$$
10=10
$$

The first equation is satisfied.

## Step 9: Verify the Second Equation

The second equation is:

$$
2x+5y=32
$$

Substitute:

$$
2(6)+5(4)=32
$$

Simplify:

$$
12+20=32
$$

$$
32=32
$$

The second equation is satisfied.

Therefore, the pair $(6,4)$ satisfies both original equations.

## Step 10: Express Both Equations as Straight Lines

To explain the result geometrically, we rewrite both equations in slope-intercept form:

$$
y=mx+c
$$

where m is the slope and c is the y-intercept.

### First Line

The first equation is:

$$
x+y=10
$$

Solve for y:

$$
y=10-x
$$

Therefore:

$$
\boxed{y=-x+10}
$$

The slope is:

$$
m_1=-1
$$

The y-intercept is:

$$
c_1=10
$$

### Second Line

The second equation is:

$$
2x+5y=32
$$

Subtract 2x:

$$
5y=32-2x
$$

Divide by 5:

$$
y=\frac{32}{5}-\frac25x
$$

Therefore:

$$
\boxed{y=-\frac25x+\frac{32}{5}}
$$

The slope is:

$$
m_2=-\frac25
$$

The y-intercept is:

$$
c_2=\frac{32}{5}
$$

## Step 11: Explain Why the Lines Intersect at Exactly One Point

The slopes of the two lines are:

$$
m_1=-1
$$

and:

$$
m_2=-\frac25
$$

Since:

$$
-1\neq-\frac25
$$

the two lines have different slopes.

Therefore, they are not parallel.

Two distinct straight lines in a plane with different slopes intersect at exactly one point.

The intersection point must satisfy both equations simultaneously.

We already calculated that point:

$$
\boxed{(6,4)}
$$

To confirm geometrically, substitute x = 6 into both line equations.

**First line:**

$$
y=-6+10=4
$$

**Second line:**

$$
y=-\frac25(6)+\frac{32}{5}
$$

$$
y=-\frac{12}{5}+\frac{32}{5}
$$

$$
y=\frac{20}{5}=4
$$

Both lines pass through:

$$
\boxed{(6,4)}
$$

Thus, the point $(6,4)$ is their unique intersection point.

## Step 12: Confirm Uniqueness Using the Determinant

We can also confirm that the system has exactly one solution by examining the coefficient matrix.

Recall:

$$
A=
\begin{pmatrix}
1&1\\
2&5
\end{pmatrix}
$$

For a 2x2 matrix:

$$
\det(A)=ad-bc
$$

Therefore:

$$
\det(A)=1(5)-1(2)
$$

$$
\det(A)=5-2
$$

$$
\boxed{\det(A)=3}
$$

Since:

$$
\det(A)\neq0
$$

the coefficient matrix is invertible.

Therefore, the system has exactly one solution.

This agrees with the geometric interpretation.

## Step 13: Interpret the Result

The first condition requires:

$$
x+y=10
$$

The second condition requires:

$$
2x+5y=32
$$

The pair:

$$
(x,y)=(6,4)
$$

satisfies both conditions.

The first condition alone allows infinitely many pairs of numbers.

For example:

$$
(10,0),\quad (8,2),\quad (6,4)
$$

all satisfy:

$$
x+y=10
$$

However, the second condition restricts the possible values.

Only the pair $(6,4)$ satisfies both conditions simultaneously.

This explains why the system has a unique solution.

## Conclusion

We solved the system:

$$
\begin{cases}
x+y=10\\
2x+5y=32
\end{cases}
$$

using Gaussian elimination.

The row echelon form is:

$$
\left[
\begin{array}{cc|c}
1&1&10\\
0&3&12
\end{array}
\right]
$$

Using back substitution, we obtained:

$$
\boxed{x=6,\qquad y=4}
$$

The solution is:

$$
\boxed{(x,y)=(6,4)}
$$

We verified both original equations:

$$
6+4=10
$$

$$
2(6)+5(4)=32
$$

Geometrically, the equations represent two straight lines:

$$
y=-x+10
$$

and:

$$
y=-\frac25x+\frac{32}{5}
$$

Since their slopes are different, the lines intersect at exactly one point.

That point is:

$$
\boxed{(6,4)}
$$

Additionally, the determinant of the coefficient matrix is:

$$
\det(A)=3\neq0
$$

Therefore, the system has exactly one solution.
