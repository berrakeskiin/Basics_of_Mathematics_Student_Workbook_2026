# Exercise 1. From a System to a Matrix

## Problem Statement

Write the system

```math
\begin{cases}2x-y+z=4,\\x+3y-2z=1,\\3x+y+z=7.\end{cases}
```

in the form $`Ax=b`$. Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## Theoretical Background and Concepts

- A linear system with $`m`$ equations and $`n`$ unknowns can be written as $`Ax=b`$, where $`A`$ is the $`m\times n`$ **coefficient matrix**, $`x`$ is the vector of **unknowns**, and $`b`$ is the **right-hand side** vector.
- Row $`i`$ of $`A`$ contains the coefficients of equation $`i`$; the product (row $`i`$)$`\cdot x`$ is the left-hand side of that equation.

## Detailed Step-by-Step Solution

```math
A=\begin{pmatrix}2&-1&1\\1&3&-2\\3&1&1\end{pmatrix},\qquad x=\begin{pmatrix}x\\y\\z\end{pmatrix},\qquad b=\begin{pmatrix}4\\1\\7\end{pmatrix},
```

```math
\begin{pmatrix}2&-1&1\\1&3&-2\\3&1&1\end{pmatrix}\begin{pmatrix}x\\y\\z\end{pmatrix}=\begin{pmatrix}4\\1\\7\end{pmatrix}.
```

**Rows and equations:** the first row $`(2,-1,1)`$ times $`(x,y,z)^T`$ gives $`2x-y+z`$, which must equal $`b_1=4`$ (the first equation). The same holds for rows 2 and 3. Each column of $`A`$ collects the coefficients of one unknown ($`x`$, $`y`$, $`z`$).

## Verification and Consistency Checks

Multiplying back:

```math
Ax=\begin{pmatrix}2x-y+z\\x+3y-2z\\3x+y+z\end{pmatrix},
```

which are exactly the three left-hand sides of the original system. ✓
