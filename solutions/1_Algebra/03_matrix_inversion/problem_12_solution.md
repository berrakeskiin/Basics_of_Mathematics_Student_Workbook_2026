# Exercise 12. Finding Inverses Without Starting from Scratch

## Problem Statement

It is known that

```math
A^{-1}=\begin{pmatrix}2&-1\\-3&2\end{pmatrix}.
```

Without finding $`A`$, compute $`(3A)^{-1}`$, $`(A^T)^{-1}`$, and $`(A^2)^{-1}`$. Justify each result using the appropriate property.

## Theoretical Background and Concepts

- $`(cA)^{-1}=\frac1c A^{-1}`$ for $`c\neq0`$, since $`(cA)(\frac1cA^{-1})=I`$.
- $`(A^T)^{-1}=(A^{-1})^T`$, since $`A^T(A^{-1})^T=(A^{-1}A)^T=I`$.
- $`(A^2)^{-1}=(A^{-1})^2`$, since $`(AA)^{-1}=A^{-1}A^{-1}`$ (inverse of a product).

## Detailed Step-by-Step Solution

```math
(3A)^{-1}=\frac13A^{-1}=\begin{pmatrix}\frac23&-\frac13\\-1&\frac23\end{pmatrix}.
```

```math
(A^T)^{-1}=(A^{-1})^T=\begin{pmatrix}2&-3\\-1&2\end{pmatrix}.
```

```math
(A^2)^{-1}=(A^{-1})^2=\begin{pmatrix}2&-1\\-3&2\end{pmatrix}\begin{pmatrix}2&-1\\-3&2\end{pmatrix}=\begin{pmatrix}4+3&-2-2\\-6-6&3+4\end{pmatrix}=\begin{pmatrix}7&-4\\-12&7\end{pmatrix}.
```

## Verification and Consistency Checks

- For the check we may find $`A=(A^{-1})^{-1}=\begin{pmatrix}2&1\\3&2\end{pmatrix}`$ (det of $`A^{-1}`$ is $`4-3=1`$). Then $`A^2=\begin{pmatrix}7&4\\12&7\end{pmatrix}`$ and $`A^2\begin{pmatrix}7&-4\\-12&7\end{pmatrix}=\begin{pmatrix}49-48&-28+28\\84-84&-48+49\end{pmatrix}=I`$. ✓
- $`3A\cdot\frac13A^{-1}=AA^{-1}=I`$. ✓
