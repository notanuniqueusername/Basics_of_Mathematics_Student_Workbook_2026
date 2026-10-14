# Exercise 6. Transpose

## The question

We are given

$$A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}.$$

Compute $A^T$, $B^T$, and $AB$, then verify in this example that $(AB)^T=B^TA^T$.

## Before calculating: what the transpose does

The transpose $X^T$ turns rows into columns: the entry in row $i$, column $j$ of $X^T$ is the entry in row $j$, column $i$ of $X$.

$$(X^T)_{ij}=x_{ji}.$$

So an $m\times n$ matrix has an $n\times m$ transpose. Geometrically, the matrix is reflected across its main diagonal.

## 1. Compute $A^T$ and $B^T$

The rows of $A$ become the columns of $A^T$:

$$A^T=\begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix}\quad(3\times2).$$

The rows of $B$ become the columns of $B^T$:

$$B^T=\begin{pmatrix}1&2&-1\\0&1&3\end{pmatrix}\quad(2\times3).$$

## 2. Compute $AB$

The sizes are $(2\times\underline3)(\underline3\times2)$, so the product is defined and is $2\times2$.

$$AB=\begin{pmatrix}1\cdot1+2\cdot2+3\cdot(-1) & 1\cdot0+2\cdot1+3\cdot3\\ 4\cdot1+5\cdot2+6\cdot(-1) & 4\cdot0+5\cdot1+6\cdot3\end{pmatrix}=\begin{pmatrix}2&11\\8&23\end{pmatrix}.$$

## 3. Compute $(AB)^T$

Swap rows and columns of $AB$:

$$(AB)^T=\begin{pmatrix}2&8\\11&23\end{pmatrix}.$$

## 4. Compute $B^TA^T$

The sizes are $(2\times\underline3)(\underline3\times2)$, so this is defined and is $2\times2$.

$$B^TA^T=\begin{pmatrix}1\cdot1+2\cdot2+(-1)\cdot3 & 1\cdot4+2\cdot5+(-1)\cdot6\\ 0\cdot1+1\cdot2+3\cdot3 & 0\cdot4+1\cdot5+3\cdot6\end{pmatrix}=\begin{pmatrix}2&8\\11&23\end{pmatrix}.$$

Comparing with step 3:

$$(AB)^T=\begin{pmatrix}2&8\\11&23\end{pmatrix}=B^TA^T.\ ✓$$

## 5. Why the order reverses

There are two reasons, one from sizes and one from entries.

**From sizes.** If $A$ is $m\times p$ and $B$ is $p\times q$, then $AB$ is $m\times q$, so $(AB)^T$ is $q\times m$. Now $B^T$ is $q\times p$ and $A^T$ is $p\times m$, so $B^TA^T$ is defined and is $q\times m$, the right size. The other order does not fit in general. Here $A^TB^T$ is $(3\times2)(2\times3)$, which is defined but is $3\times3$, so it cannot equal the $2\times2$ matrix $(AB)^T$.

**From entries.** The $(i,j)$ entry of $(AB)^T$ is the $(j,i)$ entry of $AB$:

$$\big((AB)^T\big)_{ij}=(AB)_{ji}=\sum_k a_{jk}\,b_{ki}=\sum_k (B^T)_{ik}\,(A^T)_{kj}=(B^TA^T)_{ij}.$$

Transposing flips which matrix supplies the rows and which supplies the columns, so the factors must swap places.

## 6. Verification

**Independent check of $AB$.** The first column of $AB$ should be $A$ times the first column of $B$:

$$A\begin{pmatrix}1\\2\\-1\end{pmatrix}=\begin{pmatrix}1+4-3\\4+10-6\end{pmatrix}=\begin{pmatrix}2\\8\end{pmatrix}.\ ✓$$

The second column should be $A$ times the second column of $B$:

$$A\begin{pmatrix}0\\1\\3\end{pmatrix}=\begin{pmatrix}0+2+9\\0+5+18\end{pmatrix}=\begin{pmatrix}11\\23\end{pmatrix}.\ ✓$$

**Determinant check.** A transpose does not change the determinant:

$$\det(AB)=2\cdot23-11\cdot8=-42,\qquad \det\big((AB)^T\big)=2\cdot23-8\cdot11=-42.\ ✓$$
