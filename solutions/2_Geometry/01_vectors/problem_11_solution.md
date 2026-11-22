# Exercise 11. Decomposition into Parallel and Perpendicular Components

## Problem Statement

Decompose $`u=(3,4)`$ into components parallel and perpendicular to $`v=(1,2)`$. Check

```math
u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.
```

Explain why these are two independent checks of correctness.

## Theoretical Background and Concepts

```math
u_{\parallel}=\mathrm{proj}_v u=\frac{u\cdot v}{v\cdot v}\,v,\qquad u_{\perp}=u-u_{\parallel}.
```

## Detailed Step-by-Step Solution

```math
u\cdot v=3\cdot1+4\cdot2=11,\qquad v\cdot v=1+4=5.
```

```math
u_{\parallel}=\frac{11}{5}(1,2)=\left(\frac{11}5,\ \frac{22}5\right),\qquad u_{\perp}=(3,4)-\left(\frac{11}5,\frac{22}5\right)=\left(\frac45,\ -\frac25\right).
```

**Check 1 (sum):** $`\left(\frac{11}5+\frac45,\ \frac{22}5-\frac25\right)=(3,4)=u`$ ✓.

**Check 2 (perpendicularity):** $`u_{\perp}\cdot v=\frac45\cdot1-\frac25\cdot2=0`$ ✓.

**Why two independent checks:** check 1 holds automatically for **any** vector $`u_{\parallel}`$ if we define $`u_{\perp}=u-u_{\parallel}`$, so it only catches arithmetic slips in the subtraction. Check 2 tests whether we chose the **right** parallel part: if the coefficient $`\frac{11}5`$ were wrong, the sum would still be correct, but $`u_{\perp}`$ would not be perpendicular to $`v`$. Together they confirm both the decomposition and the projection.

## Verification and Consistency Checks

- $`u_{\parallel}`$ is parallel to $`v`$ (it is $`\frac{11}5v`$) ✓.
- Pythagoras: $`\|u_{\parallel}\|^2+\|u_{\perp}\|^2=\frac{121+484}{25}+\frac{16+4}{25}=\frac{625}{25}=25=\|u\|^2`$ ✓.
