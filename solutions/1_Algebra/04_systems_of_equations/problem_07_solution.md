
# Exercise 7: Choosing a Method Deliberately

## Introduction

In this exercise, we compare different approaches to solving linear systems.

The most appropriate method depends on the structure of the coefficient matrix, the number of right-hand sides, and which calculations have already been performed.

We consider three situations:

1. A system with a triangular coefficient matrix.
2. Three systems with the same invertible coefficient matrix A, where the inverse is already known.
3. A single 3x3 system where the inverse is not given and only one solution vector is required.

We will solve the first system completely. For the other two situations, we will describe the most suitable methods without performing unnecessary calculations.

## Case 1: A System with a Triangular Coefficient Matrix

### Given System

We are given:

$$
\begin{cases}
2x-y=3\\
4y=8
\end{cases}
$$

Our goal is to choose the most efficient method and solve the system completely.

### Step 1: Identify the Structure

The coefficient matrix is:

$$
A=
\begin{pmatrix}
2&-1\\
0&4
\end{pmatrix}
$$

The right-hand side vector is:

$$
b=
\begin{pmatrix}
3\\
8
\end{pmatrix}
$$

Therefore, the matrix equation is:

$$
\begin{pmatrix}
2&-1\\
0&4
\end{pmatrix}
\begin{pmatrix}
x\\
y
\end{pmatrix}
=
\begin{pmatrix}
3\\
8
\end{pmatrix}
$$

The coefficient matrix is upper triangular because all entries below the main diagonal are zero.

This structure makes back substitution particularly convenient.

We do not need to calculate the inverse matrix or perform Gaussian elimination because the system is already in triangular form.

### Step 2: Solve for y

The second equation is:

$$
4y=8
$$

Divide both sides by 4:

$$
y=\frac84
$$

Therefore:

$$
\boxed{y=2}
$$

### Step 3: Solve for x Using Back Substitution

The first equation is:

$$
2x-y=3
$$

Substitute:

$$
y=2
$$

We obtain:

$$
2x-2=3
$$

Add 2 to both sides:

$$
2x=5
$$

Divide by 2:

$$
\boxed{x=\frac52}
$$

### Step 4: Write the Solution

The solution is:

$$
\boxed{
x=\frac52,\qquad y=2
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
\frac52\\
2
\end{pmatrix}
}
$$

### Step 5: Verify the Solution

We check both original equations.

**First equation:**

$$
2x-y=3
$$

Substitute:

$$
2\left(\frac52\right)-2=3
$$

$$
5-2=3
$$

$$
3=3
$$

The first equation is satisfied.

**Second equation:**

$$
4y=8
$$

Substitute:

$$
4(2)=8
$$

$$
8=8
$$

The second equation is satisfied.

### Why Back Substitution Is the Best Choice

Back substitution is the most efficient method for this system because:

1. The coefficient matrix is already upper triangular.
2. The second equation contains only one unknown.
3. We can immediately calculate y and substitute it into the first equation.
4. No row operations or inverse matrix calculations are required.

Therefore:

$$
\boxed{\text{Best method: Back substitution}}
$$

## Case 2: Three Systems with the Same Invertible Matrix

### Given Situation

We have three linear systems:

$$
A\mathbf{x}_1=b_1
$$

$$
A\mathbf{x}_2=b_2
$$

$$
A\mathbf{x}_3=b_3
$$

All three systems have the same invertible coefficient matrix A.

We are also told that the inverse matrix $A^{-1}$ is already known.

### Step 1: Choose the Appropriate Method

Since $A^{-1}$ is already available, the inverse matrix method is a convenient choice.

For a system:

$$
A\mathbf{x}=b
$$

we can multiply both sides by $A^{-1}$ on the left:

$$
A^{-1}A\mathbf{x}=A^{-1}b
$$

Since:

$$
A^{-1}A=I
$$

we obtain:

$$
\mathbf{x}=A^{-1}b
$$

### Step 2: Describe the Plan

We apply the known inverse matrix separately to each right-hand side:

$$
\boxed{\mathbf{x}_1=A^{-1}b_1}
$$

$$
\boxed{\mathbf{x}_2=A^{-1}b_2}
$$

$$
\boxed{\mathbf{x}_3=A^{-1}b_3}
$$

Each solution requires only a matrix-vector multiplication.

We do not need to calculate the inverse matrix again.

### Step 3: Identify Reusable Calculations

The coefficient matrix A is the same in all three systems.

Therefore, its inverse is also the same.

The reusable object is:

$$
\boxed{A^{-1}}
$$

Once the inverse is known, it can be applied to each right-hand side.

We may also combine the right-hand sides into a single matrix:

$$
B=
\begin{pmatrix}
|&|&|\\
b_1&b_2&b_3\\
|&|&|
\end{pmatrix}
$$

Then all three solution vectors can be written together:

$$
\boxed{
X=A^{-1}B
}
$$

where:

$$
X=
\begin{pmatrix}
|&|&|\\
\mathbf{x}_1&\mathbf{x}_2&\mathbf{x}_3\\
|&|&|
\end{pmatrix}
$$

This is a compact way to represent the three solutions.

### Why This Method Is Appropriate

The inverse matrix method is convenient here because:

1. All three systems have the same coefficient matrix.
2. The coefficient matrix is invertible.
3. The inverse matrix has already been calculated.
4. There are multiple right-hand sides.
5. The same inverse can be reused for all three systems.

