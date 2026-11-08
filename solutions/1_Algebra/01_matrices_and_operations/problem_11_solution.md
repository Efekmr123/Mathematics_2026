# Exercise 11 Solution: Block Matrix Multiplication

## 1. Result
- Block multiplication formula:
  $$M N = \begin{pmatrix} A E + B G & A F + B H \\ C E + D G & C F + D H \end{pmatrix}$$
- Numerical result:
  $$M N = \begin{pmatrix} 1 & 0 & 3 & 4 \\ 0 & 1 & 7 & 10 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$$

## 2. Main Steps
Given block matrices:
$$M = \begin{pmatrix} A & B \\ C & D \end{pmatrix}, \quad N = \begin{pmatrix} E & F \\ G & H \end{pmatrix}$$

Where:
$$A = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2, \quad B = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}$$
$$C = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = 0_2, \quad D = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2$$
$$E = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2, \quad F = \begin{pmatrix} 2 & 2 \\ 4 & 6 \end{pmatrix}$$
$$G = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = 0_2, \quad H = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2$$

1. **Compute top-left block ($A E + B G$)**:
   $$A E + B G = I_2 I_2 + B 0_2 = I_2 = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$

2. **Compute top-right block ($A F + B H$)**:
   $$A F + B H = I_2 F + B I_2 = F + B = \begin{pmatrix} 2 & 2 \\ 4 & 6 \end{pmatrix} + \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} = \begin{pmatrix} 3 & 4 \\ 7 & 10 \end{pmatrix}$$

3. **Compute bottom-left block ($C E + D G$)**:
   $$C E + D G = 0_2 I_2 + I_2 0_2 = 0_2 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$$

4. **Compute bottom-right block ($C F + D H$)**:
   $$C F + D H = 0_2 F + I_2 I_2 = I_2 = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$

5. **Assemble the block product**:
   $$M N = \begin{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} & \begin{pmatrix} 3 & 4 \\ 7 & 10 \end{pmatrix} \\ \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} & \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \end{pmatrix} = \begin{pmatrix} 1 & 0 & 3 & 4 \\ 0 & 1 & 7 & 10 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$$

## 3. Explanation
Block matrix multiplication works identically to ordinary matrix multiplication, treating submatrices as entries, provided that the block dimensions are compatible for multiplication at each step.

## 4. Verification
Standard $4 \times 4$ matrix multiplication yields the exact same matrix $\begin{pmatrix} 1 & 0 & 3 & 4 \\ 0 & 1 & 7 & 10 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix} \quad \checkmark$.
