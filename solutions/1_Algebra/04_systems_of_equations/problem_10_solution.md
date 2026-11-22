# Exercise 10. A Polynomial Through Three Points

## Problem Statement

Find a polynomial $`p(x)=ax^2+bx+c`$ whose graph passes through $`(0,1)`$, $`(1,3)`$, and $`(2,9)`$. Reduce the problem to a system of equations and check the result by substituting all three points.

## Theoretical Background and Concepts

- "The graph passes through $`(x_0,y_0)`$" means $`p(x_0)=y_0`$.
- Each point gives one **linear** equation in the unknown coefficients $`a,b,c`$. Three points give a $`3\times3`$ linear system.

## Detailed Step-by-Step Solution

```math
\begin{cases}p(0)=c=1,\\p(1)=a+b+c=3,\\p(2)=4a+2b+c=9.\end{cases}
```

In matrix form:

```math
\begin{pmatrix}0&0&1\\1&1&1\\4&2&1\end{pmatrix}\begin{pmatrix}a\\b\\c\end{pmatrix}=\begin{pmatrix}1\\3\\9\end{pmatrix}.
```

From the first equation $`c=1`$. Then:
- $`a+b=2`$
- $`4a+2b=8\Rightarrow 2a+b=4`$

Subtracting: $`(2a+b)-(a+b)=4-2\Rightarrow a=2`$, so $`b=0`$.

```math
p(x)=2x^2+1.
```

## Verification and Consistency Checks

- $`p(0)=1`$ ✓
- $`p(1)=2+1=3`$ ✓
- $`p(2)=8+1=9`$ ✓
