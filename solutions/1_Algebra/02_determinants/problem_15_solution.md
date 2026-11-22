# Exercise 15. Combining Determinant Properties

## Problem Statement

Let $`A`$ and $`B`$ be invertible $`2\times2`$ matrices with $`\det A=-2`$, $`\det B=3`$. Without finding the entries of the matrices, compute

```math
\det\left(B^{-1}A^TB\right).
```

State the determinant properties you use in order and explain why the factors involving $`B`$ eventually cancel.

## Theoretical Background and Concepts

1. Product rule: $`\det(XYZ)=\det X\cdot\det Y\cdot\det Z`$.
2. Inverse: $`\det(B^{-1})=\dfrac1{\det B}`$.
3. Transpose: $`\det(A^T)=\det A`$.

## Detailed Step-by-Step Solution

```math
\det\left(B^{-1}A^TB\right)=\det(B^{-1})\cdot\det(A^T)\cdot\det B\qquad\text{(product rule)}
```

```math
=\frac{1}{\det B}\cdot\det A\cdot\det B\qquad\text{(inverse and transpose rules)}
```

```math
=\frac13\cdot(-2)\cdot3=-2.
```

**Why $`B`$ cancels:** determinants are numbers, so their order can be changed: $`\frac1{\det B}\cdot\det B=1`$. Hence $`\det(B^{-1}MB)=\det M`$ for every square $`M`$ (similar matrices have the same determinant).

## Verification and Consistency Checks

- Example: $`A=\operatorname{diag}(-2,1)`$, $`B=\operatorname{diag}(3,1)`$. Then $`A^T=A`$, and $`B^{-1}A^TB=\operatorname{diag}(\tfrac13\cdot(-2)\cdot3,\ 1)=\operatorname{diag}(-2,1)`$, whose determinant is $`-2`$. ✓
- The answer equals $`\det A`$, as predicted by the cancellation argument. ✓
