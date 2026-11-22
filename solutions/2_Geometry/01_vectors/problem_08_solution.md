# Exercise 8. Linear Combination and Checking the Result

## Problem Statement

Check whether $`w=(5,1)`$ can be written as $`w=au+bv`$, where $`u=(1,1)`$ and $`v=(2,-1)`$. If so, find $`a,b`$, reconstruct $`w`$, and explain the geometric meaning of the existence of such coefficients.

## Theoretical Background and Concepts

- $`w=au+bv`$ is a linear system in $`a,b`$ (one equation per coordinate).
- If $`u,v`$ are not parallel ($`\det[\,u\ v\,]\neq0`$), every vector of $`\mathbb R^2`$ can be written uniquely in this way: $`u,v`$ form a **basis** of the plane.

## Detailed Step-by-Step Solution

```math
a(1,1)+b(2,-1)=(5,1)\iff\begin{cases}a+2b=5,\\a-b=1.\end{cases}
```

Subtracting the second equation from the first: $`3b=4\Rightarrow b=\frac43`$. Then $`a=1+b=\frac73`$.

**Answer:** yes, $`w=\frac73u+\frac43v`$.

**Reconstruction:**

```math
\tfrac73(1,1)+\tfrac43(2,-1)=\left(\tfrac73+\tfrac83,\ \tfrac73-\tfrac43\right)=(5,1)=w.
```

**Geometric meaning:** $`u`$ and $`v`$ point in different directions ($`\det\begin{pmatrix}1&2\\1&-1\end{pmatrix}=-3\neq0`$), so they form a slanted coordinate grid of the plane. The numbers $`a=\frac73`$, $`b=\frac43`$ are the coordinates of $`w`$ in this grid: go $`\frac73`$ steps along $`u`$ and $`\frac43`$ steps along $`v`$.

## Verification and Consistency Checks

- First coordinate: $`\frac73+2\cdot\frac43=\frac{15}3=5`$ ✓; second: $`\frac73-\frac43=1`$ ✓.
