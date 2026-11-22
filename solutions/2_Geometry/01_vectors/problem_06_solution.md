# Exercise 6. Projection and Perpendicular Component

## Problem Statement

Find the projection of $`u=(4,2)`$ onto the direction $`v=(1,1)`$. Then compute $`r=u-\mathrm{proj}_v u`$ and verify that $`r\cdot v=0`$. Explain this result geometrically.

## Theoretical Background and Concepts

```math
\mathrm{proj}_v u=\frac{u\cdot v}{v\cdot v}\,v.
```

- $`\mathrm{proj}_v u`$ is the part of $`u`$ parallel to $`v`$; $`r=u-\mathrm{proj}_v u`$ is the part perpendicular to $`v`$.

## Detailed Step-by-Step Solution

```math
u\cdot v=4+2=6,\qquad v\cdot v=1+1=2,\qquad \mathrm{proj}_v u=\frac62(1,1)=(3,3).
```

```math
r=u-\mathrm{proj}_v u=(4,2)-(3,3)=(1,-1).
```

```math
r\cdot v=1\cdot1+(-1)\cdot1=0.
```

**Geometric meaning:** $`\mathrm{proj}_v u`$ is the "shadow" of $`u`$ on the line spanned by $`v`$ when light falls perpendicularly. The remaining part $`r`$ goes straight from that shadow to the tip of $`u`$, so it must be perpendicular to the line. Thus $`u=(3,3)+(1,-1)`$ splits $`u`$ into a parallel and a perpendicular part.

## Verification and Consistency Checks

- $`(3,3)+(1,-1)=(4,2)=u`$ ✓.
- Pythagoras: $`\|u\|^2=20`$, $`\|(3,3)\|^2+\|(1,-1)\|^2=18+2=20`$ ✓.
