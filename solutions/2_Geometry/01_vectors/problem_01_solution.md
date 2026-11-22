# Exercise 1. Vector Operations and Their Meaning

## Problem Statement

For $`u=(2,-1,3)`$ and $`v=(-1,4,2)`$ compute $`u+v`$, $`u-v`$, $`3u-2v`$. Then verify that $`(u+v)-v=u`$, and explain geometrically what adding two vectors means.

## Theoretical Background and Concepts

- Vectors are added and multiplied by scalars **coordinate by coordinate**: $`(u_1,u_2,u_3)+(v_1,v_2,v_3)=(u_1+v_1,u_2+v_2,u_3+v_3)`$, $`c\,u=(cu_1,cu_2,cu_3)`$.
- **Geometric meaning:** $`u+v`$ is obtained by placing the start of $`v`$ at the end of $`u`$ (triangle rule), or as the diagonal of the parallelogram built on $`u`$ and $`v`$.

## Detailed Step-by-Step Solution

```math
u+v=(2-1,\ -1+4,\ 3+2)=(1,3,5).
```

```math
u-v=(2+1,\ -1-4,\ 3-2)=(3,-5,1).
```

```math
3u-2v=(6,-3,9)-(-2,8,4)=(8,-11,5).
```

**Check:**

```math
(u+v)-v=(1,3,5)-(-1,4,2)=(2,-1,3)=u.
```

**Geometric meaning:** moving first by $`u`$ and then by $`v`$ ends at the same point as moving once by $`u+v`$. Subtracting $`v`$ again moves back along $`v`$, which returns us to the end of $`u`$.

## Verification and Consistency Checks

- $`(u+v)+(u-v)=(4,-2,6)=2u`$ ✓.
- $`3u-2v`$ check of one coordinate: second coordinate $`3\cdot(-1)-2\cdot4=-11`$ ✓.
