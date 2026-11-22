# Exercise 12. Formula for a Matrix Power

## Problem Statement

Let

```math
A=\begin{pmatrix}1&1\\0&1\end{pmatrix}.
```

Compute $`A^2`$, $`A^3`$, $`A^4`$, and formulate a conjecture for $`A^n`$. Then assume the formula is true for $`n`$, multiply by $`A`$, and explain why you obtain exactly the formula for $`n+1`$.

## Theoretical Background and Concepts

- Successive powers: $`A^{n+1}=A^nA`$.
- **Mathematical induction:** if a statement holds for $`n=1`$ (base case), and its truth for $`n`$ implies its truth for $`n+1`$ (inductive step), then it holds for all $`n\ge1`$.

## Detailed Step-by-Step Solution

**Computations:**

```math
A^2=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1&2\\0&1\end{pmatrix},
```

```math
A^3=A^2A=\begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1&3\\0&1\end{pmatrix},
```

```math
A^4=A^3A=\begin{pmatrix}1&3\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1&4\\0&1\end{pmatrix}.
```

**Conjecture:**

```math
A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}\quad(n\ge1).
```

**Base case** $`n=1`$: $`\begin{pmatrix}1&1\\0&1\end{pmatrix}=A`$. ✓

**Inductive step:** assume $`A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}`$. Then

```math
A^{n+1}=A^nA=\begin{pmatrix}1&n\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1\cdot1+n\cdot0&1\cdot1+n\cdot1\\0\cdot1+1\cdot0&0\cdot1+1\cdot1\end{pmatrix}=\begin{pmatrix}1&n+1\\0&1\end{pmatrix}.
```

This is exactly the formula with $`n`$ replaced by $`n+1`$. Multiplying by $`A`$ adds 1 to the upper-right entry and leaves the other entries unchanged. By induction, the formula holds for all $`n\ge1`$.

## Verification and Consistency Checks

- The formula agrees with the computed $`A^2,A^3,A^4`$. ✓
- $`\det A^n=1\cdot1-n\cdot0=1=(\det A)^n`$. ✓
- The formula also works for $`n=0`$ ($`A^0=I`$), and $`A^{-1}=\begin{pmatrix}1&-1\\0&1\end{pmatrix}`$ satisfies $`AA^{-1}=I`$, which matches $`n=-1`$.
- Geometric interpretation: $`A`$ is a horizontal shear by 1, so applying it $`n`$ times gives a shear by $`n`$.
