# Exercise 6. Transpose

## Problem Statement

For

```math
A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}
```

compute $`A^T`$, $`B^T`$, and $`AB`$. Then verify in this example that $`(AB)^T=B^TA^T`$.

## Theoretical Background and Concepts

- The **transpose** swaps rows and columns: $`(A^T)_{ij}=a_{ji}`$. If $`A`$ is $`m\times n`$, then $`A^T`$ is $`n\times m`$.
- Property: $`(AB)^T=B^TA^T`$. The order of the factors is **reversed**. (Sizes: $`(AB)^T`$ is $`p\times m`$ when $`A`$ is $`m\times n`$ and $`B`$ is $`n\times p`$. $`B^T A^T`$ is $`(p\times n)(n\times m)=p\times m`$, which matches.)

## Detailed Step-by-Step Solution

**Transposes:**

```math
A^T=\begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix}\ (3\times2),\qquad B^T=\begin{pmatrix}1&2&-1\\0&1&3\end{pmatrix}\ (2\times3).
```

**Product $`AB`$** ($`2\times3`$ times $`3\times2`$ gives $`2\times2`$):
- $`(1,1)`$: $`1\cdot1+2\cdot2+3\cdot(-1)=1+4-3=2`$
- $`(1,2)`$: $`1\cdot0+2\cdot1+3\cdot3=0+2+9=11`$
- $`(2,1)`$: $`4\cdot1+5\cdot2+6\cdot(-1)=4+10-6=8`$
- $`(2,2)`$: $`4\cdot0+5\cdot1+6\cdot3=0+5+18=23`$

```math
AB=\begin{pmatrix}2&11\\8&23\end{pmatrix},\qquad (AB)^T=\begin{pmatrix}2&8\\11&23\end{pmatrix}.
```

**Product $`B^TA^T`$** ($`2\times3`$ times $`3\times2`$ gives $`2\times2`$):
- $`(1,1)`$: $`1\cdot1+2\cdot2+(-1)\cdot3=2`$
- $`(1,2)`$: $`1\cdot4+2\cdot5+(-1)\cdot6=8`$
- $`(2,1)`$: $`0\cdot1+1\cdot2+3\cdot3=11`$
- $`(2,2)`$: $`0\cdot4+1\cdot5+3\cdot6=23`$

```math
B^TA^T=\begin{pmatrix}2&8\\11&23\end{pmatrix}.
```

So $`(AB)^T=B^TA^T`$. ✓

## Verification and Consistency Checks

- Transposing twice gives back the original: $`(A^T)^T=A`$. ✓
- Note that $`A^TB^T`$ is $`(3\times2)(2\times3)=3\times3`$, which has a different size from $`(AB)^T`$ ($`2\times2`$). This shows why the order **must** be reversed.
