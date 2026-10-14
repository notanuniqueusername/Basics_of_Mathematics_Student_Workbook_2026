# Exercise 5. Matrix Times Vector

## The question

We are given

$$A=\begin{pmatrix}2&-1\\1&3\end{pmatrix},\qquad x=\begin{pmatrix}4\\2\end{pmatrix}.$$

Compute $Ax$, then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from $x$.

## Before calculating: two ways to read the same product

A vector is a matrix with one column, so $Ax$ is a product of a $2\times2$ matrix and a $2\times1$ matrix. The inner numbers agree ($2=2$), so it is defined, and the result is $2\times1$.

There are two equivalent ways to compute it:

- **Row view:** each entry of $Ax$ is a row of $A$ paired with $x$ (the usual row-by-column rule).
- **Column view:** $Ax$ is a sum of the columns of $A$, each scaled by the matching entry of $x$:
$$Ax=x_1\,\text{col}_1(A)+x_2\,\text{col}_2(A).$$

The column view is the one that shows what a matrix actually does to a vector.

## 1. Compute $Ax$ (row view)

$$Ax=\begin{pmatrix}2\cdot4+(-1)\cdot2\\1\cdot4+3\cdot2\end{pmatrix}=\begin{pmatrix}8-2\\4+6\end{pmatrix}=\begin{pmatrix}6\\10\end{pmatrix}.$$

## 2. Write $Ax$ as a linear combination of columns

The columns of $A$ are

$$a_1=\begin{pmatrix}2\\1\end{pmatrix},\qquad a_2=\begin{pmatrix}-1\\3\end{pmatrix}.$$

The coefficients are the entries of $x$: $x_1=4$ goes with $a_1$, and $x_2=2$ goes with $a_2$.

$$Ax=4\begin{pmatrix}2\\1\end{pmatrix}+2\begin{pmatrix}-1\\3\end{pmatrix}=\begin{pmatrix}8\\4\end{pmatrix}+\begin{pmatrix}-2\\6\end{pmatrix}=\begin{pmatrix}6\\10\end{pmatrix}.$$

This matches step 1.

## 3. Why the two views agree

Look at the first entry of the row view: $2\cdot4+(-1)\cdot2$. In the column view, the same two terms appear: $4\cdot2$ comes from $4\,a_1$ and $2\cdot(-1)$ comes from $2\,a_2$. The row view groups the arithmetic by output entry, and the column view groups it by input entry. It is the same set of products, added in a different order.

The column view also has a geometric meaning. The vector $x$ is a recipe: "take 4 of the first column and 2 of the second". So $Ax$ is a point reached by moving along the columns of $A$. In particular, $A\begin{pmatrix}1\\0\end{pmatrix}=a_1$ and $A\begin{pmatrix}0\\1\end{pmatrix}=a_2$, so **the columns of $A$ are the images of the basic vectors**.

## 4. Verification

**Check by undoing the multiplication.** Here $\det A=2\cdot3-(-1)\cdot1=7\ne0$, so $A$ is invertible, and

$$A^{-1}=\frac17\begin{pmatrix}3&1\\-1&2\end{pmatrix}.$$

If $Ax=\begin{pmatrix}6\\10\end{pmatrix}$ is correct, then applying $A^{-1}$ should return $x$:

$$A^{-1}\begin{pmatrix}6\\10\end{pmatrix}=\frac17\begin{pmatrix}3\cdot6+1\cdot10\\-1\cdot6+2\cdot10\end{pmatrix}=\frac17\begin{pmatrix}28\\14\end{pmatrix}=\begin{pmatrix}4\\2\end{pmatrix}=x.\ ✓$$

**Check by linearity.** Since $x=4e_1+2e_2$, we get $Ax=4Ae_1+2Ae_2=4a_1+2a_2$, which is exactly the combination in step 2. ✓
