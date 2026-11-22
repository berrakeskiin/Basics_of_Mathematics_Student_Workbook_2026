# Exercise 2. Determinant of a 3×3 Matrix

## Problem Statement

For

```math
A=\begin{pmatrix}1&2&-1\\0&3&4\\2&1&5\end{pmatrix}
```

compute $`\det A`$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

## Theoretical Background and Concepts

- **Sarrus' rule** (only for $`3\times3`$): add the three products along the main diagonals and subtract the three products along the anti-diagonals:

```math
\det A=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}-a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}.
```

- **Check method:** Laplace (cofactor) expansion along a column with a zero gives the same value.

## Detailed Step-by-Step Solution

Positive terms:
- $`1\cdot3\cdot5=15`$
- $`2\cdot4\cdot2=16`$
- $`(-1)\cdot0\cdot1=0`$

Negative terms:
- $`(-1)\cdot3\cdot2=-6`$
- $`1\cdot4\cdot1=4`$
- $`2\cdot0\cdot5=0`$

```math
\det A=(15+16+0)-(-6+4+0)=31-(-2)=33.
```

## Verification and Consistency Checks

Cofactor expansion along the first column (it contains a zero):

```math
\det A=1\cdot\det\begin{pmatrix}3&4\\1&5\end{pmatrix}-0+2\cdot\det\begin{pmatrix}2&-1\\3&4\end{pmatrix}=1\cdot(15-4)+2\cdot(8+3)=11+22=33.
```

Both methods give $`\det A=33`$. ✓
