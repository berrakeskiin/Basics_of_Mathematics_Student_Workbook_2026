# Exercise 4. Gauss–Jordan

## Problem Statement

Find $`A^{-1}`$ using the Gauss–Jordan method for

```math
A=\begin{pmatrix}1&2\\3&5\end{pmatrix}.
```

Show the augmented matrix $`[A\mid I]`$ after successive operations and explain why obtaining $`I`$ on the left gives the inverse on the right.

## Theoretical Background and Concepts

- Each row operation equals multiplication from the left by an elementary matrix $`E`$.
- If $`E_k\cdots E_1A=I`$, then $`E_k\cdots E_1=A^{-1}`$. Applying the same operations to $`I`$ gives $`E_k\cdots E_1I=A^{-1}`$. So $`[A\mid I]\to[I\mid A^{-1}]`$.

## Detailed Step-by-Step Solution

```math
\left[\begin{array}{cc|cc}1&2&1&0\\3&5&0&1\end{array}\right]
```

$`R_2\leftarrow R_2-3R_1`$:

```math
\left[\begin{array}{cc|cc}1&2&1&0\\0&-1&-3&1\end{array}\right]
```

$`R_2\leftarrow -R_2`$:

```math
\left[\begin{array}{cc|cc}1&2&1&0\\0&1&3&-1\end{array}\right]
```

$`R_1\leftarrow R_1-2R_2`$:

```math
\left[\begin{array}{cc|cc}1&0&-5&2\\0&1&3&-1\end{array}\right]
```

```math
A^{-1}=\begin{pmatrix}-5&2\\3&-1\end{pmatrix}.
```

**Why it works:** the operations that turned $`A`$ into $`I`$ are exactly "multiplication by $`A^{-1}`$". The same operations applied to $`I`$ therefore produce $`A^{-1}I=A^{-1}`$.

## Verification and Consistency Checks

```math
AA^{-1}=\begin{pmatrix}1&2\\3&5\end{pmatrix}\begin{pmatrix}-5&2\\3&-1\end{pmatrix}=\begin{pmatrix}-5+6&2-2\\-15+15&6-5\end{pmatrix}=I.
```

✓ The $`2\times2`$ formula gives the same: $`\det A=-1`$, $`\frac1{-1}\begin{pmatrix}5&-2\\-3&1\end{pmatrix}=\begin{pmatrix}-5&2\\3&-1\end{pmatrix}`$. ✓
