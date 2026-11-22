# Exercise 5. Row Operations

## Problem Statement

For

```math
A=\begin{pmatrix}1&2&3\\2&1&0\\-1&4&2\end{pmatrix}
```

find $`\det A`$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Theoretical Background and Concepts

Effect of row operations on the determinant:
- $`R_i\leftarrow R_i+kR_j`$: determinant **does not change**;
- $`R_i\leftrightarrow R_j`$: determinant **changes sign**;
- $`R_i\leftarrow cR_i`$: determinant is **multiplied by $`c`$**.

The goal is an upper triangular matrix, whose determinant is the product of the diagonal.

## Detailed Step-by-Step Solution

**Step 1:** $`R_2\leftarrow R_2-2R_1`$ (no change): $`(2,1,0)-2(1,2,3)=(0,-3,-6)`$

**Step 2:** $`R_3\leftarrow R_3+R_1`$ (no change): $`(-1,4,2)+(1,2,3)=(0,6,5)`$

```math
\begin{pmatrix}1&2&3\\0&-3&-6\\0&6&5\end{pmatrix}
```

**Step 3:** $`R_3\leftarrow R_3+2R_2`$ (no change): $`(0,6,5)+2(0,-3,-6)=(0,0,-7)`$

```math
\begin{pmatrix}1&2&3\\0&-3&-6\\0&0&-7\end{pmatrix}
```

Only operations of the type "add a multiple of a row" were used, so the determinant never changed:

```math
\det A=1\cdot(-3)\cdot(-7)=21.
```

## Verification and Consistency Checks

Cofactor expansion of the original matrix along the first row:

```math
\det A=1\cdot(1\cdot2-0\cdot4)-2\cdot(2\cdot2-0\cdot(-1))+3\cdot(2\cdot4-1\cdot(-1))=2-8+27=21.
```

Both methods give $`21`$. ✓
