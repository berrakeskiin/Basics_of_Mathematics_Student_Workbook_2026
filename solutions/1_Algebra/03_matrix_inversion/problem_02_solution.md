# Exercise 2. Formula for a 2×2 Matrix

## Problem Statement

Find the inverse of

```math
A=\begin{pmatrix}3&2\\5&4\end{pmatrix}
```

using the formula for a $`2\times2`$ matrix. At the end, check the result by computing one product with $`A`$.

## Theoretical Background and Concepts

If $`\det A=ad-bc\neq0`$, then

```math
\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1}=\frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}
```

(swap the diagonal entries, change the sign of the off-diagonal entries, divide by the determinant).

## Detailed Step-by-Step Solution

```math
\det A=3\cdot4-2\cdot5=12-10=2\neq0.
```

```math
A^{-1}=\frac12\begin{pmatrix}4&-2\\-5&3\end{pmatrix}=\begin{pmatrix}2&-1\\-\frac52&\frac32\end{pmatrix}.
```

## Verification and Consistency Checks

```math
AA^{-1}=\begin{pmatrix}3&2\\5&4\end{pmatrix}\begin{pmatrix}2&-1\\-\frac52&\frac32\end{pmatrix}=\begin{pmatrix}6-5&-3+3\\10-10&-5+6\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}.
```

✓ Also $`\det A^{-1}=2\cdot\frac32-(-1)(-\frac52)=3-\frac52=\frac12=\frac1{\det A}`$. ✓
