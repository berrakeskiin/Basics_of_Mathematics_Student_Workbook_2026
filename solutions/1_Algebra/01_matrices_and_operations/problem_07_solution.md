# Exercise 7. Identity Matrix, Zero Matrix, and Powers

## Problem Statement

For

```math
A=\begin{pmatrix}2&1\\0&2\end{pmatrix}
```

compute $`AI,\ IA,\ A+0,\ A^2,\ A^3`$. Explain the roles of the matrices $`I`$ and $`0`$, and describe the pattern you observe in successive powers of $`A`$.

## Theoretical Background and Concepts

- $`I=\begin{pmatrix}1&0\\0&1\end{pmatrix}`$ is the **identity matrix**, the neutral element of multiplication: $`AI=IA=A`$.
- $`0=\begin{pmatrix}0&0\\0&0\end{pmatrix}`$ is the **zero matrix**, the neutral element of addition: $`A+0=A`$.
- Powers: $`A^2=AA`$, $`A^3=A^2A`$, etc.
- We can write $`A=2I+N`$ with $`N=\begin{pmatrix}0&1\\0&0\end{pmatrix}`$, where $`N^2=0`$ and $`N`$ commutes with $`I`$.

## Detailed Step-by-Step Solution

**Neutral elements:**

```math
AI=\begin{pmatrix}2\cdot1+1\cdot0&2\cdot0+1\cdot1\\0&2\end{pmatrix}=\begin{pmatrix}2&1\\0&2\end{pmatrix}=A,\qquad IA=A,\qquad A+0=A.
```

**$`A^2`$:**

```math
A^2=\begin{pmatrix}2&1\\0&2\end{pmatrix}\begin{pmatrix}2&1\\0&2\end{pmatrix}=\begin{pmatrix}4&2+2\\0&4\end{pmatrix}=\begin{pmatrix}4&4\\0&4\end{pmatrix}.
```

**$`A^3`$:**

```math
A^3=A^2A=\begin{pmatrix}4&4\\0&4\end{pmatrix}\begin{pmatrix}2&1\\0&2\end{pmatrix}=\begin{pmatrix}8&4+8\\0&8\end{pmatrix}=\begin{pmatrix}8&12\\0&8\end{pmatrix}.
```

**Pattern:** the diagonal entries are $`2^n`$, the lower-left entry stays $`0`$, and the upper-right entry is $`1, 4, 12,\dots = n\cdot2^{n-1}`$:

```math
A^n=\begin{pmatrix}2^n&n\,2^{n-1}\\0&2^n\end{pmatrix}.
```

Explanation: $`A^n=(2I+N)^n=2^nI+n\,2^{n-1}N`$, because $`N^2=0`$ removes all the other terms of the binomial expansion.

## Verification and Consistency Checks

- Formula for $`n=1`$: $`\begin{pmatrix}2&1\\0&2\end{pmatrix}=A`$ ✓; $`n=2`$: $`\begin{pmatrix}4&4\\0&4\end{pmatrix}`$ ✓; $`n=3`$: $`\begin{pmatrix}8&12\\0&8\end{pmatrix}`$ ✓.
- Determinant: $`\det A=4`$, so $`\det A^3=4^3=64`$; directly $`8\cdot8-12\cdot0=64`$. ✓
