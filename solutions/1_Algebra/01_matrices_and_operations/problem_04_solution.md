# Exercise 4. Matrix Multiplication and Noncommutativity

## Problem Statement

For

```math
A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\3&1\end{pmatrix}
```

compute $`AB`$ and $`BA`$. Is $`AB=BA`$? Use this example to explain what noncommutativity of matrix multiplication means.

## Theoretical Background and Concepts

- Matrix product: $`(AB)_{ij}=\sum_k a_{ik}b_{kj}`$ ("row $`i`$ of $`A`$ times column $`j`$ of $`B`$").
- For numbers $`xy=yx`$ always. For matrices this is **not** true in general: multiplication is **noncommutative**. It is enough to show one example where $`AB\neq BA`$.

## Detailed Step-by-Step Solution

**$`AB`$:**
- $`(1,1)`$: $`1\cdot2+2\cdot3=8`$
- $`(1,2)`$: $`1\cdot0+2\cdot1=2`$
- $`(2,1)`$: $`0\cdot2+1\cdot3=3`$
- $`(2,2)`$: $`0\cdot0+1\cdot1=1`$

```math
AB=\begin{pmatrix}8&2\\3&1\end{pmatrix}.
```

**$`BA`$:**
- $`(1,1)`$: $`2\cdot1+0\cdot0=2`$
- $`(1,2)`$: $`2\cdot2+0\cdot1=4`$
- $`(2,1)`$: $`3\cdot1+1\cdot0=3`$
- $`(2,2)`$: $`3\cdot2+1\cdot1=7`$

```math
BA=\begin{pmatrix}2&4\\3&7\end{pmatrix}.
```

**Comparison:** $`AB\neq BA`$ (for example $`(AB)_{11}=8`$ but $`(BA)_{11}=2`$).

**Meaning:** noncommutativity means that the order of the factors matters: in general $`AB\ne BA`$, even when both products are defined and have the same size. So when working with matrices we must keep the order of factors, e.g. $`(A+B)^2=A^2+AB+BA+B^2`$, which is not $`A^2+2AB+B^2`$ unless $`AB=BA`$.

## Verification and Consistency Checks

- Determinant check: $`\det A=1`$, $`\det B=2`$. Then $`\det(AB)=8\cdot1-2\cdot3=2`$ and $`\det(BA)=2\cdot7-4\cdot3=2`$. Both equal $`\det A\cdot\det B=2`$. ✓
- Trace check: $`\operatorname{tr}(AB)=8+1=9`$ and $`\operatorname{tr}(BA)=2+7=9`$. They are equal, as they must be ($`\operatorname{tr}(AB)=\operatorname{tr}(BA)`$ always), even though the matrices are different. ✓