If the inverse were not already known, computing it solely to solve a few systems might not be the most efficient approach.

For example, a single matrix factorization could also be reused across multiple right-hand sides.

However, because the inverse is already available, directly multiplying by it avoids repeating elimination or calculating a new inverse.

Therefore:

$$
\boxed{\text{Best method: Use the known inverse matrix}}
$$

## Case 3: A Single 3x3 System Without a Known Inverse

### Given Situation

We have one linear system:

$$
A\mathbf{x}=b
$$

where A is a 3x3 coefficient matrix.

The inverse matrix is not provided.

Our only goal is to find one solution vector.

### Step 1: Choose the Appropriate Method

For this situation, Gaussian elimination is the most suitable general method.

We do not need to calculate the entire inverse matrix because only one right-hand side is involved.

Instead, we can work directly with the augmented matrix.

### Step 2: Construct the Augmented Matrix

Write:

$$
[A|b]
$$

For a general 3x3 system:

$$
A=
\begin{pmatrix}
a_{11}&a_{12}&a_{13}\\
a_{21}&a_{22}&a_{23}\\
a_{31}&a_{32}&a_{33}
\end{pmatrix}
$$

and:

$$
b=
\begin{pmatrix}
b_1\\
b_2\\
b_3
\end{pmatrix}
$$

The augmented matrix is:

$$
\left[
\begin{array}{ccc|c}
a_{11}&a_{12}&a_{13}&b_1\\
a_{21}&a_{22}&a_{23}&b_2\\
a_{31}&a_{32}&a_{33}&b_3
\end{array}
\right]
$$

### Step 3: Describe the Elimination Process

We would apply elementary row operations to transform the augmented matrix into row echelon form.

The main steps are:

1. Choose a nonzero pivot in the first column, swapping rows if necessary.
2. Eliminate the entries below the first pivot.
3. Choose a nonzero pivot in the second column when possible.
4. Eliminate the entries below the second pivot.
5. Continue until row echelon form is obtained.
6. Examine the resulting rows for contradictions or free variables.
7. If the system has a unique solution, use back substitution to calculate the unknowns.

For a system with three nonzero pivots, the resulting matrix has the general structure:

$$
\left[
\begin{array}{ccc|c}
p_1&*&*&c_1\\
0&p_2&*&c_2\\
0&0&p_3&c_3
\end{array}
\right]
$$

where:

$$
p_1,p_2,p_3\neq0
$$

We can then solve from the last equation upward.

If a contradictory row appears, the system has no solution.

If there are free variables and no contradiction, the system has infinitely many solutions.

### Step 4: Explain Why the Inverse Is Unnecessary

Calculating $A^{-1}$ would require additional work.

For example, Gauss-Jordan inversion begins with:

$$
[A|I]
$$

and transforms it into:

$$
[I|A^{-1}]
$$

This computes the complete inverse matrix.

However, when we only need to solve:

$$
A\mathbf{x}=b
$$

for one right-hand side, we can instead perform elimination directly on:

$$
[A|b]
$$

This avoids calculating all entries of the inverse matrix.

### Why Gaussian Elimination Is the Best Choice

Gaussian elimination is appropriate because:

1. The inverse matrix is not given.
2. Only one right-hand side needs to be processed.
3. The goal is to find a solution vector, not the inverse matrix.
4. Row operations can directly reveal whether the system is consistent.
5. Back substitution gives the solution when a unique solution exists.

Therefore:

$$
\boxed{\text{Best method: Gaussian elimination}}
$$

## Step 4: Compare the Three Situations

| Situation | Recommended Method | Main Reason |
|---|---|---|
| Upper triangular system | Back substitution | The system is already in a form that can be solved from the last equation upward |
| Three systems with the same A and known inverse | Inverse matrix method | The existing inverse can be reused for all right-hand sides |
| One 3x3 system without a known inverse | Gaussian elimination | It solves the system directly without computing the full inverse |

The best method depends on the available information and the structure of the problem.

A method should not be selected only because it is familiar.

Instead, we should consider:

- Whether the coefficient matrix has a special structure.
- Whether the inverse matrix is already known.
- How many right-hand sides must be solved.
- Which calculations can be reused.
- Which calculations are unnecessary for the required result.

## Conclusion

We considered three different situations and selected the most appropriate method for each.

### Case 1: Triangular System

The best method is back substitution.

We solved:

$$
\begin{cases}
2x-y=3\\
4y=8
\end{cases}
$$

and obtained:

$$
\boxed{
(x,y)=\left(\frac52,2\right)
}
$$

The solution was verified in both original equations.

### Case 2: Three Systems with a Known Inverse

The best method is to reuse the known inverse matrix:

$$
\boxed{
\mathbf{x}_i=A^{-1}b_i,
\qquad i=1,2,3
}
$$

The inverse matrix does not need to be calculated again.

### Case 3: One 3x3 System Without a Known Inverse

The best method is Gaussian elimination applied to:

$$
\boxed{[A|b]}
$$

This avoids calculating the full inverse and allows us to analyze the solution directly.

### Final Observation

The choice of method depends on the structure of the coefficient matrix, the number of right-hand sides, and which computations are already available.

Therefore, selecting an efficient method is an important part of solving linear systems.
