# Exercise 1. Determinant of a 2×2 Matrix

## Problem Statement

Compute

```math
\det\begin{pmatrix}3&-2\\5&4\end{pmatrix},\qquad \det\begin{pmatrix}1&7\\2&14\end{pmatrix}.
```

Which matrix is invertible? Justify your answer.

## Theoretical Background and Concepts

- For a $`2\times2`$ matrix: $`\det\begin{pmatrix}a&b\\c&d\end{pmatrix}=ad-bc`$.
- A square matrix is invertible **if and only if** its determinant is not zero.

## Detailed Step-by-Step Solution

```math
\det\begin{pmatrix}3&-2\\5&4\end{pmatrix}=3\cdot4-(-2)\cdot5=12+10=22.
```

```math
\det\begin{pmatrix}1&7\\2&14\end{pmatrix}=1\cdot14-7\cdot2=14-14=0.
```

**Conclusion:** the first matrix is invertible ($`\det=22\neq0`$). The second matrix is **not** invertible ($`\det=0`$): its second row is exactly 2 times the first row, so the rows are linearly dependent.

## Verification and Consistency Checks

- Inverse of the first matrix: $`\frac1{22}\begin{pmatrix}4&2\\-5&3\end{pmatrix}`$. Check: $`\begin{pmatrix}3&-2\\5&4\end{pmatrix}\begin{pmatrix}4&2\\-5&3\end{pmatrix}=\begin{pmatrix}22&0\\0&22\end{pmatrix}`$, so the product with $`\frac1{22}`$ is $`I`$. ✓
- For the second matrix, $`(2,14)=2\cdot(1,7)`$, which confirms $`\det=0`$. ✓
