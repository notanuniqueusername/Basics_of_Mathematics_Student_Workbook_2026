# Exercise 7. Inverse of a Product

## The question

For
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\0&3\end{pmatrix}$$
compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

## Before calculating: the concepts

The inverse product rule is $(AB)^{-1}=B^{-1}A^{-1}$.

## 1. Compute the composite matrix

In $AB$, each diagonal entry of $B$ scales the corresponding column of $A$ because $B$ is diagonal. Thus the first column becomes $(2,0)^T$ and the second becomes $(3,3)^T$. Its determinant is $2\cdot3=6$, so its inverse exists.

## 2. Compare direct inversion with reversed factors

First multiply the given matrices:

$$AB=\begin{pmatrix}1\cdot2+1\cdot0&1\cdot0+1\cdot3\\0\cdot2+1\cdot0&0\cdot0+1\cdot3\end{pmatrix}=\begin{pmatrix}2&3\\0&3\end{pmatrix}.$$

For a matrix $M=\begin{pmatrix}a&b\\c&d\end{pmatrix}$ with $ad-bc\ne0$, use

$$M^{-1}=\frac1{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}.$$

For $AB$, the determinant is $2\cdot3-3\cdot0=6$. Exchange the diagonal entries $2,3$ and negate the off-diagonal entries $3,0$ to construct

$$(AB)^{-1}=\frac16\begin{pmatrix}3&-3\\0&2\end{pmatrix}=\begin{pmatrix}1/2&-1/2\\0&1/3\end{pmatrix}.$$

Separately invert the factors. The shear $A$ sends $(x,y)^T$ to $(x+y,y)^T$. To undo it, keep the second coordinate and subtract it from the first, giving $A^{-1}(X,Y)^T=(X-Y,Y)^T$. The diagonal scaling $B$ sends $(x,y)^T$ to $(2x,3y)^T$, so its inverse divides the coordinates by $2$ and $3$. These constructions give

$$A^{-1}=\begin{pmatrix}1&-1\\0&1\end{pmatrix},\qquad B^{-1}=\begin{pmatrix}1/2&0\\0&1/3\end{pmatrix}.$$

Their reversed product is

$$B^{-1}A^{-1}=\begin{pmatrix}(1/2)1+0\cdot0&(1/2)(-1)+0\cdot1\\0\cdot1+(1/3)0&0(-1)+(1/3)1\end{pmatrix}=\boxed{\begin{pmatrix}1/2&-1/2\\0&1/3\end{pmatrix}}.$$

Thus the two methods give identical entries.

## 3. Explain why reversal is required

In $(AB)(B^{-1}A^{-1})$, the adjacent factors $B$ and $B^{-1}$ cancel first. The remaining factors $A$ and $A^{-1}$ then cancel. If the inverse factors were kept in the same order, those matching pairs would not generally be adjacent, and cancellation would not be justified.

## 4. Verification

With $C$ equal to the computed inverse,

$$(AB)C=\begin{pmatrix}2(1/2)+3\cdot0&2(-1/2)+3(1/3)\\0(1/2)+3\cdot0&0(-1/2)+3(1/3)\end{pmatrix}=I.$$

The order rule also follows directly from

$$(AB)(B^{-1}A^{-1})=A(BB^{-1})A^{-1}=I,$$

$$(B^{-1}A^{-1})(AB)=B^{-1}(A^{-1}A)B=I.$$

Both cancellations require the inverse factors to appear in reversed order. The proof uses associativity without commuting any matrix factors.
