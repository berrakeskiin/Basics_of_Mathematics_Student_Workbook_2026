# Exercise 14. A System of Equations and the Determinant

## Problem Statement

Consider the system $`Ax=b`$, where

```math
A=\begin{pmatrix}1&2\\k&4\end{pmatrix}.
```

For which values of $`k`$ does the system have exactly one solution for every $`b`$? For the remaining value, give an example of $`b`$ with infinitely many solutions, and an example with no solution.

## Theoretical Background and Concepts

- If $`\det A\neq0`$, then $`A`$ is invertible and $`Ax=b`$ has exactly one solution $`x=A^{-1}b`$ for every $`b`$.
- If $`\det A=0`$, the system has either **no** solution or **infinitely many**, depending on $`b`$.

## Detailed Step-by-Step Solution

```math
\det A=1\cdot4-2\cdot k=4-2k.
```

$`4-2k\neq0\iff k\neq2`$.

**Answer:** for every $`k\neq2`$ the system has exactly one solution for every $`b`$.

**Case $`k=2`$:**

```math
A=\begin{pmatrix}1&2\\2&4\end{pmatrix},\qquad\text{the second equation's left side is 2 times the first one.}
```

- **Infinitely many solutions:** $`b=\begin{pmatrix}1\\2\end{pmatrix}`$. The equations are $`x+2y=1`$ and $`2x+4y=2`$; the second is 2 times the first, so every point of the line $`x+2y=1`$ is a solution, e.g. $`(1,0)`$, $`(-1,1)`$, $`(3,-1)`$.
- **No solution:** $`b=\begin{pmatrix}1\\0\end{pmatrix}`$. The equations $`x+2y=1`$ and $`2x+4y=0`$ give $`x+2y=1`$ and $`x+2y=0`$ at the same time, which is a contradiction ($`1=0`$).

## Verification and Consistency Checks

- Example $`k=0`$: $`\det=4\neq0`$; for $`b=(1,2)^T`$: $`y=\frac12`$, $`x=1-2\cdot\frac12=0`$, a unique solution. ✓
- For $`k=2`$: $`(1,0)`$ satisfies $`1+0=1`$ and $`2+0=2`$ ✓; $`(-1,1)`$ satisfies $`-1+2=1`$ and $`-2+4=2`$ ✓.
