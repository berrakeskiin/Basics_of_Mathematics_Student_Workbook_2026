# Exercise 10. Inverse of a Diagonal Matrix

## Problem Statement

Given

```math
D=\begin{pmatrix}2&0&0\\0&-3&0\\0&0&5\end{pmatrix},\qquad E=\begin{pmatrix}2&0&0\\0&0&0\\0&0&5\end{pmatrix},
```

decide without Gauss–Jordan elimination which matrix is invertible. For the invertible matrix, give the inverse and check it by multiplication.

## Theoretical Background and Concepts

- The determinant of a diagonal matrix is the product of its diagonal entries.
- A diagonal matrix is invertible $`\iff`$ all diagonal entries are nonzero, and then its inverse is the diagonal matrix of the reciprocals.

## Detailed Step-by-Step Solution

- $`\det D=2\cdot(-3)\cdot5=-30\neq0`$, so **$`D`$ is invertible**.
- $`\det E=2\cdot0\cdot5=0`$, so **$`E`$ is not invertible** (it sends the vector $`(0,1,0)^T`$ to the zero vector).

```math
D^{-1}=\begin{pmatrix}\frac12&0&0\\0&-\frac13&0\\0&0&\frac15\end{pmatrix}.
```

## Verification and Consistency Checks

```math
DD^{-1}=\begin{pmatrix}2\cdot\frac12&0&0\\0&(-3)\cdot(-\frac13)&0\\0&0&5\cdot\frac15\end{pmatrix}=\begin{pmatrix}1&0&0\\0&1&0\\0&0&1\end{pmatrix}=I.
```

✓ $`\det D^{-1}=\frac12\cdot(-\frac13)\cdot\frac15=-\frac1{30}=\frac1{\det D}`$. ✓
