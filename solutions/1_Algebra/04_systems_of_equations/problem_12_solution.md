# Exercise 12. Homogeneous System

## Problem Statement

Solve

```math
\begin{cases}x+2y-z=0,\\2x+4y-2z=0,\\x-y+2z=0.\end{cases}
```

Give all solutions in parametric form and explain why $`(0,0,0)`$ always satisfies a homogeneous system.

## Theoretical Background and Concepts

- A system is **homogeneous** if all right-hand sides are $`0`$: $`Ax=0`$.
- $`x=0`$ is always a solution because $`A\cdot0=0`$. A homogeneous system is therefore never inconsistent: it has either only the zero solution or infinitely many.

## Detailed Step-by-Step Solution

```math
\begin{pmatrix}1&2&-1\\2&4&-2\\1&-1&2\end{pmatrix}\xrightarrow{R_2-2R_1,\ R_3-R_1}\begin{pmatrix}1&2&-1\\0&0&0\\0&-3&3\end{pmatrix}.
```

(The right-hand side stays $`0`$, so we omit it.)

Third row: $`-3y+3z=0\Rightarrow y=z`$. Let $`z=t`$ (free), so $`y=t`$.

First row: $`x+2t-t=0\Rightarrow x=-t`$.

```math
(x,y,z)=t\,(-1,1,1),\qquad t\in\mathbb R.
```

The solution set is a line through the origin. For $`t=0`$ we get $`(0,0,0)`$.

**Why $`(0,0,0)`$ always works:** every equation has the form $`a_1x+a_2y+a_3z=0`$; putting $`x=y=z=0`$ gives $`0=0`$.

## Verification and Consistency Checks

Take $`t=1`$: $`(-1,1,1)`$.
- $`-1+2-1=0`$ ✓
- $`-2+4-2=0`$ ✓
- $`-1-1+2=0`$ ✓
