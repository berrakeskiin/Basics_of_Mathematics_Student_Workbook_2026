# Exercise 5. Relative Position of Two Lines

## Problem Statement

Analyze the position of

```math
L_1:(x,y,z)=(1,1,0)+t(1,2,1),\qquad L_2:(x,y,z)=(2,0,1)+s(0,1,-1).
```

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

## Theoretical Background and Concepts

- **Parallel** $`\iff`$ the direction vectors are multiples of each other.
- If not parallel: they **intersect** if the system $`P_1+tv_1=P_2+sv_2`$ has a solution, otherwise they are **skew**.

## Detailed Step-by-Step Solution

**Parallel?** $`v_1=(1,2,1)`$, $`v_2=(0,1,-1)`$. A multiple of $`v_2`$ has first coordinate $`0`$, but $`v_1`$ has $`1`$, so **not parallel**.

**Intersection?** Set the coordinates equal:

```math
\begin{cases}1+t=2,\\1+2t=s,\\t=1-s.\end{cases}
```

From the first equation $`t=1`$. Then the second gives $`s=3`$, but the third gives $`s=1-t=0`$. Contradiction ($`3\neq0`$), so **no common point**.

**Conclusion:** the lines are neither parallel nor intersecting, so they are **skew**.

## Verification and Consistency Checks

- Skew-line test: $`n=v_1\times v_2=(2\cdot(-1)-1\cdot1,\ 1\cdot0-1\cdot(-1),\ 1\cdot1-2\cdot0)=(-3,1,1)`$, $`w=P_2-P_1=(1,-1,1)`$, $`w\cdot n=-3-1+1=-3\neq0`$. Nonzero means the lines do not lie in one plane, confirming "skew". ✓
- Distance between them: $`\frac{|w\cdot n|}{\|n\|}=\frac3{\sqrt{11}}\approx0.90`$.
