# Exercise 9. Cross Product as a Perpendicular Direction

## Problem Statement

For $`u=(1,2,0)`$ and $`v=(0,1,3)`$ compute $`u\times v`$. Use dot products to check perpendicularity to both vectors, compute $`v\times u`$, and compare the results.

## Theoretical Background and Concepts

```math
u\times v=(u_2v_3-u_3v_2,\ u_3v_1-u_1v_3,\ u_1v_2-u_2v_1).
```

- $`u\times v`$ is perpendicular to both $`u`$ and $`v`$; its length is the area of the parallelogram spanned by $`u,v`$.
- **Anticommutativity:** $`v\times u=-(u\times v)`$ (the direction is given by the right-hand rule).

## Detailed Step-by-Step Solution

```math
u\times v=(2\cdot3-0\cdot1,\ 0\cdot0-1\cdot3,\ 1\cdot1-2\cdot0)=(6,-3,1).
```

**Perpendicularity:**
- $`(u\times v)\cdot u=6\cdot1+(-3)\cdot2+1\cdot0=0`$ ✓
- $`(u\times v)\cdot v=6\cdot0+(-3)\cdot1+1\cdot3=0`$ ✓

**Reversed order:**

```math
v\times u=(1\cdot0-3\cdot2,\ 3\cdot0-0\cdot0,\ 0\cdot2-1\cdot1)=(-6,3,-1)=-(u\times v).
```

**Comparison:** both vectors lie on the same line (perpendicular to $`u`$ and $`v`$) and have the same length, but they point in **opposite** directions.

## Verification and Consistency Checks

- $`\|u\times v\|^2=36+9+1=46`$, and $`\|u\|^2\|v\|^2-(u\cdot v)^2=5\cdot10-2^2=46`$ ✓ (Lagrange's identity).
