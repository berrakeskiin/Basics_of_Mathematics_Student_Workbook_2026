# Exercise 1. Definition of the Inverse

## Problem Statement

For

```math
A=\begin{pmatrix}2&1\\1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}
```

check, without using a formula, whether $`B=A^{-1}`$. Compute $`AB`$ and $`BA`$ and relate the result to the definition of the inverse.

## Theoretical Background and Concepts

- **Definition:** a square matrix $`B`$ is the inverse of $`A`$ if $`AB=I`$ **and** $`BA=I`$.
- If such $`B`$ exists, it is unique and is denoted $`A^{-1}`$.

## Detailed Step-by-Step Solution

```math
AB=\begin{pmatrix}2\cdot1+1\cdot(-1)&2\cdot(-1)+1\cdot2\\1\cdot1+1\cdot(-1)&1\cdot(-1)+1\cdot2\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}=I.
```

```math
BA=\begin{pmatrix}1\cdot2+(-1)\cdot1&1\cdot1+(-1)\cdot1\\-1\cdot2+2\cdot1&-1\cdot1+2\cdot1\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}=I.
```

**Conclusion:** both products equal the identity matrix, so by the definition $`B=A^{-1}`$.

## Verification and Consistency Checks

- $`\det A=2-1=1\neq0`$, so $`A`$ is invertible, consistent with the result. ✓
- $`\det B=2-1=1=\dfrac1{\det A}`$, as required for an inverse. ✓
