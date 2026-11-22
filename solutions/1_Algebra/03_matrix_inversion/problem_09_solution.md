# Exercise 9. Matrix Equation

## Problem Statement

Given

```math
A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}3&1\\2&4\end{pmatrix},
```

solve $`AX=B`$ for $`X`$. Before calculating, decide on which side $`A^{-1}`$ must be used. Then check the result by computing $`AX`$.

## Theoretical Background and Concepts

- In $`AX=B`$, the matrix $`A`$ stands on the **left** of $`X`$. To remove it we multiply both sides **from the left** by $`A^{-1}`$: $`A^{-1}AX=A^{-1}B`$, so $`X=A^{-1}B`$.
- $`BA^{-1}`$ would be wrong, because matrix multiplication is not commutative.

## Detailed Step-by-Step Solution

```math
\det A=1,\qquad A^{-1}=\begin{pmatrix}1&-2\\0&1\end{pmatrix}.
```

```math
X=A^{-1}B=\begin{pmatrix}1&-2\\0&1\end{pmatrix}\begin{pmatrix}3&1\\2&4\end{pmatrix}=\begin{pmatrix}3-4&1-8\\2&4\end{pmatrix}=\begin{pmatrix}-1&-7\\2&4\end{pmatrix}.
```

## Verification and Consistency Checks

```math
AX=\begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}-1&-7\\2&4\end{pmatrix}=\begin{pmatrix}-1+4&-7+8\\2&4\end{pmatrix}=\begin{pmatrix}3&1\\2&4\end{pmatrix}=B.
```

✓ For comparison, the wrong order gives $`BA^{-1}=\begin{pmatrix}3&-5\\2&0\end{pmatrix}\neq X`$.
