# Exercise 12. A Parameter Revealed by a Row Operation

## Problem Statement

For

```math
A(t)=\begin{pmatrix}1&2&3\\2&4&t\\0&1&1\end{pmatrix}
```

find the values of $`t`$ for which the matrix is not invertible. First perform $`R_2\leftarrow R_2-2R_1`$ and use the resulting structure. At the end, explain what happens to the rows for that value of the parameter.

## Theoretical Background and Concepts

- $`R_i\leftarrow R_i+kR_j`$ does not change the determinant; a row swap changes its sign.
- $`A`$ is not invertible $`\iff\det A=0\iff`$ the rows are linearly dependent.

## Detailed Step-by-Step Solution

$`R_2\leftarrow R_2-2R_1`$: $`(2,4,t)-2(1,2,3)=(0,0,t-6)`$ (determinant unchanged):

```math
\begin{pmatrix}1&2&3\\0&0&t-6\\0&1&1\end{pmatrix}.
```

Swap $`R_2\leftrightarrow R_3`$ (sign changes) to get a triangular matrix:

```math
\begin{pmatrix}1&2&3\\0&1&1\\0&0&t-6\end{pmatrix},\qquad \det=1\cdot1\cdot(t-6)=t-6.
```

Therefore

```math
\det A(t)=-(t-6)=6-t.
```

$`\det A(t)=0\iff t=6`$. **The matrix is not invertible only for $`t=6`$.**

**What happens to the rows:** for $`t=6`$ the second row is $`(2,4,6)=2\cdot(1,2,3)`$, i.e. $`R_2=2R_1`$. The rows are linearly dependent, which is exactly why the operation $`R_2-2R_1`$ produced a zero row.

## Verification and Consistency Checks

Direct expansion along the first row:

```math
\det A(t)=1\cdot(4-t)-2\cdot(2-0)+3\cdot(2-0)=4-t-4+6=6-t.
```

✓ Numerical check: $`t=7`$ gives $`\det=-1`$, and $`t=0`$ gives $`\det=6`$, both consistent with $`6-t`$.
