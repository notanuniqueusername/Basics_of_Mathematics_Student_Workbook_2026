# Exercise 15. Combining Determinant Properties

## The question

Let $A$ and $B$ be invertible $2\times2$ matrices with
$$\det A=-2,\qquad \det B=3.$$
Without finding the entries of the matrices, compute
$$\det\left(B^{-1}A^TB\right).$$
State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

## Before calculating: the concepts

Use, in order, the determinant of a product, the determinant of an inverse, and invariance under transpose.

## 1. List the properties in their order of use

First split the determinant of the three-factor product into three scalar determinants. Next replace the inverse determinant by a reciprocal and the transpose determinant by the original determinant. Only then cancel the nonzero scalar factors involving $B$.

## 2. Evaluate the resulting scalar expression

Apply the product rule first, keeping all three factors:

$$\det(B^{-1}A^TB)=\det(B^{-1})\det(A^T)\det B.$$

Since $BB^{-1}=I$, taking determinants gives $3\det(B^{-1})=1$, so $\det(B^{-1})=1/3$. Transpose invariance gives $\det(A^T)=\det A=-2$. Substitute:

$$\det(B^{-1}A^TB)=\frac13(-2)3=\boxed{-2}.$$

Equivalently, keeping the determinant symbols until the last line,

$$\frac1{\det B}\det A\det B=\det A,$$

because the nonzero scalar $\det B$ cancels with its reciprocal. No entries of $A$ or $B$ are required.

## 3. Explain the cancellation carefully

This cancellation happens among scalar determinants. It does not require moving $B$ past $A^T$ inside the original matrix expression. In general the matrix $B^{-1}A^TB$ can differ from $A^T$ even though the two determinants agree.

## 4. Verification

Set $C=B^{-1}A^TB$. Rearranging the defining identity by valid adjacent cancellations gives $BC=A^TB$. Therefore its determinants must satisfy

$$\det B\det C=\det(A^T)\det B.$$

With the computed answer, the left side is $3(-2)=-6$ and the right side is $(-2)3=-6$. Also $C$ is a product of invertible matrices and must be invertible; its computed determinant $-2$ is nonzero, as required.
