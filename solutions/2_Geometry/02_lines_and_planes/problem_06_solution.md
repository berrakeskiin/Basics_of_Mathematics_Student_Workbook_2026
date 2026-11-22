# Exercise 6. Angle Between Planes

## Problem Statement

Given

```math
\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.
```

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough.

## Theoretical Background and Concepts

- The coefficients of $`x,y,z`$ form a normal vector: $`n_1=(1,1,1)`$, $`n_2=(1,-1,0)`$.
- Planes are **parallel** $`\iff`$ their normals are parallel.
- The angle between planes equals the (acute) angle between their normals: $`\cos\varphi=\dfrac{|n_1\cdot n_2|}{\|n_1\|\,\|n_2\|}`$.

## Detailed Step-by-Step Solution

**Parallel?** $`n_2`$ has third coordinate $`0`$ while $`n_1`$ has $`1`$, so $`n_1`$ is not a multiple of $`n_2`$. **Not parallel.**

**Angle:**

```math
n_1\cdot n_2=1\cdot1+1\cdot(-1)+1\cdot0=0\ \Rightarrow\ \cos\varphi=0\ \Rightarrow\ \varphi=90^\circ.
```

The planes are **perpendicular**.

**Why normals are enough:** each plane is completely "tilted" according to its normal. Rotating one plane into the other means rotating one normal into the other by the same angle. The position (the constants $`1`$ and $`2`$) only shifts the planes and does not change the angle.

## Verification and Consistency Checks

- A vector lying in $`\Pi_2`$, e.g. $`(1,1,0)`$ (since $`1-1=0`$), is parallel to $`n_1`$'s projection... more simply: $`n_2=(1,-1,0)`$ lies in the direction space of $`\Pi_1`$ because $`n_1\cdot n_2=0`$. A plane containing the normal direction of another plane is perpendicular to it. ✓
