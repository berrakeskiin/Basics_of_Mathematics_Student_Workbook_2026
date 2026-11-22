# Exercise 12. Intersection Line of Two Planes

## Problem Statement

Find a parametric equation of the line of intersection of

```math
x+y+z=3,\qquad x-y+z=1.
```

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

## Theoretical Background and Concepts

- The intersection line consists of the solutions of the $`2\times3`$ system; one variable is free.
- The direction lies in both planes, so it is perpendicular to both normals; hence it is parallel to $`n_1\times n_2`$.

## Detailed Step-by-Step Solution

**Way 1 (system):** subtracting the equations: $`2y=2\Rightarrow y=1`$. Then $`x+z=2`$. Let $`z=t`$:

```math
(x,y,z)=(2-t,\ 1,\ t)=(2,1,0)+t(-1,0,1).
```

Direction from the system: $`(-1,0,1)`$.

**Way 2 (cross product):** $`n_1=(1,1,1)`$, $`n_2=(1,-1,1)`$:

```math
n_1\times n_2=\big(1\cdot1-1\cdot(-1),\ 1\cdot1-1\cdot1,\ 1\cdot(-1)-1\cdot1\big)=(2,0,-2).
```

**Comparison:** $`(2,0,-2)=-2\cdot(-1,0,1)`$. The vectors are parallel, so both ways describe the same direction (length and orientation of a direction vector do not matter).

## Verification and Consistency Checks

- Point $`(2,1,0)`$: $`2+1+0=3`$ ✓ and $`2-1+0=1`$ ✓.
- Any $`t`$: $`(2-t)+1+t=3`$ ✓ and $`(2-t)-1+t=1`$ ✓.
