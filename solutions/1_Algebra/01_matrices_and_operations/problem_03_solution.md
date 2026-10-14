# Exercise 3. When Can Matrices Be Multiplied?

## The question

The matrix sizes are

$$A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.$$

For the products $AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA$, determine whether each is defined. If so, state the size of the result, and justify each decision using the dimension compatibility condition.

## Before calculating: the condition

A product $XY$ pairs each **row** of $X$ with each **column** of $Y$, multiplying entry by entry and adding. This only works if a row of $X$ and a column of $Y$ have the same length.

- A row of $X$ has as many entries as $X$ has **columns**.
- A column of $Y$ has as many entries as $Y$ has **rows**.

So, for $X_{m\times n}$ and $Y_{p\times q}$:

- $XY$ is defined **if and only if $n=p$** (the inner numbers match).
- If defined, the result has size $m\times q$ (the outer numbers).

A quick way to remember it: write the sizes side by side, $(m\times \underline{n})(\underline{p}\times q)$. The inner pair must agree, and the outer pair is the answer.

## 1. Go through the products

**$AB$:** $(2\times\underline3)(\underline3\times4)$. Inner numbers $3=3$, so it is **defined**, with size $2\times4$.

**$BA$:** $(3\times\underline4)(\underline2\times3)$. Inner numbers $4\ne2$, so it is **not defined**.

**$BC$:** $(3\times\underline4)(\underline4\times2)$. Inner numbers $4=4$, so it is **defined**, with size $3\times2$.

**$CB$:** $(4\times\underline2)(\underline3\times4)$. Inner numbers $2\ne3$, so it is **not defined**.

**$AC$:** $(2\times\underline3)(\underline4\times2)$. Inner numbers $3\ne4$, so it is **not defined**.

**$CA$:** $(4\times\underline2)(\underline2\times3)$. Inner numbers $2=2$, so it is **defined**, with size $4\times3$.

**$AD$:** $(2\times\underline3)(\underline2\times2)$. Inner numbers $3\ne2$, so it is **not defined**.

**$DA$:** $(2\times\underline2)(\underline2\times3)$. Inner numbers $2=2$, so it is **defined**, with size $2\times3$.

## 2. Summary

| Product | Sizes | Inner match? | Result size |
|---|---|---|---|
| $AB$ | $2\times3$, $3\times4$ | yes | $2\times4$ |
| $BA$ | $3\times4$, $2\times3$ | no | not defined |
| $BC$ | $3\times4$, $4\times2$ | yes | $3\times2$ |
| $CB$ | $4\times2$, $3\times4$ | no | not defined |
| $AC$ | $2\times3$, $4\times2$ | no | not defined |
| $CA$ | $4\times2$, $2\times3$ | yes | $4\times3$ |
| $AD$ | $2\times3$, $2\times2$ | no | not defined |
| $DA$ | $2\times2$, $2\times3$ | yes | $2\times3$ |

## 3. What the pattern shows

- **Order matters for existence, not only for the values.** $AB$ is defined but $BA$ is not. The same happens for $BC$ versus $CB$, and $AD$ versus $DA$. In these cases the question "is $AB=BA$?" does not even make sense, since one side does not exist.
- **Both orders can exist with different sizes.** $AB$ is $2\times4$, and $BA$ would be... not defined, but compare $CA$ ($4\times3$) with $AC$ (not defined). Even when both exist, as with square matrices, the results need not be equal (Exercise 4).
- **Only a square matrix on both sides guarantees both orders.** Two matrices of the same square size $n\times n$ can always be multiplied in either order, and the result is again $n\times n$.

## 4. Verification

The rule can be double-checked by actually trying to pair a row with a column in a failing case.

Take $AC$. A row of $A$ has 3 entries, and a column of $C$ has 4 entries:

$$(a_{11},a_{12},a_{13})\ \text{ paired with }\ (c_{11},c_{21},c_{31},c_{41}).$$

The entry $c_{41}$ has no partner, so the pairing fails. ✓

Take $CA$. A row of $C$ has 2 entries, and a column of $A$ has 2 entries:

$$(c_{11},c_{12})\ \text{ paired with }\ (a_{11},a_{21}).$$

Every entry has a partner, so the pairing works. There are $4$ rows of $C$ and $3$ columns of $A$, giving $4\cdot3$ pairings, which is exactly the $4\times3$ result size. ✓
