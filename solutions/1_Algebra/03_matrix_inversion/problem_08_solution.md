# Exercise 8. Inverse of a Transformation

## The question

The matrix
$$S=\begin{pmatrix}2&0\\0&\frac12\end{pmatrix}$$
describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

## Before calculating: the concepts

Invert a diagonal scaling by taking reciprocals of its nonzero scaling factors.

## 1. Identify the two independent directions

The coordinate axes are preserved: $S(1,0)^T=(2,0)^T$ and $S(0,1)^T=(0,1/2)^T$. Neither scaling factor vanishes, so both input coordinates remain recoverable. The inverse can therefore be found one coordinate at a time, without a row-reduction procedure or a general inverse formula.

## 2. Write the inverse transformation

For a general input vector,

$$S\begin{pmatrix}x\\y\end{pmatrix}=\begin{pmatrix}2x\\y/2\end{pmatrix}.$$

Recover the first coordinate by dividing by $2$ and the second by multiplying by $2$:

$$\boxed{S^{-1}=\begin{pmatrix}1/2&0\\0&2\end{pmatrix}},\qquad S^{-1}\begin{pmatrix}X\\Y\end{pmatrix}=\begin{pmatrix}X/2\\2Y\end{pmatrix}.$$

Geometrically, $S^{-1}$ compresses horizontally by a factor $1/2$ and stretches vertically by a factor $2$. These are exactly the reciprocal operations to the original scaling.

## 3. Explain what the inverse preserves and changes

The scaling acts independently on the coordinate axes: horizontal lengths double and vertical lengths halve. The inverse uses reciprocal factors so that each coordinate returns to its original value.

Individual vector lengths need not be preserved. For example, $(1,0)^T$ becomes $(2,0)^T$, whereas $(0,1)^T$ becomes $(0,1/2)^T$. Nevertheless the signed area scale is $\det S=2(1/2)=1$, so parallelogram areas are preserved. The inverse has the same determinant, $(1/2)2=1$.

This separates two geometric properties: undoing a transformation recovers every vector, while area preservation alone does not require individual lengths to stay fixed. The product checks below verify recovery of vectors, which is the defining inverse property.

## 4. Verification

Take $v=(1,2)^T$. Then

$$Sv=\begin{pmatrix}2\cdot1\\(1/2)2\end{pmatrix}=\begin{pmatrix}2\\1\end{pmatrix},\qquad S^{-1}Sv=\begin{pmatrix}(1/2)2\\2\cdot1\end{pmatrix}=\begin{pmatrix}1\\2\end{pmatrix}=v.$$

The identity check works for every vector:

$$S^{-1}S=\begin{pmatrix}(1/2)2&0\\0&2(1/2)\end{pmatrix}=I,\qquad SS^{-1}=I.$$

The same vector test in the opposite order gives $S^{-1}v=(1/2,4)^T$ and $S(1/2,4)^T=(1,2)^T$, illustrating both inverse identities.
