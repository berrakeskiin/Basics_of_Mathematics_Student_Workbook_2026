# Exercise 10. Columns of a Matrix Product

## Problem Statement

Given

```math
A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&2\\-1&0\\3&1\end{pmatrix},
```

with columns of $`B`$ denoted $`b_1,b_2`$.
1. Compute $`Ab_1`$ and $`Ab_2`$.
2. Compute the matrix $`AB`$.
3. Compare the results and explain why the columns of $`AB`$ are exactly $`Ab_1`$ and $`Ab_2`$.

## Theoretical Background and Concepts

- If $`B=[\,b_1\ b_2\ \cdots\ b_p\,]`$, then

```math
AB=[\,Ab_1\ \ Ab_2\ \cdots\ Ab_p\,].
```

- This follows from the definition $`(AB)_{ij}=\sum_k a_{ik}b_{kj}`$: column $`j`$ of $`AB`$ uses only column $`j`$ of $`B`$.

## Detailed Step-by-Step Solution

$`b_1=\begin{pmatrix}1\\-1\\3\end{pmatrix}`$, $`b_2=\begin{pmatrix}2\\0\\1\end{pmatrix}`$.

**1.**

```math
Ab_1=\begin{pmatrix}1\cdot1+2\cdot(-1)+0\cdot3\\0\cdot1+1\cdot(-1)+1\cdot3\end{pmatrix}=\begin{pmatrix}-1\\2\end{pmatrix},\qquad Ab_2=\begin{pmatrix}1\cdot2+2\cdot0+0\cdot1\\0\cdot2+1\cdot0+1\cdot1\end{pmatrix}=\begin{pmatrix}2\\1\end{pmatrix}.
```

**2.** Using row-times-column:

```math
AB=\begin{pmatrix}1-2+0&2+0+0\\0-1+3&0+0+1\end{pmatrix}=\begin{pmatrix}-1&2\\2&1\end{pmatrix}.
```

**3.** The first column of $`AB`$ is $`(-1,2)^T=Ab_1`$, and the second column is $`(2,1)^T=Ab_2`$.
Reason: the entry $`(AB)_{ij}`$ equals (row $`i`$ of $`A`$)·(column $`j`$ of $`B`$). Fixing $`j`$ and letting $`i`$ run over all rows gives exactly the vector $`A b_j`$. So each column of the product is "$`A`$ applied to the corresponding column of $`B`$".

## Verification and Consistency Checks

- Size: $`A`$ is $`2\times3`$ and $`B`$ is $`3\times2`$, so $`AB`$ is $`2\times2`$; each $`Ab_j`$ is $`2\times1`$. ✓
- Both computation methods gave identical numbers. ✓
