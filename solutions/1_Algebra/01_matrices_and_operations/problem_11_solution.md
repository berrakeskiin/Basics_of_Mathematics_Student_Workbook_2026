# Exercise 11. When Do Matrices Commute?

## Problem Statement

Given

```math
A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}a&b\\c&d\end{pmatrix}.
```

Find the conditions on $`a,b,c,d`$ under which $`AB=BA`$. Describe the general form of all such matrices $`B`$.

## Theoretical Background and Concepts

- Two matrices commute if $`AB=BA`$. In general this fails, but certain matrices do commute with a given $`A`$ (for example $`I`$, $`A`$ itself, and every polynomial in $`A`$).
- Method: compute both products and compare them entry by entry. This gives a system of equations in $`a,b,c,d`$.

## Detailed Step-by-Step Solution

```math
AB=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix}=\begin{pmatrix}a+c&b+d\\c&d\end{pmatrix},
```

```math
BA=\begin{pmatrix}a&b\\c&d\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}a&a+b\\c&c+d\end{pmatrix}.
```

Compare entries:
- $`(1,1)`$: $`a+c=a\Rightarrow c=0`$
- $`(1,2)`$: $`b+d=a+b\Rightarrow d=a`$
- $`(2,1)`$: $`c=c`$ (always true)
- $`(2,2)`$: $`d=c+d\Rightarrow c=0`$

**Conditions:** $`c=0`$ and $`d=a`$; $`a`$ and $`b`$ are arbitrary.

**General form:**

```math
B=\begin{pmatrix}a&b\\0&a\end{pmatrix}=aI+b\begin{pmatrix}0&1\\0&0\end{pmatrix}=(a-b)I+bA,\qquad a,b\in\mathbb R.
```

So exactly the matrices of the form $`\alpha I+\beta A`$ commute with $`A`$.

## Verification and Consistency Checks

- Take $`a=2,\ b=5`$: $`B=\begin{pmatrix}2&5\\0&2\end{pmatrix}`$. Then $`AB=\begin{pmatrix}2&7\\0&2\end{pmatrix}`$ and $`BA=\begin{pmatrix}2&7\\0&2\end{pmatrix}`$. ✓
- Counter-check with $`c\ne0`$: $`B=\begin{pmatrix}1&0\\1&1\end{pmatrix}`$ gives $`AB=\begin{pmatrix}2&1\\1&1\end{pmatrix}`$ and $`BA=\begin{pmatrix}1&1\\1&2\end{pmatrix}`$, which are not equal, as predicted. ✓
- Special cases $`B=I`$ ($`a=1,b=0`$) and $`B=A`$ ($`a=1,b=1`$) are included. ✓
