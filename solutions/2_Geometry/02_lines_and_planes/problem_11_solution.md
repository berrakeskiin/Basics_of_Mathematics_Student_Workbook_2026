# Exercise 11. Plane Containing a Line and a Point

## Problem Statement

Find the equation of the plane containing

```math
(x,y,z)=(1,0,2)+t(1,1,-1)
```

and the point $`P=(0,2,1)`$. Check that both the entire line and the point lie in the plane you obtain.

## Theoretical Background and Concepts

- We need two independent directions in the plane: the line direction $`v`$ and the vector $`\overrightarrow{AP}`$ from a point $`A`$ of the line to $`P`$.
- The normal is $`n=v\times\overrightarrow{AP}`$ (this requires $`P`$ not to lie on the line).

## Detailed Step-by-Step Solution

$`A=(1,0,2)`$, $`v=(1,1,-1)`$, $`\overrightarrow{AP}=P-A=(-1,2,-1)`$.

$`P`$ is not on the line: $`\overrightarrow{AP}`$ is not a multiple of $`v`$, so the two directions are independent.

```math
n=v\times\overrightarrow{AP}=\big(1\cdot(-1)-(-1)\cdot2,\ (-1)\cdot(-1)-1\cdot(-1),\ 1\cdot2-1\cdot(-1)\big)=(1,2,3).
```

```math
1\cdot(x-1)+2\cdot(y-0)+3\cdot(z-2)=0\quad\Rightarrow\quad x+2y+3z=7.
```

## Verification and Consistency Checks

- **Point $`P`$:** $`0+4+3=7`$ ✓.
- **Entire line:** $`(1+t)+2t+3(2-t)=1+t+2t+6-3t=7`$ for **every** $`t`$ ✓.
- $`n\cdot v=1+2-3=0`$ and $`n\cdot\overrightarrow{AP}=-1+4-3=0`$ ✓.
