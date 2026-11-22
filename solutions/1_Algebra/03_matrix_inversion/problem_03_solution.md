# Exercise 3. When Does the Inverse Not Exist?

## Problem Statement

For

```math
A=\begin{pmatrix}2&4\\1&2\end{pmatrix}
```

explain in two ways why $`A^{-1}`$ does not exist: using the determinant and using dependence between the rows.

## Theoretical Background and Concepts

- $`A`$ is invertible $`\iff\det A\neq0`$.
- Equivalently, $`A`$ is invertible $`\iff`$ its rows (columns) are linearly independent.

## Detailed Step-by-Step Solution

**Way 1 (determinant):**

```math
\det A=2\cdot2-4\cdot1=4-4=0.
```

The determinant is zero, so $`A^{-1}`$ does not exist (the formula would require dividing by $`0`$).

**Way 2 (dependent rows):** $`R_1=(2,4)=2\cdot(1,2)=2R_2`$. The rows are linearly dependent, so $`A`$ maps the whole plane onto one line (every $`Ax`$ is a multiple of $`(2,1)^T`$). Different vectors are sent to the same image, e.g. $`A(2,-1)^T=(0,0)^T=A(0,0)^T`$, so the transformation cannot be undone.

Both arguments say the same thing: dependent rows $`\iff`$ zero determinant $`\iff`$ no inverse.

## Verification and Consistency Checks

- $`A\begin{pmatrix}2\\-1\end{pmatrix}=\begin{pmatrix}4-4\\2-2\end{pmatrix}=\begin{pmatrix}0\\0\end{pmatrix}`$: a nonzero vector goes to zero, which is impossible for an invertible matrix. ✓
