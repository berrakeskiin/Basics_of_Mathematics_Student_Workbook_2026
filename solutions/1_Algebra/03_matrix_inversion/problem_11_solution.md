# Exercise 11. Parameter and Invertibility

## Problem Statement

For

```math
A(t)=\begin{pmatrix}1&t\\t&1\end{pmatrix}
```

find all $`t`$ for which the matrix is invertible, and then give a formula for $`A(t)^{-1}`$. Explain what happens to this formula at the excluded values.

## Theoretical Background and Concepts

- $`A`$ is invertible $`\iff\det A\neq0`$.
- $`\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1}=\frac1{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}`$.

## Detailed Step-by-Step Solution

```math
\det A(t)=1\cdot1-t\cdot t=1-t^2=(1-t)(1+t).
```

$`\det A(t)=0\iff t=1`$ or $`t=-1`$. **The matrix is invertible for all $`t\neq\pm1`$.**

For $`t\neq\pm1`$:

```math
A(t)^{-1}=\frac{1}{1-t^2}\begin{pmatrix}1&-t\\-t&1\end{pmatrix}.
```

**At the excluded values** the factor $`\frac1{1-t^2}`$ has a zero denominator, so the formula breaks down. This matches the matrices: $`A(1)=\begin{pmatrix}1&1\\1&1\end{pmatrix}`$ and $`A(-1)=\begin{pmatrix}1&-1\\-1&1\end{pmatrix}`$ have equal or opposite rows, so they are not invertible.

## Verification and Consistency Checks

```math
A(t)\begin{pmatrix}1&-t\\-t&1\end{pmatrix}=\begin{pmatrix}1-t^2&-t+t\\t-t&-t^2+1\end{pmatrix}=(1-t^2)I,
```

so multiplying by $`\frac1{1-t^2}`$ gives $`I`$. ✓ Example $`t=0`$: $`A(0)^{-1}=I`$, which is correct since $`A(0)=I`$. ✓
