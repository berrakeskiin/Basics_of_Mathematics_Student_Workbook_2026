# Exercise 15. Classifying Three Systems

## Problem Statement

For each system, perform only as much elimination as necessary to recognize its type:

1. $`\begin{cases}x+y=2,\\x-y=0,\end{cases}`$
2. $`\begin{cases}x+y=2,\\2x+2y=4,\end{cases}`$
3. $`\begin{cases}x+y=2,\\2x+2y=5.\end{cases}`$

Justify each classification: one solution, infinitely many solutions, or no solution.

## Theoretical Background and Concepts

After elimination:
- every unknown has a pivot $`\Rightarrow`$ **one solution**;
- a row $`0=0`$ and a free variable, no contradiction $`\Rightarrow`$ **infinitely many**;
- a row $`0=c`$ with $`c\neq0`$ $`\Rightarrow`$ **no solution**.

## Detailed Step-by-Step Solution

**System 1:** $`R_2\leftarrow R_2-R_1`$:

```math
\left[\begin{array}{cc|c}1&1&2\\0&-2&-2\end{array}\right]
```

Two pivots, no contradiction $`\Rightarrow`$ **exactly one solution**: $`y=1`$, $`x=1`$.

**System 2:** $`R_2\leftarrow R_2-2R_1`$:

```math
\left[\begin{array}{cc|c}1&1&2\\0&0&0\end{array}\right]
```

The second equation is 2 times the first; one free variable $`\Rightarrow`$ **infinitely many solutions**: $`(2-t,\ t)`$.

**System 3:** $`R_2\leftarrow R_2-2R_1`$:

```math
\left[\begin{array}{cc|c}1&1&2\\0&0&1\end{array}\right]
```

The row means $`0=1`$ $`\Rightarrow`$ **no solution** (parallel distinct lines).

## Verification and Consistency Checks

- System 1: $`(1,1)`$: $`1+1=2`$ ✓, $`1-1=0`$ ✓.
- System 2: $`t=0`$ gives $`(2,0)`$: $`2=2`$ ✓, $`4=4`$ ✓.
- System 3: $`2x+2y=2(x+y)=4\neq5`$ whenever $`x+y=2`$, so no point works ✓.
