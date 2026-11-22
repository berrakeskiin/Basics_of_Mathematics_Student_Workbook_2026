# Exercise 7. Linear Dependence Without Heavy Computation

## Problem Statement

Given $`u=(1,2,3)`$, $`v=(2,4,6)`$, $`w=(0,1,1)`$. Identify a specific relation between $`u`$ and $`v`$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

## Theoretical Background and Concepts

- Vectors $`u,v,w`$ are **linearly dependent** if there are numbers $`\alpha,\beta,\gamma`$, not all zero, with $`\alpha u+\beta v+\gamma w=0`$.
- If two of the vectors are already dependent, the whole set is dependent (we can take the third coefficient equal to $`0`$).

## Detailed Step-by-Step Solution

**Relation:** $`v=(2,4,6)=2\cdot(1,2,3)=2u`$.

Therefore

```math
2u-1\cdot v+0\cdot w=(0,0,0),
```

with coefficients $`(2,-1,0)`$, which are not all zero. **The vectors are linearly dependent**, so they cannot be independent, whatever $`w`$ is.

**Why no long calculation is needed:** one nontrivial combination equal to zero is enough to prove dependence, and the relation $`v=2u`$ is visible directly from the coordinates.

## Verification and Consistency Checks

- Determinant check: $`\det\begin{pmatrix}1&2&3\\2&4&6\\0&1&1\end{pmatrix}=1(4-6)-2(2-0)+3(2-0)=-2-4+6=0`$ ✓ (zero determinant $`\iff`$ dependent rows).
- Geometrically, $`u`$ and $`v`$ lie on one line, so the three vectors span at most a plane, not all of $`\mathbb R^3`$.
