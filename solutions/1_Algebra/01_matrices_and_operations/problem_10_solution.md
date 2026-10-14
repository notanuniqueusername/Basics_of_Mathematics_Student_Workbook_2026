# Exercise 10. Columns of a Matrix Product

## The question

We are given

$$A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&2\\-1&0\\3&1\end{pmatrix}.$$

Let $b_1,b_2$ be the columns of $B$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute $AB$.
3. Compare, and explain why the columns of $AB$ are exactly $Ab_1$ and $Ab_2$.

## Before calculating: the idea

By Exercise 3, $A$ is $2\times3$ and $B$ is $3\times2$, so $AB$ is defined and is $2\times2$.

The claim to test is that a product can be built **one column at a time**:

$$AB=A\begin{pmatrix}b_1&b_2\end{pmatrix}=\begin{pmatrix}Ab_1&Ab_2\end{pmatrix}.$$

So multiplying by a matrix $B$ is just multiplying by each of its columns separately, and then placing the results side by side.

## 1. Compute $Ab_1$ and $Ab_2$

The columns of $B$ are

$$b_1=\begin{pmatrix}1\\-1\\3\end{pmatrix},\qquad b_2=\begin{pmatrix}2\\0\\1\end{pmatrix}.$$

Each is a vector with 3 entries, matching the 3 columns of $A$, so the products are defined.

$$Ab_1=\begin{pmatrix}1\cdot1+2\cdot(-1)+0\cdot3\\0\cdot1+1\cdot(-1)+1\cdot3\end{pmatrix}=\begin{pmatrix}-1\\2\end{pmatrix}.$$

$$Ab_2=\begin{pmatrix}1\cdot2+2\cdot0+0\cdot1\\0\cdot2+1\cdot0+1\cdot1\end{pmatrix}=\begin{pmatrix}2\\1\end{pmatrix}.$$

## 2. Compute $AB$ directly

Using the usual row-by-column rule:

$$AB=\begin{pmatrix}1\cdot1+2\cdot(-1)+0\cdot3 & 1\cdot2+2\cdot0+0\cdot1\\ 0\cdot1+1\cdot(-1)+1\cdot3 & 0\cdot2+1\cdot0+1\cdot1\end{pmatrix}=\begin{pmatrix}-1&2\\2&1\end{pmatrix}.$$

## 3. Compare

$$\begin{pmatrix}Ab_1&Ab_2\end{pmatrix}=\begin{pmatrix}-1&2\\2&1\end{pmatrix}=AB.$$

The first column of $AB$ is $\begin{pmatrix}-1\\2\end{pmatrix}=Ab_1$, and the second is $\begin{pmatrix}2\\1\end{pmatrix}=Ab_2$. ✓

## 4. Why this must happen

Look at how an entry of $AB$ is defined:

$$(AB)_{ij}=\sum_k a_{ik}\,b_{kj}.$$

Fix the column index $j$. The entries $(AB)_{1j},(AB)_{2j},\dots$ all use only the $j$-th column of $B$, namely $b_j=(b_{1j},b_{2j},\dots)$, and nothing from the other columns. But the same sums, $\sum_k a_{ik}b_{kj}$ over $i=1,2,\dots$, are exactly the entries of $Ab_j$ (row of $A$ paired with the vector $b_j$).

So the $j$-th column of $AB$ equals $Ab_j$. The row-by-column rule for $AB$ is just the row-by-column rule for $Ax$, repeated once for each column of $B$.

This also connects to Exercise 5. Since $Ab_j$ is a linear combination of the columns of $A$ with coefficients from $b_j$, **every column of $AB$ is a combination of the columns of $A$**. For example:

$$Ab_1=1\begin{pmatrix}1\\0\end{pmatrix}-1\begin{pmatrix}2\\1\end{pmatrix}+3\begin{pmatrix}0\\1\end{pmatrix}=\begin{pmatrix}1-2+0\\0-1+3\end{pmatrix}=\begin{pmatrix}-1\\2\end{pmatrix}.$$

## 5. Verification

**Column view of $b_2$.** Using the same combination idea for the second column:

$$Ab_2=2\begin{pmatrix}1\\0\end{pmatrix}+0\begin{pmatrix}2\\1\end{pmatrix}+1\begin{pmatrix}0\\1\end{pmatrix}=\begin{pmatrix}2\\1\end{pmatrix}.\ ✓$$

**Linearity check.** Since the columns of $B$ add up to $b_1+b_2=\begin{pmatrix}3\\-1\\4\end{pmatrix}$, we need $A(b_1+b_2)=Ab_1+Ab_2$:

$$A\begin{pmatrix}3\\-1\\4\end{pmatrix}=\begin{pmatrix}3-2+0\\0-1+4\end{pmatrix}=\begin{pmatrix}1\\3\end{pmatrix},\qquad Ab_1+Ab_2=\begin{pmatrix}-1+2\\2+1\end{pmatrix}=\begin{pmatrix}1\\3\end{pmatrix}.\ ✓$$

**Determinant check.** $\det(AB)=(-1)(1)-(2)(2)=-5$. This is a valid $2\times2$ result and is not zero, so the two columns $\begin{pmatrix}-1\\2\end{pmatrix}$ and $\begin{pmatrix}2\\1\end{pmatrix}$ are independent.
