# Exercise 8. Determinant of a Product

## The question

Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

## Before calculating: the concepts

Determinants multiply: $\det(AB)=\det A\det B$. For invertible $A$, $\det(A^{-1})=1/\det A$. Products here require square matrices of the same size.

## 1. Check that the inverse exists

The expression $A^{-1}B$ is meaningful only if $A$ is invertible. Since the supplied determinant of $A$ is $3$, the inverse exists and its determinant is the reciprocal $1/3$. No entries of either matrix are needed.

## 2. Compute the three product determinants

Both product orders have determinants given by the product of the scalar determinants:

$$\det(AB)=\det A\det B=3(-5)=\boxed{-15},$$

$$\det(BA)=\det B\det A=(-5)3=\boxed{-15}.$$

To obtain the inverse determinant used in the third product, take determinants in $AA^{-1}=I$:

$$3\det(A^{-1})=1,\qquad \det(A^{-1})=\frac13.$$

Therefore

$$\det(A^{-1}B)=\det(A^{-1})\det B=\frac13(-5)=\boxed{-\frac53}.$$

The two product orders have equal scalar determinants; the next section explains what this does and does not imply for the matrices.

## 3. Distinguish equal determinants from equal products

The determinants of $AB$ and $BA$ agree because their scalar factors can be multiplied in either order. This does not allow the matrix factors themselves to be reordered.

For a concrete example consistent with the given determinant data, take

$$A=\begin{pmatrix}3&0\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}-5&1\\0&1\end{pmatrix}.$$

Then

$$AB=\begin{pmatrix}-15&3\\0&1\end{pmatrix},\qquad BA=\begin{pmatrix}-15&1\\0&1\end{pmatrix}.$$

The upper-right entries differ, while both triangular products have determinant $-15$. This illustrates exactly what the determinant equality establishes and why it cannot establish equality of the matrices.

## 4. Verification

The identity $A(A^{-1}B)=B$ requires

$$\det A\cdot\det(A^{-1}B)=3\left(-\frac53\right)=-5=\det B.$$

Also both $A$ and $B$ have nonzero determinants, so $AB$, $BA$, and $A^{-1}B$ are invertible. All three computed determinants are nonzero, consistently with that conclusion. The existence check concerns $A^{-1}$ specifically; it is not enough merely to know that $B$ is invertible.
