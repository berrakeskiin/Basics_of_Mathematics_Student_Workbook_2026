# Exercise 9. A System from a Sum Condition

## Problem Statement

Find numbers $`x,y`$ satisfying

```math
x+y=10,\qquad 2x+5y=32.
```

Solve the system and explain geometrically why the solution is unique.

## Theoretical Background and Concepts

- Each linear equation in $`x,y`$ is a line in the plane; a solution of the system is a common point.
- Two lines with **different slopes** intersect in exactly one point. Equivalently, $`\det A\neq0`$.

## Detailed Step-by-Step Solution

```math
\left[\begin{array}{cc|c}1&1&10\\2&5&32\end{array}\right]\xrightarrow{R_2-2R_1}\left[\begin{array}{cc|c}1&1&10\\0&3&12\end{array}\right].
```

$`3y=12\Rightarrow y=4`$, and $`x=10-4=6`$.

**Solution:** $`(x,y)=(6,4)`$.

**Geometric explanation:** the lines are $`y=-x+10`$ (slope $`-1`$) and $`y=-\frac25x+\frac{32}5`$ (slope $`-\frac25`$). The slopes are different, so the lines are not parallel and meet in exactly one point, $`(6,4)`$. Also $`\det\begin{pmatrix}1&1\\2&5\end{pmatrix}=3\neq0`$.

## Verification and Consistency Checks

- $`6+4=10`$ ✓
- $`2\cdot6+5\cdot4=12+20=32`$ ✓
