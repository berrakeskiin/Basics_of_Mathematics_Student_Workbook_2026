# Exercise 10. Detecting Dependence

## Problem Statement

Without carrying out a full determinant calculation, explain why

```math
\det\begin{pmatrix}1&2&3\\2&4&6\\0&1&5\end{pmatrix}=0.
```

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

## Theoretical Background and Concepts

- If one row is a multiple of another row (more generally, if the rows are linearly dependent), the determinant is $`0`$.
- Reason: $`R_2\leftarrow R_2-2R_1`$ does not change the determinant but creates a zero row, and a matrix with a zero row has determinant $`0`$.
- $`\det A=0\iff A`$ is not invertible.

## Detailed Step-by-Step Solution

**Dependence:** $`R_2=(2,4,6)=2\cdot(1,2,3)=2R_1`$.

Applying $`R_2\leftarrow R_2-2R_1`$ (determinant unchanged):

```math
\begin{pmatrix}1&2&3\\0&0&0\\0&1&5\end{pmatrix}.
```

This matrix has a zero row, so its determinant is $`0`$, and therefore the original determinant is also $`0`$.

**Noninvertibility:** the rows span at most a 2-dimensional space, so the matrix maps $`\mathbb R^3`$ onto a plane (or smaller). For example, the system $`Ax=b`$ cannot have a unique solution, and $`A^{-1}`$ does not exist.

## Verification and Consistency Checks

- Full expansion along the first row: $`1\cdot(4\cdot5-6\cdot1)-2\cdot(2\cdot5-6\cdot0)+3\cdot(2\cdot1-4\cdot0)=14-20+6=0`$. ✓
- A nonzero vector in the null space confirms noninvertibility: from $`x_2+5x_3=0`$ and $`x_1+2x_2+3x_3=0`$, take $`x_3=1`$, $`x_2=-5`$, $`x_1=7`$; then $`A(7,-5,1)^T=(0,0,0)^T`$. ✓
