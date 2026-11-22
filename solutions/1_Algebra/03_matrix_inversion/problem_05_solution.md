# Exercise 5. A 3×3 Matrix

## Problem Statement

Use Gauss–Jordan elimination to find the inverse of

```math
A=\begin{pmatrix}1&1&0\\0&1&1\\1&0&1\end{pmatrix}.
```

Check the result by multiplication.

## Theoretical Background and Concepts

- Write $`[A\mid I]`$ and use row operations to reach $`[I\mid A^{-1}]`$.
- The inverse exists because $`\det A=1\cdot(1-0)-1\cdot(0-1)+0=2\neq0`$.

## Detailed Step-by-Step Solution

```math
\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&1&0&1&0\\1&0&1&0&0&1\end{array}\right]
```

$`R_3\leftarrow R_3-R_1`$:

```math
\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&1&0&1&0\\0&-1&1&-1&0&1\end{array}\right]
```

$`R_3\leftarrow R_3+R_2`$:

```math
\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&1&0&1&0\\0&0&2&-1&1&1\end{array}\right]
```

$`R_3\leftarrow \frac12R_3`$:

```math
\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&1&0&1&0\\0&0&1&-\frac12&\frac12&\frac12\end{array}\right]
```

$`R_2\leftarrow R_2-R_3`$:

```math
\left[\begin{array}{ccc|ccc}1&1&0&1&0&0\\0&1&0&\frac12&\frac12&-\frac12\\0&0&1&-\frac12&\frac12&\frac12\end{array}\right]
```

$`R_1\leftarrow R_1-R_2`$:

```math
\left[\begin{array}{ccc|ccc}1&0&0&\frac12&-\frac12&\frac12\\0&1&0&\frac12&\frac12&-\frac12\\0&0&1&-\frac12&\frac12&\frac12\end{array}\right]
```

```math
A^{-1}=\frac12\begin{pmatrix}1&-1&1\\1&1&-1\\-1&1&1\end{pmatrix}.
```

## Verification and Consistency Checks

```math
A\cdot\begin{pmatrix}1&-1&1\\1&1&-1\\-1&1&1\end{pmatrix}=\begin{pmatrix}1+1&-1+1&1-1\\1-1&1+1&-1+1\\1-1&-1+1&1+1\end{pmatrix}=\begin{pmatrix}2&0&0\\0&2&0\\0&0&2\end{pmatrix},
```

so after multiplying by $`\frac12`$ we get $`AA^{-1}=I`$. ✓
