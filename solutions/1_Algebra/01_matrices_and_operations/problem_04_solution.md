# Exercise 4. Matrix Multiplication and Noncommutativity

## The question

We are given

$$A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\3&1\end{pmatrix}.$$

Compute $AB$ and $BA$. Is $AB=BA$? Use the example to explain what noncommutativity means.

## Before calculating: the rule

Both matrices are $2\times2$, so by Exercise 3 both $AB$ and $BA$ are defined and are again $2\times2$.

The entry in row $i$, column $j$ of a product is the row $i$ of the first matrix paired with the column $j$ of the second, multiplying entry by entry and adding:

$$(XY)_{ij}=\sum_k x_{ik}\,y_{kj}.$$

## 1. Compute $AB$

Rows of $A$ paired with columns of $B$:

$$AB=\begin{pmatrix}1\cdot2+2\cdot3 & 1\cdot0+2\cdot1\\ 0\cdot2+1\cdot3 & 0\cdot0+1\cdot1\end{pmatrix}=\begin{pmatrix}8&2\\3&1\end{pmatrix}.$$

## 2. Compute $BA$

Now the roles swap: rows of $B$ paired with columns of $A$:

$$BA=\begin{pmatrix}2\cdot1+0\cdot0 & 2\cdot2+0\cdot1\\ 3\cdot1+1\cdot0 & 3\cdot2+1\cdot1\end{pmatrix}=\begin{pmatrix}2&4\\3&7\end{pmatrix}.$$

## 3. Compare

$$AB=\begin{pmatrix}8&2\\3&1\end{pmatrix}\neq\begin{pmatrix}2&4\\3&7\end{pmatrix}=BA.$$

So $AB\ne BA$. In fact, the difference is

$$AB-BA=\begin{pmatrix}6&-2\\0&-6\end{pmatrix},$$

which is far from the zero matrix. Only the entry $(2,1)$ happens to agree.

## 4. What noncommutativity means

Noncommutativity means that **the order of the factors changes the result**. For numbers, $2\cdot3=3\cdot2$ always, but for matrices $AB=BA$ is not a law. Here the two products differ in three of four entries.

Two points are worth stating precisely:

- It does **not** mean $AB=BA$ never happens. Some pairs do commute, for example $A$ and the identity matrix, or $A$ and $A^2$. Exercise 11 asks exactly when this occurs.
- It means we are **not allowed to assume** $AB=BA$, so we can never swap factors without checking. For instance, $(A+B)^2=A^2+AB+BA+B^2$, which is not $A^2+2AB+B^2$ unless $AB=BA$.

The reason is in the rule: $AB$ uses rows of $A$ with columns of $B$, while $BA$ uses rows of $B$ with columns of $A$. These are different pairings, so there is no reason for them to give the same numbers.

## 5. Verification

Each product can be checked by a second method, and the two products can be compared by invariants.

**Columns check.** The first column of $AB$ should equal $A$ times the first column of $B$:

$$A\begin{pmatrix}2\\3\end{pmatrix}=\begin{pmatrix}1\cdot2+2\cdot3\\0\cdot2+1\cdot3\end{pmatrix}=\begin{pmatrix}8\\3\end{pmatrix}.\ ✓$$

The first column of $BA$ should equal $B$ times the first column of $A$:

$$B\begin{pmatrix}1\\0\end{pmatrix}=\begin{pmatrix}2\\3\end{pmatrix}.\ ✓$$

**Determinant check.** We have $\det A=1$ and $\det B=2$, and $\det(AB)=\det A\cdot\det B$:

$$\det(AB)=8\cdot1-2\cdot3=2,\qquad \det(BA)=2\cdot7-4\cdot3=2.\ ✓$$

Both equal $1\cdot2=2$, as expected.

**Trace check.** The trace (sum of diagonal entries) of $AB$ and $BA$ is always the same: $8+1=9$ and $2+7=9$. ✓

The determinant and trace agree, yet the matrices differ. So these two products have the same "size" in these senses but are still different matrices, which is a good reminder that agreeing on some numbers does not make matrices equal.
