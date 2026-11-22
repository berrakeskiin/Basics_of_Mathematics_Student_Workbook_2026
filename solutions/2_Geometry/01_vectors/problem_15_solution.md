# Exercise 15. Comparing Directions Using the Cosine of the Angle

## Problem Statement

Given $`a=(1,2,1)`$, $`b=(2,4,2)`$, $`c=(2,0,3)`$. For each pair compute $`\dfrac{u\cdot v}{\|u\|\,\|v\|}`$. Order the pairs by increasing angle. Explain why for $`a`$ and $`b`$ the value is $`1`$ even though the vectors have different lengths.

## Theoretical Background and Concepts

- $`\cos\theta=\dfrac{u\cdot v}{\|u\|\,\|v\|}`$; on $`[0^\circ,180^\circ]`$, a larger cosine means a smaller angle.
- Dividing by the lengths removes the effect of length; only the **direction** matters.

## Detailed Step-by-Step Solution

Lengths: $`\|a\|=\sqrt6`$, $`\|b\|=\sqrt{24}=2\sqrt6`$, $`\|c\|=\sqrt{13}`$.

```math
\cos(a,b)=\frac{2+8+2}{\sqrt6\cdot2\sqrt6}=\frac{12}{12}=1\ \Rightarrow\ \theta=0^\circ.
```

```math
\cos(a,c)=\frac{2+0+3}{\sqrt6\cdot\sqrt{13}}=\frac5{\sqrt{78}}\approx0.566\ \Rightarrow\ \theta\approx55.5^\circ.
```

```math
\cos(b,c)=\frac{4+0+6}{2\sqrt6\cdot\sqrt{13}}=\frac{10}{2\sqrt{78}}=\frac5{\sqrt{78}}\approx0.566\ \Rightarrow\ \theta\approx55.5^\circ.
```

**Order by increasing angle:** $`(a,b)`$ with $`0^\circ`$, then $`(a,c)`$ and $`(b,c)`$, which are equal ($`\approx55.5^\circ`$).

**Why $`\cos(a,b)=1`$:** $`b=2a`$, so $`b`$ points in exactly the same direction as $`a`$; it is only twice as long. The cosine formula divides by both lengths, so the factor 2 cancels and only the (identical) direction remains.

## Verification and Consistency Checks

- $`(a,c)`$ and $`(b,c)`$ must have the same angle because $`b`$ has the same direction as $`a`$ ✓.
- All cosines lie in $`[-1,1]`$ ✓.
