# Exercise 13. Determinant by Elimination

## Problem Statement

Compute the determinant of

```math
A=\begin{pmatrix}1&2&3\\2&5&7\\1&0&2\end{pmatrix}
```

using elimination. Record the effect of every row operation used on the value of the determinant.

## Theoretical Background and Concepts

- Elimination turns $`A`$ into an upper triangular matrix $`U`$.
- $`R_i\leftarrow R_i+kR_j`$: no change; $`R_i\leftrightarrow R_j`$: sign change; $`R_i\leftarrow cR_i`$: multiply by $`c`$.
- $`\det U`$ = product of the diagonal.

## Detailed Step-by-Step Solution

| Step | Operation | Result row | Effect on det |
|---|---|---|---|
| 1 | $`R_2\leftarrow R_2-2R_1`$ | $`(0,1,1)`$ | none |
| 2 | $`R_3\leftarrow R_3-R_1`$ | $`(0,-2,-1)`$ | none |
| 3 | $`R_3\leftarrow R_3+2R_2`$ | $`(0,0,1)`$ | none |

```math
U=\begin{pmatrix}1&2&3\\0&1&1\\0&0&1\end{pmatrix},\qquad \det A=\det U=1\cdot1\cdot1=1.
```

## Verification and Consistency Checks

Cofactor expansion along the third row (it contains a zero):

```math
\det A=1\cdot\det\begin{pmatrix}2&3\\5&7\end{pmatrix}-0+2\cdot\det\begin{pmatrix}1&2\\2&5\end{pmatrix}=1\cdot(14-15)+2\cdot(5-4)=-1+2=1.
```

✓
