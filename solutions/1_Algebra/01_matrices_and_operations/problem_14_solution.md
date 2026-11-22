# Exercise 14. Rotation Matrices

## Problem Statement

The matrix for a rotation through an angle $`\theta`$ is

```math
R(\theta)=\begin{pmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{pmatrix}.
```

Compute $`R(\alpha)R(\beta)`$ and, using the angle-sum formulas, show that $`R(\alpha)R(\beta)=R(\alpha+\beta)`$. Explain the result geometrically.

## Theoretical Background and Concepts

- $`R(\theta)`$ rotates every vector in the plane counterclockwise by the angle $`\theta`$ about the origin.
- Angle-sum formulas:

```math
\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta,\qquad \sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta.
```

- The product of matrices corresponds to composing the transformations.

## Detailed Step-by-Step Solution

```math
R(\alpha)R(\beta)=\begin{pmatrix}\cos\alpha&-\sin\alpha\\\sin\alpha&\cos\alpha\end{pmatrix}\begin{pmatrix}\cos\beta&-\sin\beta\\\sin\beta&\cos\beta\end{pmatrix}.
```

Entries:
- $`(1,1)`$: $`\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)`$
- $`(1,2)`$: $`-\cos\alpha\sin\beta-\sin\alpha\cos\beta=-(\sin\alpha\cos\beta+\cos\alpha\sin\beta)=-\sin(\alpha+\beta)`$
- $`(2,1)`$: $`\sin\alpha\cos\beta+\cos\alpha\sin\beta=\sin(\alpha+\beta)`$
- $`(2,2)`$: $`-\sin\alpha\sin\beta+\cos\alpha\cos\beta=\cos(\alpha+\beta)`$

Therefore

```math
R(\alpha)R(\beta)=\begin{pmatrix}\cos(\alpha+\beta)&-\sin(\alpha+\beta)\\\sin(\alpha+\beta)&\cos(\alpha+\beta)\end{pmatrix}=R(\alpha+\beta).
```

**Geometric meaning:** rotating first by $`\beta`$ and then by $`\alpha`$ is the same as one rotation by $`\alpha+\beta`$. Angles of consecutive rotations add up.

## Verification and Consistency Checks

- Because $`\alpha+\beta=\beta+\alpha`$, we get $`R(\alpha)R(\beta)=R(\beta)R(\alpha)`$: rotations about the same point **commute**, even though matrices in general do not.
- Special case $`\beta=-\alpha`$: $`R(\alpha)R(-\alpha)=R(0)=I`$, so $`R(\alpha)^{-1}=R(-\alpha)`$. ✓
- Numerical check with $`\alpha=\beta=90^\circ`$: $`R(90^\circ)=\begin{pmatrix}0&-1\\1&0\end{pmatrix}`$, and $`R(90^\circ)^2=\begin{pmatrix}-1&0\\0&-1\end{pmatrix}=R(180^\circ)`$. ✓
- $`\det R(\theta)=\cos^2\theta+\sin^2\theta=1`$, which is consistent with $`\det(R(\alpha)R(\beta))=1\cdot1=1`$. ✓
