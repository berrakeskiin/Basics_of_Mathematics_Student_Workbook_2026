# Exercise 5. Matrix Times Vector

## Problem Statement

Let

```math
A=\begin{pmatrix}2&-1\\1&3\end{pmatrix},\qquad x=\begin{pmatrix}4\\2\end{pmatrix}.
```

Compute $`Ax`$. Then express $`Ax`$ as a linear combination of the columns of $`A`$, with coefficients coming from the vector $`x`$.

## Theoretical Background and Concepts

- **Row view:** the $`i`$-th component of $`Ax`$ is (row $`i`$ of $`A`$) $`\cdot\ x`$.
- **Column view:** if $`A=[\,a_1\ a_2\,]`$ (columns) and $`x=(x_1,x_2)^T`$, then

```math
Ax=x_1a_1+x_2a_2,
```

i.e. $`Ax`$ is a linear combination of the columns of $`A`$ with the components of $`x`$ as weights.

## Detailed Step-by-Step Solution

**Row view:**

```math
Ax=\begin{pmatrix}2\cdot4+(-1)\cdot2\\1\cdot4+3\cdot2\end{pmatrix}=\begin{pmatrix}8-2\\4+6\end{pmatrix}=\begin{pmatrix}6\\10\end{pmatrix}.
```

**Column view:** columns of $`A`$ are $`a_1=\begin{pmatrix}2\\1\end{pmatrix}`$, $`a_2=\begin{pmatrix}-1\\3\end{pmatrix}`$, and $`x_1=4`$, $`x_2=2`$:

```math
Ax=4\begin{pmatrix}2\\1\end{pmatrix}+2\begin{pmatrix}-1\\3\end{pmatrix}=\begin{pmatrix}8\\4\end{pmatrix}+\begin{pmatrix}-2\\6\end{pmatrix}=\begin{pmatrix}6\\10\end{pmatrix}.
```

## Verification and Consistency Checks

- Both methods give the same vector $`(6,10)^T`$. ✓
- Size check: $`A`$ is $`2\times2`$ and $`x`$ is $`2\times1`$, so $`Ax`$ must be $`2\times1`$. ✓
- The column view shows that $`Ax`$ always lies in the span of the columns of $`A`$ (the column space).
