# Exercise 6. Solving a System Using the Inverse

## The question

Solve
$$Ax=b,$$
where
$$A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}5\\7\end{pmatrix},$$
using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

## Before calculating: the concepts

Multiplying $Ax=b$ on the left by $A^{-1}$ gives $x=A^{-1}b$.

## 1. Find the inverse before applying it

The determinant is $2\cdot3-1\cdot1=5$, so an inverse exists. The unknown is a two-entry column vector, and $A^{-1}b$ is a valid $(2\times2)(2\times1)$ product. The right-hand side belongs on the right of the inverse.

## 2. Compute the solution vector

Use the $2\times2$ inverse rule

$$M=\begin{pmatrix}a&b\\c&d\end{pmatrix},\qquad M^{-1}=\frac1{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix},\qquad ad-bc\ne0.$$

For the given $A$, exchange the diagonal entries $2,3$, negate the off-diagonal entries $1,1$, and divide every entry by the determinant $5$:

$$\det A=2\cdot3-1\cdot1=5,\qquad A^{-1}=\frac15\begin{pmatrix}3&-1\\-1&2\end{pmatrix}.$$

Multiplying $Ax=b$ on the left gives

$$A^{-1}Ax=A^{-1}b\quad\Longrightarrow\quad Ix=A^{-1}b\quad\Longrightarrow\quad x=A^{-1}b.$$

Compute the two row-column products:

$$x=\frac15\begin{pmatrix}3\cdot5+(-1)7\\(-1)5+2\cdot7\end{pmatrix}=\frac15\begin{pmatrix}8\\9\end{pmatrix}=\boxed{\begin{pmatrix}8/5\\9/5\end{pmatrix}}.$$

The result is a $2\times1$ vector, matching the number of unknowns.

## 3. Interpret the two entries

The first coordinate is $(3\cdot5-1\cdot7)/5=8/5$, and the second is $(-1\cdot5+2\cdot7)/5=9/5$. These are the two unknowns in the original system. Since $A$ is invertible, the vector found is the only possible solution, not just one example.

## 4. Verification

**Check the inverse used in the method:**

$$AA^{-1}=\frac15\begin{pmatrix}2\cdot3+1(-1)&2(-1)+1\cdot2\\1\cdot3+3(-1)&1(-1)+3\cdot2\end{pmatrix}=\frac15\begin{pmatrix}5&0\\0&5\end{pmatrix}=I.$$

**Check the solution in the original equation:**

$$Ax=\begin{pmatrix}2(8/5)+9/5\\8/5+3(9/5)\end{pmatrix}=\begin{pmatrix}25/5\\35/5\end{pmatrix}=\begin{pmatrix}5\\7\end{pmatrix}=b.$$

Both equations hold. Invertibility establishes uniqueness in addition to this existence check.
