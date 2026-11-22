# Exercise 4. Triangular Matrix

## Problem Statement

Without expanding the determinant, compute

```math
\det\begin{pmatrix}2&4&1\\0&-3&5\\0&0&7\end{pmatrix}.
```

State the rule for an arbitrary triangular matrix and explain it using this example.

## Theoretical Background and Concepts

- **Rule:** the determinant of a triangular matrix (upper or lower) equals the **product of its diagonal entries**.
- Reason: in a cofactor expansion along the first column, only the diagonal entry is nonzero, and the remaining minor is again triangular. Repeating this gives the product of the diagonal.

## Detailed Step-by-Step Solution

```math
\det\begin{pmatrix}2&4&1\\0&-3&5\\0&0&7\end{pmatrix}=2\cdot(-3)\cdot7=-42.
```

**Explanation with this example:** expanding along the first column gives

```math
2\cdot\det\begin{pmatrix}-3&5\\0&7\end{pmatrix}=2\cdot\big((-3)\cdot7-5\cdot0\big)=2\cdot(-21)=-42,
```

because the other two entries of the first column are zero. The entries above the diagonal ($`4,1,5`$) never contribute.

## Verification and Consistency Checks

- Sarrus' rule: positive terms $`2\cdot(-3)\cdot7+4\cdot5\cdot0+1\cdot0\cdot0=-42`$, negative terms are all $`0`$ (each contains a zero below the diagonal), so $`\det=-42`$. ✓
- All diagonal entries are nonzero, so the matrix is invertible, consistent with $`\det\neq0`$. ✓
