# Exercise 8. Determinant of a Product

## Problem Statement

Let $`A,B`$ be square matrices such that $`\det A=3`$ and $`\det B=-5`$. Compute $`\det(AB)`$, $`\det(BA)`$ and, if it exists, $`\det(A^{-1}B)`$. Explain why the first two results are equal even though usually $`AB\neq BA`$.

## Theoretical Background and Concepts

- $`\det(AB)=\det A\cdot\det B`$.
- If $`\det A\neq0`$, then $`A^{-1}`$ exists and $`\det(A^{-1})=\dfrac{1}{\det A}`$.

## Detailed Step-by-Step Solution

```math
\det(AB)=\det A\cdot\det B=3\cdot(-5)=-15.
```

```math
\det(BA)=\det B\cdot\det A=(-5)\cdot3=-15.
```

Since $`\det A=3\neq0`$, $`A^{-1}`$ exists:

```math
\det(A^{-1}B)=\det(A^{-1})\cdot\det B=\frac13\cdot(-5)=-\frac53.
```

**Why $`\det(AB)=\det(BA)`$:** the matrices $`AB`$ and $`BA`$ may be different, but their determinants are products of two **numbers**, $`\det A`$ and $`\det B`$, and multiplication of numbers is commutative.

## Verification and Consistency Checks

- Example: $`A=\operatorname{diag}(3,1)`$, $`B=\begin{pmatrix}0&1\\5&0\end{pmatrix}`$ ($`\det B=-5`$). Then $`AB=\begin{pmatrix}0&3\\5&0\end{pmatrix}`$ and $`BA=\begin{pmatrix}0&1\\15&0\end{pmatrix}`$, so $`AB\neq BA`$, but both determinants equal $`-15`$. ✓
- $`\det(A\cdot A^{-1}B)=3\cdot(-\frac53)=-5=\det B`$. ✓
