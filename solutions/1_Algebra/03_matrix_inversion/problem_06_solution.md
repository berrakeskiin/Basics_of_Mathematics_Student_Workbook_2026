# Exercise 6. Solving a System Using the Inverse

## Problem Statement

Solve $`Ax=b`$, where

```math
A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}5\\7\end{pmatrix},
```

using $`x=A^{-1}b`$. Then substitute the resulting vector back into the equation and check the result.

## Theoretical Background and Concepts

- If $`A`$ is invertible, multiplying $`Ax=b`$ from the left by $`A^{-1}`$ gives $`x=A^{-1}b`$ (the unique solution).
- $`2\times2`$ formula: $`\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1}=\frac1{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}`$.

## Detailed Step-by-Step Solution

```math
\det A=2\cdot3-1\cdot1=5,\qquad A^{-1}=\frac15\begin{pmatrix}3&-1\\-1&2\end{pmatrix}.
```

```math
x=A^{-1}b=\frac15\begin{pmatrix}3\cdot5-1\cdot7\\-1\cdot5+2\cdot7\end{pmatrix}=\frac15\begin{pmatrix}8\\9\end{pmatrix}=\begin{pmatrix}\frac85\\\frac95\end{pmatrix}.
```

## Verification and Consistency Checks

Substitution:

```math
Ax=\begin{pmatrix}2\cdot\frac85+\frac95\\\frac85+3\cdot\frac95\end{pmatrix}=\begin{pmatrix}\frac{16+9}5\\\frac{8+27}5\end{pmatrix}=\begin{pmatrix}5\\7\end{pmatrix}=b.
```

✓
