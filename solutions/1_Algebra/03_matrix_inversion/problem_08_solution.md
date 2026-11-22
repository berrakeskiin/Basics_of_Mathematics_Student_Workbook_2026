# Exercise 8. Inverse of a Transformation

## Problem Statement

The matrix

```math
S=\begin{pmatrix}2&0\\0&\frac12\end{pmatrix}
```

describes a scaling of the plane. Find $`S^{-1}`$ and explain geometrically what the inverse transformation does. Check the action of the pair $`S,S^{-1}`$ on one simple vector.

## Theoretical Background and Concepts

- The inverse of a diagonal matrix with nonzero diagonal entries is the diagonal matrix of the reciprocals.
- Geometrically, $`S^{-1}`$ undoes the transformation $`S`$: $`S^{-1}(Sx)=x`$.

## Detailed Step-by-Step Solution

```math
S^{-1}=\begin{pmatrix}\frac12&0\\0&2\end{pmatrix}.
```

**Geometric meaning:** $`S`$ stretches the plane by factor $`2`$ in the $`x`$-direction and compresses it by factor $`\frac12`$ in the $`y`$-direction. $`S^{-1}`$ does the opposite: it compresses by $`\frac12`$ in the $`x`$-direction and stretches by $`2`$ in the $`y`$-direction, returning every point to its original position.

**Check on $`v=(1,1)^T`$:**

```math
Sv=\begin{pmatrix}2\\\frac12\end{pmatrix},\qquad S^{-1}(Sv)=\begin{pmatrix}\frac12\cdot2\\2\cdot\frac12\end{pmatrix}=\begin{pmatrix}1\\1\end{pmatrix}=v.
```

## Verification and Consistency Checks

- $`SS^{-1}=\mathrm{diag}(2\cdot\frac12,\ \frac12\cdot2)=I`$. ✓
- $`\det S=2\cdot\frac12=1`$: the scaling preserves area (a $`1\times1`$ square becomes a $`2\times\frac12`$ rectangle), and $`\det S^{-1}=1`$ too. ✓
