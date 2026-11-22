# Exercise 13. A Recurrence Written in Matrix Form

## Problem Statement

Let

```math
F=\begin{pmatrix}1&1\\1&0\end{pmatrix}.
```

Compute $`F^2,F^3,F^4,F^5`$. Compare the numbers obtained with the sequence $`0,1,1,2,3,5,8,\ldots`$ and describe the relationship. Then compute $`F\begin{pmatrix}a\\b\end{pmatrix}`$ and explain how this multiplication performs one recurrence step.

## Theoretical Background and Concepts

- The **Fibonacci sequence**: $`f_0=0,\ f_1=1,\ f_{n+1}=f_n+f_{n-1}`$, which gives $`0,1,1,2,3,5,8,13,\dots`$
- A linear recurrence of order 2 can be written as a matrix acting on the vector of two consecutive terms. Then $`n`$ steps of the recurrence correspond to the $`n`$-th power of the matrix.

## Detailed Step-by-Step Solution

**Powers:**

```math
F^2=\begin{pmatrix}1&1\\1&0\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}=\begin{pmatrix}2&1\\1&1\end{pmatrix},
```

```math
F^3=F^2F=\begin{pmatrix}2&1\\1&1\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}=\begin{pmatrix}3&2\\2&1\end{pmatrix},
```

```math
F^4=F^3F=\begin{pmatrix}5&3\\3&2\end{pmatrix},\qquad F^5=F^4F=\begin{pmatrix}8&5\\5&3\end{pmatrix}.
```

**Relationship:** all entries are Fibonacci numbers:

```math
F^n=\begin{pmatrix}f_{n+1}&f_n\\f_n&f_{n-1}\end{pmatrix}.
```

For example $`F^5`$ contains $`f_6=8,\ f_5=5,\ f_4=3`$.

**One recurrence step:**

```math
F\begin{pmatrix}a\\b\end{pmatrix}=\begin{pmatrix}1\cdot a+1\cdot b\\1\cdot a+0\cdot b\end{pmatrix}=\begin{pmatrix}a+b\\a\end{pmatrix}.
```

If $`a=f_n`$ and $`b=f_{n-1}`$ (two consecutive terms), the result is $`\begin{pmatrix}f_n+f_{n-1}\\f_n\end{pmatrix}=\begin{pmatrix}f_{n+1}\\f_n\end{pmatrix}`$:
- the first row **creates the sum** of the two terms (the next term),
- the second row **keeps** the previous term $`a`$ for the next step.

So starting from $`\begin{pmatrix}f_1\\f_0\end{pmatrix}=\begin{pmatrix}1\\0\end{pmatrix}`$:

```math
F^n\begin{pmatrix}1\\0\end{pmatrix}=\begin{pmatrix}f_{n+1}\\f_n\end{pmatrix}.
```

## Verification and Consistency Checks

- $`F^5\begin{pmatrix}1\\0\end{pmatrix}=\begin{pmatrix}8\\5\end{pmatrix}=\begin{pmatrix}f_6\\f_5\end{pmatrix}`$. ✓
- Induction step for the formula: $`F^nF=\begin{pmatrix}f_{n+1}+f_n&f_{n+1}\\f_n+f_{n-1}&f_n\end{pmatrix}=\begin{pmatrix}f_{n+2}&f_{n+1}\\f_{n+1}&f_n\end{pmatrix}`$. ✓
- Determinant: $`\det F=-1`$, so $`\det F^n=(-1)^n`$. For $`n=5`$: $`8\cdot3-5\cdot5=-1`$. ✓ (This is Cassini's identity $`f_{n+1}f_{n-1}-f_n^2=(-1)^n`$.)
