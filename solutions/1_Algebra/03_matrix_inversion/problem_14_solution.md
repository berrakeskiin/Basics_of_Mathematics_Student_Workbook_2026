# Exercise 14. A Matrix That Is Its Own Inverse

## Problem Statement

Assume that a square matrix $`A`$ satisfies $`A^2=I`$. Show that $`A^{-1}=A`$. Then give an example of a $`2\times2`$ matrix different from $`I`$ and $`-I`$ that satisfies this condition, and verify it by multiplication.

## Theoretical Background and Concepts

- **Definition:** $`B=A^{-1}`$ if $`AB=I`$ and $`BA=I`$.
- Such a matrix is called an *involution*: applying it twice gives back the starting point (e.g. a reflection).

## Detailed Step-by-Step Solution

**Proof:** $`A^2=I`$ means $`A\cdot A=I`$. Taking $`B=A`$ we have $`AB=A\cdot A=I`$ and $`BA=A\cdot A=I`$. By the definition of the inverse, $`A^{-1}=A`$. $`\blacksquare`$

**Example:** the reflection across the line $`y=x`$ (swapping coordinates):

```math
A=\begin{pmatrix}0&1\\1&0\end{pmatrix}.
```

**Verification by multiplication:**

```math
A^2=\begin{pmatrix}0&1\\1&0\end{pmatrix}\begin{pmatrix}0&1\\1&0\end{pmatrix}=\begin{pmatrix}0\cdot0+1\cdot1&0\cdot1+1\cdot0\\1\cdot0+0\cdot1&1\cdot1+0\cdot0\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}=I.
```

Geometric meaning: swapping $`x`$ and $`y`$ twice returns the original vector.

## Verification and Consistency Checks

- $`A\neq I`$ and $`A\neq-I`$, as required. ✓
- $`\det A=-1`$, and $`(\det A)^2=1=\det I`$, consistent with $`A^2=I`$. ✓
- Another example: $`\begin{pmatrix}1&0\\0&-1\end{pmatrix}`$ (reflection across the $`x`$-axis) also squares to $`I`$.
