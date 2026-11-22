# Exercise 1. Matrix Size and Entries

## Problem Statement

Given

```math
A=\begin{pmatrix}2&-1&3\\0&4&5\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\-2&3\\4&1\end{pmatrix}.
```

1. State the sizes of matrices $`A`$ and $`B`$.
2. Read off the entries $`a_{12}`$, $`a_{23}`$, $`b_{21}`$, and $`b_{32}`$.
3. Write the second row of $`A`$ and the first column of $`B`$ as vectors.

## Theoretical Background and Concepts

- A matrix of size $`m\times n`$ has $`m`$ rows and $`n`$ columns.
- The entry $`a_{ij}`$ is located in **row $`i`$** and **column $`j`$** (first index = row, second index = column).
- A row of a matrix can be written as a row vector, and a column as a column vector.

## Detailed Step-by-Step Solution

**1. Sizes.**
$`A`$ has 2 rows and 3 columns, so $`A`$ is $`2\times 3`$.
$`B`$ has 3 rows and 2 columns, so $`B`$ is $`3\times 2`$.

**2. Entries.**
- $`a_{12}`$: row 1, column 2 of $`A`$ → $`a_{12}=-1`$.
- $`a_{23}`$: row 2, column 3 of $`A`$ → $`a_{23}=5`$.
- $`b_{21}`$: row 2, column 1 of $`B`$ → $`b_{21}=-2`$.
- $`b_{32}`$: row 3, column 2 of $`B`$ → $`b_{32}=1`$.

**3. Row and column.**
Second row of $`A`$:

```math
r_2(A)=\begin{pmatrix}0&4&5\end{pmatrix}.
```

First column of $`B`$:

```math
c_1(B)=\begin{pmatrix}1\\-2\\4\end{pmatrix}.
```

## Verification and Consistency Checks

- The row vector $`r_2(A)`$ has 3 components, which matches the number of columns of $`A`$ (3).
- The column vector $`c_1(B)`$ has 3 components, which matches the number of rows of $`B`$ (3).
- Indices are valid: for $`A`$ ($`2\times3`$) we need $`i\le 2,\ j\le 3`$; for $`B`$ ($`3\times2`$) we need $`i\le 3,\ j\le 2`$. All requested entries satisfy this.
