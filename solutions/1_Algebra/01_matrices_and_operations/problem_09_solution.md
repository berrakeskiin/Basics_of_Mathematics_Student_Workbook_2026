# Exercise 9. Composing Transformations

## Problem Statement

Let

```math
S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad R=\begin{pmatrix}0&-1\\1&0\end{pmatrix},\qquad x=\begin{pmatrix}1\\2\end{pmatrix}.
```

$`S`$ is a nonuniform scaling, and $`R`$ is a $`90^\circ`$ counterclockwise rotation. Compute $`RSx`$ and $`SRx`$. Compare the results and explain geometrically why the order of these transformations matters.

## Theoretical Background and Concepts

- A matrix acts on a vector as a linear transformation.
- $`RSx=R(Sx)`$: first apply $`S`$, then $`R`$. **The matrix closest to $`x`$ acts first.**
- Composition of transformations corresponds to the matrix product. Since matrix multiplication is not commutative, the order of transformations generally matters.

## Detailed Step-by-Step Solution

**$`RSx`$ (scale first, then rotate):**

```math
Sx=\begin{pmatrix}2\cdot1\\1\cdot2\end{pmatrix}=\begin{pmatrix}2\\2\end{pmatrix},\qquad R(Sx)=\begin{pmatrix}0\cdot2-1\cdot2\\1\cdot2+0\cdot2\end{pmatrix}=\begin{pmatrix}-2\\2\end{pmatrix}.
```

**$`SRx`$ (rotate first, then scale):**

```math
Rx=\begin{pmatrix}-2\\1\end{pmatrix},\qquad S(Rx)=\begin{pmatrix}2\cdot(-2)\\1\cdot1\end{pmatrix}=\begin{pmatrix}-4\\1\end{pmatrix}.
```

**Comparison:** $`RSx=(-2,2)^T\neq SRx=(-4,1)^T`$.

**Geometric explanation:** $`S`$ stretches only the **horizontal** direction (x-axis) by 2. In $`RS`$, the horizontal component of $`x`$ (which is 1) is stretched, and then the vector is rotated. In $`SR`$, the vector is rotated first, so its original vertical component (2) becomes horizontal, and that is what gets stretched. Different parts of the vector are stretched, so the results differ. Rotation does not "respect" the special x-direction of the scaling, so the transformations do not commute.

## Verification and Consistency Checks

- Matrix products: $`RS=\begin{pmatrix}0&-1\\2&0\end{pmatrix}`$ and $`RS\,x=(-2,2)^T`$ ✓. $`SR=\begin{pmatrix}0&-2\\1&0\end{pmatrix}`$ and $`SR\,x=(-4,1)^T`$ ✓. Also $`RS\ne SR`$.
- Length check: $`|x|=\sqrt5`$. Rotation preserves length, so $`|Rx|=\sqrt{4+1}=\sqrt5`$ ✓. Also $`|RSx|=|Sx|=\sqrt8`$ ✓.
