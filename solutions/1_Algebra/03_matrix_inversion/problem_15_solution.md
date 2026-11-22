# Exercise 15. Two Methods for Solving the Same System

## Problem Statement

For

```math
A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}7\\8\end{pmatrix}
```

solve $`Ax=b`$ in two ways: (1) using $`A^{-1}b`$, (2) using Gaussian elimination. Compare both solutions and the number of essential steps, and state which method was simpler here.

## Theoretical Background and Concepts

- **Method 1:** if $`\det A\neq0`$, then $`x=A^{-1}b`$.
- **Method 2:** Gaussian elimination: reduce $`[A\mid b]`$ to triangular form, then back-substitute.

## Detailed Step-by-Step Solution

**Method 1 (inverse):**

```math
\det A=6-1=5,\qquad A^{-1}=\frac15\begin{pmatrix}3&-1\\-1&2\end{pmatrix},
```

```math
x=\frac15\begin{pmatrix}3\cdot7-1\cdot8\\-1\cdot7+2\cdot8\end{pmatrix}=\frac15\begin{pmatrix}13\\9\end{pmatrix}=\begin{pmatrix}\frac{13}5\\\frac95\end{pmatrix}.
```

**Method 2 (elimination):** swap the equations to have a leading 1:

```math
\left[\begin{array}{cc|c}1&3&8\\2&1&7\end{array}\right]\xrightarrow{R_2-2R_1}\left[\begin{array}{cc|c}1&3&8\\0&-5&-9\end{array}\right].
```

Back-substitution: $`-5y=-9\Rightarrow y=\frac95`$, and $`x=8-3\cdot\frac95=\frac{40-27}5=\frac{13}5`$.

**Comparison:** both methods give $`x=\frac{13}5,\ y=\frac95`$.
- Method 1: determinant, inverse (4 entries), then a matrix–vector product.
- Method 2: one row operation and two short back-substitution steps.

For this single system, **elimination was simpler**. The inverse is more useful when the same $`A`$ must be used with many different right-hand sides $`b`$ (compare Exercise 6, where $`b=(5,7)^T`$ used the same $`A^{-1}`$).

## Verification and Consistency Checks

```math
A\begin{pmatrix}\frac{13}5\\\frac95\end{pmatrix}=\begin{pmatrix}\frac{26+9}5\\\frac{13+27}5\end{pmatrix}=\begin{pmatrix}7\\8\end{pmatrix}=b.
```

✓
