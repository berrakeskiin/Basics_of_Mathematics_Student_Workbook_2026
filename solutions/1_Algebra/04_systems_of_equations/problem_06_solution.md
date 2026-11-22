# Exercise 6. A System with a Parameter — Which Cases Actually Occur?

## Problem Statement

Analyze, depending on the parameter $`a`$, the system

```math
\begin{cases}x+y=2,\\ax+ay=4.\end{cases}
```

Among the three possibilities (exactly one solution, infinitely many, no solution), determine which actually occur and for which $`a`$. If one type cannot occur, explain why.

## Theoretical Background and Concepts

- A unique solution requires $`\det A\neq0`$.
- If $`\det A=0`$, elimination gives either a contradiction $`0=c\neq0`$ (no solution) or $`0=0`$ (infinitely many).

## Detailed Step-by-Step Solution

```math
\det\begin{pmatrix}1&1\\a&a\end{pmatrix}=a-a=0\quad\text{for every }a.
```

So **exactly one solution never occurs**: the second left-hand side $`a(x+y)`$ is always a multiple of the first.

Elimination $`R_2\leftarrow R_2-aR_1`$:

```math
\left[\begin{array}{cc|c}1&1&2\\a&a&4\end{array}\right]\to\left[\begin{array}{cc|c}1&1&2\\0&0&4-2a\end{array}\right].
```

- **$`a=2`$:** last row is $`0=0`$. The second equation is $`2x+2y=4`$, the same as the first. **Infinitely many solutions:** $`(x,y)=(2-t,\ t)`$, $`t\in\mathbb R`$.
- **$`a\neq2`$:** last row is $`0=4-2a\neq0`$, a contradiction. **No solution.** (For example $`a=0`$ gives $`0=4`$; $`a=1`$ gives $`x+y=4`$ together with $`x+y=2`$.)

**Summary:** infinitely many solutions for $`a=2`$; no solution for $`a\neq2`$; a unique solution is impossible.

## Verification and Consistency Checks

- $`a=2`$, $`t=0`$: $`(2,0)`$ gives $`2=2`$ and $`4=4`$ ✓.
- $`a=3`$: if $`x+y=2`$, then $`3x+3y=6\neq4`$, so no solution ✓.
