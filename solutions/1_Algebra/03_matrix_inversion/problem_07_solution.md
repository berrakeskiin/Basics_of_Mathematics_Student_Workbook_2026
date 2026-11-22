# Exercise 7. Inverse of a Product

## Problem Statement

For

```math
A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\0&3\end{pmatrix}
```

compute $`(AB)^{-1}`$ and $`B^{-1}A^{-1}`$. Check that the results are the same and explain the meaning of the reversed order.

## Theoretical Background and Concepts

- $`(AB)^{-1}=B^{-1}A^{-1}`$, because $`(AB)(B^{-1}A^{-1})=A(BB^{-1})A^{-1}=AA^{-1}=I`$.
- The order is reversed, like taking off socks and shoes: what was done last is undone first.

## Detailed Step-by-Step Solution

**Way 1:**

```math
AB=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}2&0\\0&3\end{pmatrix}=\begin{pmatrix}2&3\\0&3\end{pmatrix},\qquad \det(AB)=6,
```

```math
(AB)^{-1}=\frac16\begin{pmatrix}3&-3\\0&2\end{pmatrix}=\begin{pmatrix}\frac12&-\frac12\\0&\frac13\end{pmatrix}.
```

**Way 2:**

```math
A^{-1}=\begin{pmatrix}1&-1\\0&1\end{pmatrix},\qquad B^{-1}=\begin{pmatrix}\frac12&0\\0&\frac13\end{pmatrix},
```

```math
B^{-1}A^{-1}=\begin{pmatrix}\frac12&0\\0&\frac13\end{pmatrix}\begin{pmatrix}1&-1\\0&1\end{pmatrix}=\begin{pmatrix}\frac12&-\frac12\\0&\frac13\end{pmatrix}.
```

The results are equal.

**Meaning:** $`ABx`$ means "first apply $`B`$, then $`A`$". To undo it we must first undo $`A`$ (the last step), then undo $`B`$, so the inverse is $`B^{-1}A^{-1}`$.

## Verification and Consistency Checks

```math
(AB)(AB)^{-1}=\begin{pmatrix}2&3\\0&3\end{pmatrix}\begin{pmatrix}\frac12&-\frac12\\0&\frac13\end{pmatrix}=\begin{pmatrix}1&-1+1\\0&1\end{pmatrix}=I.
```

✓ The wrong order $`A^{-1}B^{-1}=\begin{pmatrix}\frac12&-\frac13\\0&\frac13\end{pmatrix}`$ is different, which confirms that the order matters.
