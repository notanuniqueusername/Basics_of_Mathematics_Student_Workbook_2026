# Exercise 1. Determinant of a 2×2 Matrix

## The question

Compute
$$\det\begin{pmatrix}3&-2\\5&4\end{pmatrix},\qquad \det\begin{pmatrix}1&7\\2&14\end{pmatrix}.$$
Which matrix is invertible? Justify your answer.

## Before calculating: the concepts

For $M=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, $\det M=ad-bc$. A square matrix is invertible exactly when its determinant is nonzero.

## 1. Identify the two diagonal products

For a $2\times2$ determinant, the positive product runs from the upper left to the lower right. The product from the upper right to the lower left is subtracted. A negative entry inside the second product must retain its sign: subtracting a negative product adds its absolute value.

## 2. Calculate each determinant

Call the matrices $M_1$ and $M_2$. For the first matrix, identify $a=3$, $b=-2$, $c=5$, and $d=4$:

$$\det M_1=ad-bc=3\cdot4-(-2)\cdot5=12-(-10)=\boxed{22}.$$

The parentheses matter: the second diagonal product is $-10$, and the formula subtracts that product. Since $22\ne0$, $M_1$ is invertible.

For the second matrix, $a=1$, $b=7$, $c=2$, and $d=14$:

$$\det M_2=1\cdot14-7\cdot2=14-14=\boxed{0}.$$

Thus $M_2$ has no inverse. The determinant test gives a different conclusion for each matrix.

## 3. Connect the numbers with invertibility

The determinant criterion applies separately to the two matrices. A nonzero determinant means two independent rows and an inverse; a zero determinant means dependence. The answer therefore needs both a numerical calculation and an invertibility conclusion for each matrix.

## 4. Verification

**First matrix: verify an inverse.** Put $C=\frac1{22}\begin{pmatrix}4&2\\-5&3\end{pmatrix}$. Then

$$M_1C=\frac1{22}\begin{pmatrix}3\cdot4+(-2)(-5)&3\cdot2+(-2)3\\5\cdot4+4(-5)&5\cdot2+4\cdot3\end{pmatrix}=\frac1{22}\begin{pmatrix}22&0\\0&22\end{pmatrix}=I.$$

**Second matrix: inspect the rows.** Its second row is $2(1,7)=(2,14)$, so the rows are dependent. Also $M_2(-7,1)^T=(-7+7,-14+14)^T=0$ despite $(-7,1)^T\ne0$. Both checks agree with singularity.
