# Exercise 6. Parameter and Invertibility

## Problem Statement

For

```math
A(t)=\begin{pmatrix}t&1\\2&t\end{pmatrix}
```

find all values of $`t`$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

## Theoretical Background and Concepts

- A square matrix is invertible $`\iff \det A\neq0`$. So the matrix is **not** invertible exactly when $`\det A(t)=0`$.
- For $`2\times2`$: $`\det\begin{pmatrix}a&b\\c&d\end{pmatrix}=ad-bc`$.

## Detailed Step-by-Step Solution

```math
\det A(t)=t\cdot t-1\cdot2=t^2-2.
```

```math
t^2-2=0\iff t^2=2\iff t=\sqrt2\ \text{ or }\ t=-\sqrt2.
```

**Answer:** $`A(t)`$ is not invertible for $`t=\pm\sqrt2`$, and it is invertible for all other real $`t`$.

**Relation to the determinant:** for these values the determinant is zero, which means the rows are linearly dependent (one is a multiple of the other), so the matrix squeezes the plane onto a line and cannot be reversed.

## Verification and Consistency Checks

- $`t=\sqrt2`$: rows $`(\sqrt2,1)`$ and $`(2,\sqrt2)`$. Since $`\sqrt2\cdot(\sqrt2,1)=(2,\sqrt2)`$, the second row is a multiple of the first. ✓
- $`t=-\sqrt2`$: $`-\sqrt2\cdot(-\sqrt2,1)=(2,-\sqrt2)`$, again the second row. ✓
- Example $`t=0`$: $`\det=-2\neq0`$, so $`A(0)`$ is invertible, as expected. ✓
