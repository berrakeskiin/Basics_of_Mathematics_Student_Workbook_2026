# Exercise 11. Shortening the Calculation with Row Operations

## Problem Statement

Compute

```math
\det\begin{pmatrix}1&2&3\\1&3&4\\1&4&6\end{pmatrix}
```

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## Theoretical Background and Concepts

- Adding a multiple of one row to another row, $`R_i\leftarrow R_i+kR_j`$, **does not change** the determinant.
- (Swapping rows changes the sign; multiplying a row by $`c`$ multiplies the determinant by $`c`$; neither is needed here.)
- The determinant of a triangular matrix is the product of its diagonal entries.

## Detailed Step-by-Step Solution

All entries of the first column are $`1`$, so subtract the first row:

- $`R_2\leftarrow R_2-R_1`$: $`(0,1,1)`$ (no change)
- $`R_3\leftarrow R_3-R_1`$: $`(0,2,3)`$ (no change)

```math
\begin{pmatrix}1&2&3\\0&1&1\\0&2&3\end{pmatrix}
```

- $`R_3\leftarrow R_3-2R_2`$: $`(0,0,1)`$ (no change)

```math
\begin{pmatrix}1&2&3\\0&1&1\\0&0&1\end{pmatrix}
```

```math
\det=1\cdot1\cdot1=1.
```

All three operations were of the type $`R_i\leftarrow R_i+kR_j`$, so none of them changed the determinant.

## Verification and Consistency Checks

Direct expansion along the first row:

```math
1\cdot(3\cdot6-4\cdot4)-2\cdot(1\cdot6-4\cdot1)+3\cdot(1\cdot4-3\cdot1)=2-4+3=1.
```

✓
