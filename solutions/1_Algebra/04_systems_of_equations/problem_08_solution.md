# Exercise 8. Two Systems with the Same Coefficient Matrix

## Problem Statement

Solve by elimination the two systems

```math
\begin{cases}2x+y=5,\\x-y=1,\end{cases}\qquad\qquad \begin{cases}2x+y=1,\\x-y=4.\end{cases}
```

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## Theoretical Background and Concepts

- Row operations are chosen by looking only at the **coefficient matrix** $`A`$. The right-hand side just follows along.
- Therefore systems with the same $`A`$ can be solved together using $`[A\mid b_1\ b_2]`$.

## Detailed Step-by-Step Solution

Both systems have $`A=\begin{pmatrix}2&1\\1&-1\end{pmatrix}`$. Solve them together, swapping the rows first:

```math
\left[\begin{array}{cc|cc}1&-1&1&4\\2&1&5&1\end{array}\right]\xrightarrow{R_2-2R_1}\left[\begin{array}{cc|cc}1&-1&1&4\\0&3&3&-7\end{array}\right].
```

**System 1:** $`3y=3\Rightarrow y=1`$, $`x=1+y=2`$. Solution $`(2,1)`$.

**System 2:** $`3y=-7\Rightarrow y=-\frac73`$, $`x=4+y=\frac53`$. Solution $`\left(\frac53,-\frac73\right)`$.

**What is the same:** the operations ($`R_1\leftrightarrow R_2`$, then $`R_2-2R_1`$) and the resulting left part $`\begin{pmatrix}1&-1\\0&3\end{pmatrix}`$ are identical, because they depend only on $`A`$. Only the right-hand column values differ.

## Verification and Consistency Checks

- System 1: $`2\cdot2+1=5`$ ✓, $`2-1=1`$ ✓.
- System 2: $`2\cdot\frac53-\frac73=\frac{10-7}3=1`$ ✓, $`\frac53+\frac73=4`$ ✓.
