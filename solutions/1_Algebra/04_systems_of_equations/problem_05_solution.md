# Exercise 5. Row Echelon Form and Number of Solutions

## Problem Statement

For the augmented matrix

```math
\left[\begin{array}{ccc|c}1&2&-1&3\\0&1&2&1\\0&0&0&0\end{array}\right]
```

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## Theoretical Background and Concepts

- The matrix is already in row echelon form. There is no row $`[0\ 0\ 0\mid c]`$ with $`c\neq0`$, so the system is **consistent**.
- Number of free variables = number of unknowns $`-`$ number of pivots.

## Detailed Step-by-Step Solution

Pivots are in columns 1 ($`x`$) and 2 ($`y`$). There are 3 unknowns and 2 pivots, so $`3-2=1`$ free variable: $`z`$. Therefore the system has **infinitely many solutions** (a one-parameter family).

Let $`z=t`$. Second row: $`y+2t=1\Rightarrow y=1-2t`$.

First row: $`x+2y-z=3\Rightarrow x=3-2(1-2t)+t=3-2+4t+t=1+5t`$.

```math
(x,y,z)=(1+5t,\ 1-2t,\ t)=(1,1,0)+t\,(5,-2,1),\qquad t\in\mathbb R.
```

Geometrically, this is a line in $`\mathbb R^3`$.

## Verification and Consistency Checks

Take $`t=1`$: $`(6,-1,1)`$.
- Row 1: $`6+2(-1)-1=3`$ ✓
- Row 2: $`-1+2\cdot1=1`$ ✓
- Row 3: $`0=0`$ ✓
