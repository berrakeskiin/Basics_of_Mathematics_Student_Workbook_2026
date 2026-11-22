# Exercise 2. Addition and Scalar Multiplication

## Problem Statement

For

```math
A=\begin{pmatrix}1&2\\-1&3\end{pmatrix},\qquad B=\begin{pmatrix}4&-2\\0&5\end{pmatrix}
```

compute $`A+B`$, $`A-B`$, $`3A-2B`$. Explain why matrix addition is possible only for matrices of the same size.

## Theoretical Background and Concepts

- **Addition/subtraction** is done entry by entry: $`(A\pm B)_{ij}=a_{ij}\pm b_{ij}`$.
- **Scalar multiplication** multiplies every entry: $`(kA)_{ij}=k\,a_{ij}`$.
- Because addition pairs each entry of $`A`$ with the entry in the same position in $`B`$, both matrices must have exactly the same positions, i.e. the same size.

## Detailed Step-by-Step Solution

**$`A+B`$:**

```math
A+B=\begin{pmatrix}1+4&2+(-2)\\-1+0&3+5\end{pmatrix}=\begin{pmatrix}5&0\\-1&8\end{pmatrix}.
```

**$`A-B`$:**

```math
A-B=\begin{pmatrix}1-4&2-(-2)\\-1-0&3-5\end{pmatrix}=\begin{pmatrix}-3&4\\-1&-2\end{pmatrix}.
```

**$`3A-2B`$:**

```math
3A=\begin{pmatrix}3&6\\-3&9\end{pmatrix},\qquad 2B=\begin{pmatrix}8&-4\\0&10\end{pmatrix},
```

```math
3A-2B=\begin{pmatrix}3-8&6-(-4)\\-3-0&9-10\end{pmatrix}=\begin{pmatrix}-5&10\\-3&-1\end{pmatrix}.
```

**Why the same size is needed:**
The sum is defined entry by entry. If, for example, $`A`$ were $`2\times2`$ and $`B`$ were $`2\times3`$, then $`B`$ would have entries $`b_{13}, b_{23}`$ with no matching entries in $`A`$, so $`a_{13}+b_{13}`$ would not make sense. Therefore $`A+B`$ is defined only when $`A`$ and $`B`$ have the same number of rows and the same number of columns.

## Verification and Consistency Checks

- Check: $`(A+B)+(A-B)=2A`$:

```math
\begin{pmatrix}5&0\\-1&8\end{pmatrix}+\begin{pmatrix}-3&4\\-1&-2\end{pmatrix}=\begin{pmatrix}2&4\\-2&6\end{pmatrix}=2A.\ \checkmark
```

- Check one entry of $`3A-2B`$ directly: position (1,2): $`3\cdot2-2\cdot(-2)=6+4=10`$. ✓
- All results are $`2\times2`$, the same size as $`A`$ and $`B`$. ✓
