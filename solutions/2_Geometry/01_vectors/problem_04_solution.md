# Exercise 4. Dot Product and Perpendicularity

## Problem Statement

For $`u=(1,2,-1)`$ and $`v=(2,-1,3)`$ compute $`u\cdot v`$ and determine whether the vectors are perpendicular. Then find $`a`$ so that $`w=(2,-1,a)`$ is perpendicular to $`u`$, and check the result.

## Theoretical Background and Concepts

- Dot product: $`u\cdot v=u_1v_1+u_2v_2+u_3v_3`$.
- Nonzero vectors are **perpendicular** $`\iff u\cdot v=0`$ (because $`u\cdot v=\|u\|\|v\|\cos\theta`$ and $`\cos90^\circ=0`$).

## Detailed Step-by-Step Solution

```math
u\cdot v=1\cdot2+2\cdot(-1)+(-1)\cdot3=2-2-3=-3\neq0.
```

**The vectors are not perpendicular** (the negative value means the angle is obtuse).

**Condition for $`w`$:**

```math
u\cdot w=1\cdot2+2\cdot(-1)+(-1)\cdot a=2-2-a=-a=0\ \Rightarrow\ a=0.
```

So $`w=(2,-1,0)`$.

## Verification and Consistency Checks

- $`u\cdot w=2-2+0=0`$ ✓.
- For another value, e.g. $`a=1`$: $`u\cdot w=-1\neq0`$, so $`a=0`$ is the only solution. ✓
