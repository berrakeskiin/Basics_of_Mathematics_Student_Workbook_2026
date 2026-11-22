# Exercise 5. Angle Between Vectors

## Problem Statement

Given $`u=(1,1,0)`$ and $`v=(1,0,1)`$: (1) use the sign of $`u\cdot v`$ to predict the type of angle; (2) compute the angle; (3) compare the result with the prediction.

## Theoretical Background and Concepts

- $`\cos\theta=\dfrac{u\cdot v}{\|u\|\,\|v\|}`$, $`\theta\in[0^\circ,180^\circ]`$.
- Sign of $`u\cdot v`$: positive $`\Rightarrow`$ acute angle; zero $`\Rightarrow`$ right angle; negative $`\Rightarrow`$ obtuse angle.

## Detailed Step-by-Step Solution

1. **Prediction:** $`u\cdot v=1\cdot1+1\cdot0+0\cdot1=1>0`$, so the angle is **acute**.
2. **Calculation:** $`\|u\|=\sqrt2`$, $`\|v\|=\sqrt2`$,

```math
\cos\theta=\frac{1}{\sqrt2\cdot\sqrt2}=\frac12\ \Rightarrow\ \theta=60^\circ.
```

3. **Comparison:** $`60^\circ<90^\circ`$, so the angle is indeed acute, as predicted.

## Verification and Consistency Checks

- Geometric check: $`u`$, $`v`$ and $`u-v=(0,1,-1)`$ all have length $`\sqrt2`$, so the triangle with sides $`u`$, $`v`$, $`u-v`$ is equilateral, and every angle of an equilateral triangle is $`60^\circ`$. ✓
