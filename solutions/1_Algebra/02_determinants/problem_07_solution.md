# Exercise 7. Using Properties Instead of Recomputing

## Problem Statement

Suppose that for a $`3\times3`$ matrix, $`\det A=-4`$. Compute $`\det(2A)`$, $`\det(A^T)`$, $`\det(A^2)`$, $`\det(-A)`$. Justify each answer using the appropriate property.

## Theoretical Background and Concepts

For an $`n\times n`$ matrix $`A`$ (here $`n=3`$):
- $`\det(cA)=c^n\det A`$ (each of the $`n`$ rows is multiplied by $`c`$);
- $`\det(A^T)=\det A`$;
- $`\det(AB)=\det A\cdot\det B`$, so $`\det(A^2)=(\det A)^2`$.

## Detailed Step-by-Step Solution

```math
\det(2A)=2^3\det A=8\cdot(-4)=-32.
```

```math
\det(A^T)=\det A=-4.
```

```math
\det(A^2)=(\det A)^2=(-4)^2=16.
```

```math
\det(-A)=(-1)^3\det A=-1\cdot(-4)=4.
```

## Verification and Consistency Checks

- Test with a concrete matrix: $`A=\mathrm{diag}(-4,1,1)`$ has $`\det A=-4`$. Then $`2A=\mathrm{diag}(-8,2,2)`$ with $`\det=-32`$ ✓; $`A^2=\mathrm{diag}(16,1,1)`$ with $`\det=16`$ ✓; $`-A=\mathrm{diag}(4,-1,-1)`$ with $`\det=4`$ ✓.
- Note: $`\det(2A)\neq2\det A`$; the factor is $`2^3`$ because the matrix is $`3\times3`$.
