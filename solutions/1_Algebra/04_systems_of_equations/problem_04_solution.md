# Exercise 4. Infinitely Many Solutions

## Problem Statement

Solve

```math
\begin{cases}x+y+z=2,\\2x+2y+2z=4,\\x-y+z=0.\end{cases}
```

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point satisfies the system.

## Theoretical Background and Concepts

- If after elimination there are fewer pivots than unknowns and no contradiction, the system has **infinitely many** solutions.
- Variables without a pivot are **free**; we denote them by parameters.

## Detailed Step-by-Step Solution

```math
\left[\begin{array}{ccc|c}1&1&1&2\\2&2&2&4\\1&-1&1&0\end{array}\right]
```

$`R_2\leftarrow R_2-2R_1`$ (gives a zero row), $`R_3\leftarrow R_3-R_1`$:

```math
\left[\begin{array}{ccc|c}1&1&1&2\\0&0&0&0\\0&-2&0&-2\end{array}\right]
```

From the third row: $`-2y=-2\Rightarrow y=1`$. From the first row: $`x+1+z=2\Rightarrow x+z=1`$.

The variable $`z`$ has no pivot, so it is **free**: $`z=t`$.

```math
(x,y,z)=(1-t,\ 1,\ t),\qquad t\in\mathbb R.
```

## Verification and Consistency Checks

Take $`t=2`$: $`(x,y,z)=(-1,1,2)`$.
- $`-1+1+2=2`$ ✓
- $`-2+2+4=4`$ ✓
- $`-1-1+2=0`$ ✓

The second equation is just 2 times the first, so it gives no new information; that is why one variable remains free.
