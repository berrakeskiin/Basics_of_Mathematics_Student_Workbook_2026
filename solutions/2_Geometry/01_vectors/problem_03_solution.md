# Exercise 3. Vector Normalization

## Problem Statement

For $`v=(3,4)`$ find a unit vector $`e`$ with the same direction and orientation. Check that $`\|e\|=1`$, reconstruct $`v`$ as $`v=\|v\|e`$, and explain what changes during normalization and what remains unchanged.

## Theoretical Background and Concepts

- A **unit vector** has length 1.
- **Normalization:** $`e=\dfrac{v}{\|v\|}`$ (for $`v\neq0`$). Dividing by a positive number keeps the direction and orientation.

## Detailed Step-by-Step Solution

```math
\|v\|=\sqrt{3^2+4^2}=\sqrt{25}=5,\qquad e=\frac{v}{\|v\|}=\left(\frac35,\ \frac45\right).
```

**Check of length:**

```math
\|e\|=\sqrt{\left(\tfrac35\right)^2+\left(\tfrac45\right)^2}=\sqrt{\tfrac{9}{25}+\tfrac{16}{25}}=\sqrt1=1.
```

**Reconstruction:** $`\|v\|e=5\cdot\left(\frac35,\frac45\right)=(3,4)=v`$.

**What changes and what stays:** the **length** changes (from 5 to 1). The **direction** and **orientation** stay the same, because we multiplied by the positive number $`\frac15`$.

## Verification and Consistency Checks

- $`e`$ and $`v`$ are parallel: $`\frac{3/5}{3}=\frac{4/5}{4}=\frac15`$ ✓.
- $`-e=(-\frac35,-\frac45)`$ is also a unit vector, but with the opposite orientation, so it is not the answer. ✓
