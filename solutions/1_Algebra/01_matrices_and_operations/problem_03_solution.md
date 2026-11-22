# Exercise 3. When Can Matrices Be Multiplied?

## Problem Statement

The matrix sizes are $A_{2\times3},\ B_{3\times4},\ C_{4\times2},\ D_{2\times2}$.
For the products $AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA$ determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Theoretical Background and Concepts

**Compatibility condition:** the product $XY$ of $X_{m\times n}$ and $Y_{p\times q}$ is defined **only if $n=p$** (number of columns of the first = number of rows of the second). The result then has size $m\times q$.

Reason: the entry $(XY)_{ij}=\sum_k x_{ik}y_{kj}$ pairs row $i$ of $X$ (length $n$) with column $j$ of $Y$ (length $p$), so the lengths must match.

## Detailed Step-by-Step Solution

| Product | Sizes | Inner dimensions | Defined? | Result size |
|---|---|---|---|---|
| $AB$ | $(2\times3)(3\times4)$ | $3=3$ | yes | $2\times4$ |
| $BA$ | $(3\times4)(2\times3)$ | $4\ne2$ | no | — |
| $BC$ | $(3\times4)(4\times2)$ | $4=4$ | yes | $3\times2$ |
| $CB$ | $(4\times2)(3\times4)$ | $2\ne3$ | no | — |
| $AC$ | $(2\times3)(4\times2)$ | $3\ne4$ | no | — |
| $CA$ | $(4\times2)(2\times3)$ | $2=2$ | yes | $4\times3$ |
| $AD$ | $(2\times3)(2\times2)$ | $3\ne2$ | no | — |
| $DA$ | $(2\times2)(2\times3)$ | $2=2$ | yes | $2\times3$ |

So the defined products are: $AB\ (2\times4)$, $BC\ (3\times2)$, $CA\ (4\times3)$, $DA\ (2\times3)$.

## Verification and Consistency Checks

- The example shows that $XY$ being defined does **not** imply $YX$ is defined ($AB$ yes, $BA$ no), which is consistent with the non-commutativity of matrix multiplication.
- Chain check: $A\,B\,C$ has sizes $(2\times3)(3\times4)(4\times2)$; all inner dimensions match, so $ABC$ is $2\times2$. That is consistent with $AB$ ($2\times4$) and $BC$ ($3\times2$) both being defined.
