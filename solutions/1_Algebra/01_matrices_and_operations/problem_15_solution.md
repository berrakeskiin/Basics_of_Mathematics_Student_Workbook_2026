# Exercise 15. Associativity of Multiplication and Different Calculation Paths

## Problem Statement

Given

```math
A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\quad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix},\quad C=\begin{pmatrix}2&1\\0&-1\end{pmatrix}.
```

Compute $`(AB)C`$ and $`A(BC)`$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

## Theoretical Background and Concepts

- **Associativity:** $`(AB)C=A(BC)`$ whenever the products are defined. This means we can write $`ABC`$ without parentheses.
- The **result** does not depend on the grouping, but the **amount of work** can. Multiplying an $`m\times n`$ matrix by an $`n\times p`$ matrix requires $`m\cdot n\cdot p`$ scalar multiplications.

## Detailed Step-by-Step Solution

Sizes: $`A`$ is $`2\times3`$, $`B`$ is $`3\times2`$, $`C`$ is $`2\times2`$, so $`ABC`$ is $`2\times2`$.

**Path 1: $`(AB)C`$**

```math
AB=\begin{pmatrix}1+4+0&0+2+0\\0+2-1&0+1+3\end{pmatrix}=\begin{pmatrix}5&2\\1&4\end{pmatrix},
```

```math
(AB)C=\begin{pmatrix}5\cdot2+2\cdot0&5\cdot1+2\cdot(-1)\\1\cdot2+4\cdot0&1\cdot1+4\cdot(-1)\end{pmatrix}=\begin{pmatrix}10&3\\2&-3\end{pmatrix}.
```

**Path 2: $`A(BC)`$**

```math
BC=\begin{pmatrix}2&1\\4&2-1\\-2&-1-3\end{pmatrix}=\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix},
```

```math
A(BC)=\begin{pmatrix}2+8+0&1+2+0\\0+4-2&0+1-4\end{pmatrix}=\begin{pmatrix}10&3\\2&-3\end{pmatrix}.
```

**Results are equal:** $`(AB)C=A(BC)=\begin{pmatrix}10&3\\2&-3\end{pmatrix}`$.

**Number of scalar multiplications:**
- $`(AB)C`$: $`AB`$ costs $`2\cdot3\cdot2=12`$, then $`(AB)C`$ costs $`2\cdot2\cdot2=8`$, so **20** in total.
- $`A(BC)`$: $`BC`$ costs $`3\cdot2\cdot2=12`$, then $`A(BC)`$ costs $`2\cdot3\cdot2=12`$, so **24** in total.

The first path is cheaper because its intermediate result $`AB`$ is small ($`2\times2`$), while $`BC`$ is $`3\times2`$.

**Meaning of associativity here:** whether we first combine $`A`$ with $`B`$ or $`B`$ with $`C`$, the final matrix is the same. In terms of transformations, $`ABC`$ means "apply $`C`$, then $`B`$, then $`A`$", and grouping does not change this order. Only the order of the factors matters, not the parentheses.

## Verification and Consistency Checks

- Both paths give identical entries. ✓
- Size checks: $`AB`$ is $`2\times2`$, $`BC`$ is $`3\times2`$, and both final results are $`2\times2`$. ✓
- Check one entry directly with a triple sum: $`(ABC)_{11}=\sum_{k,l}a_{1k}b_{kl}c_{l1}=(1\cdot1+2\cdot2+0)\cdot2+(0+2\cdot1+0)\cdot0=10`$. ✓
