# Exercise 15. Associativity of Multiplication and Different Calculation Paths

## The question

We are given

$$A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\quad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix},\quad C=\begin{pmatrix}2&1\\0&-1\end{pmatrix}.$$

Compute $(AB)C$ and $A(BC)$, compare the results and the number of intermediate operations, and explain what associativity means here.

## Before calculating: the plan

The sizes are $A_{2\times3}$, $B_{3\times2}$, $C_{2\times2}$. By the rule from Exercise 3, both groupings are defined:

- $(AB)C$: $AB$ is $2\times2$, then $(2\times2)(2\times2)$ gives $2\times2$.
- $A(BC)$: $BC$ is $3\times2$, then $(2\times3)(3\times2)$ gives $2\times2$.

The final sizes agree, but the **intermediate matrices differ** ($2\times2$ versus $3\times2$). The question is whether the final entries also agree.

## 1. Path 1: $(AB)C$

First $AB$:

$$AB=\begin{pmatrix}1\cdot1+2\cdot2+0\cdot(-1) & 1\cdot0+2\cdot1+0\cdot3\\ 0\cdot1+1\cdot2+1\cdot(-1) & 0\cdot0+1\cdot1+1\cdot3\end{pmatrix}=\begin{pmatrix}5&2\\1&4\end{pmatrix}.$$

Then multiply by $C$:

$$(AB)C=\begin{pmatrix}5\cdot2+2\cdot0 & 5\cdot1+2\cdot(-1)\\ 1\cdot2+4\cdot0 & 1\cdot1+4\cdot(-1)\end{pmatrix}=\begin{pmatrix}10&3\\2&-3\end{pmatrix}.$$

## 2. Path 2: $A(BC)$

First $BC$:

$$BC=\begin{pmatrix}1\cdot2+0\cdot0 & 1\cdot1+0\cdot(-1)\\ 2\cdot2+1\cdot0 & 2\cdot1+1\cdot(-1)\\ -1\cdot2+3\cdot0 & -1\cdot1+3\cdot(-1)\end{pmatrix}=\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}.$$

Then multiply $A$ by it:

$$A(BC)=\begin{pmatrix}1\cdot2+2\cdot4+0\cdot(-2) & 1\cdot1+2\cdot1+0\cdot(-4)\\ 0\cdot2+1\cdot4+1\cdot(-2) & 0\cdot1+1\cdot1+1\cdot(-4)\end{pmatrix}=\begin{pmatrix}10&3\\2&-3\end{pmatrix}.$$

## 3. Compare

$$(AB)C=\begin{pmatrix}10&3\\2&-3\end{pmatrix}=A(BC).$$

The two paths go through different intermediate matrices, $\begin{pmatrix}5&2\\1&4\end{pmatrix}$ and $\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}$, yet end at the same result.

## 4. Counting the work

A product of an $m\times n$ matrix and an $n\times q$ matrix needs $m\cdot n\cdot q$ multiplications (each of the $mq$ entries takes $n$ of them).

| Path | Step | Sizes | Multiplications |
|---|---|---|---|
| $(AB)C$ | $AB$ | $(2\times3)(3\times2)$ | $2\cdot3\cdot2=12$ |
| | $(AB)C$ | $(2\times2)(2\times2)$ | $2\cdot2\cdot2=8$ |
| | **Total** | | **20** |
| $A(BC)$ | $BC$ | $(3\times2)(2\times2)$ | $3\cdot2\cdot2=12$ |
| | $A(BC)$ | $(2\times3)(3\times2)$ | $2\cdot3\cdot2=12$ |
| | **Total** | | **24** |

Both paths give the same answer, but $(AB)C$ is cheaper here, because it keeps the intermediate matrix small ($2\times2$ rather than $3\times2$). For large matrices, choosing the grouping well can make a big difference in computation time.

## 5. What associativity means

Associativity says

$$(AB)C=A(BC)$$

whenever the products are defined. So the grouping does not matter, and we can write $ABC$ without brackets. This is what allowed us earlier to compute $A^3$ as either $A^2A$ or $AA^2$ (Exercise 7).

It is important to separate two things:

- **Grouping can be changed freely.** Brackets do not affect the result.
- **Order cannot be changed.** Associativity says nothing about $AB$ versus $BA$, and as we saw in Exercises 3, 4, and 9, swapping factors generally changes the result or makes the product undefined.

The reason associativity holds is that a product is a composition of transformations (Exercise 9). Applying "first $C$, then $B$, then $A$" gives the same overall effect whether we combine $B$ and $A$ into one step first or combine $C$ and $B$ first. Composition of functions is always associative, and matrix multiplication is composition.

## 6. Verification

**Test on a vector.** Take $x=\begin{pmatrix}1\\0\end{pmatrix}$. Apply the three matrices one at a time, right to left:

$$Cx=\begin{pmatrix}2\\0\end{pmatrix},\qquad B(Cx)=\begin{pmatrix}2\\4\\-2\end{pmatrix},\qquad A\big(B(Cx)\big)=\begin{pmatrix}2+8+0\\0+4-2\end{pmatrix}=\begin{pmatrix}10\\2\end{pmatrix}.$$

This is the first column of $(AB)C=A(BC)$. ✓

**Column check.** The first column of $(AB)C$ equals $AB$ times the first column of $C$ (Exercise 10):

$$\begin{pmatrix}5&2\\1&4\end{pmatrix}\begin{pmatrix}2\\0\end{pmatrix}=\begin{pmatrix}10\\2\end{pmatrix}.\ ✓$$

**Second column.** Applying the matrices to the second column of $C$, $\begin{pmatrix}1\\-1\end{pmatrix}$:

$$B\begin{pmatrix}1\\-1\end{pmatrix}=\begin{pmatrix}1\\1\\-4\end{pmatrix},\qquad A\begin{pmatrix}1\\1\\-4\end{pmatrix}=\begin{pmatrix}1+2\\1-4\end{pmatrix}=\begin{pmatrix}3\\-3\end{pmatrix}.\ ✓$$
