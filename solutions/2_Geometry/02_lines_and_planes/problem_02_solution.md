# Exercise 2. A Line in Space

## Problem Statement

Given

```math
L:(x,y,z)=(2,-1,3)+t(1,2,-2).
```

State a point on the line and its direction vector, check whether $`P=(4,3,-1)`$ lies on $`L`$, and find the point corresponding to $`t=-1`$.

## Theoretical Background and Concepts

- Parametric form = **point + parameter $`\cdot`$ direction**: $`P_0+t\,v`$.
- A point lies on the line if **one and the same** value of $`t`$ satisfies all three coordinate equations.

## Detailed Step-by-Step Solution

**Point and direction:** $`P_0=(2,-1,3)`$ (for $`t=0`$), $`v=(1,2,-2)`$.

**Is $`P=(4,3,-1)`$ on $`L`$?**
- $`x`$: $`2+t=4\Rightarrow t=2`$
- $`y`$: $`-1+2t=3\Rightarrow t=2`$
- $`z`$: $`3-2t=-1\Rightarrow t=2`$

All three coordinates give the same $`t=2`$, so **$`P`$ lies on $`L`$**.

**Point for $`t=-1`$:**

```math
(2,-1,3)+(-1)(1,2,-2)=(1,-3,5).
```

## Verification and Consistency Checks

- $`P-P_0=(2,4,-4)=2v`$ ✓, so $`P`$ is reached by moving 2 steps along $`v`$.
- $`(1,-3,5)-P_0=(-1,-2,2)=-v`$ ✓.
