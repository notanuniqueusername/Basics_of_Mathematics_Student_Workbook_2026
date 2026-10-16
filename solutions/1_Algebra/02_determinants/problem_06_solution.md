# Exercise 6. Parameter and Invertibility

## The question

For
$$A(t)=\begin{pmatrix}t&1\\2&t\end{pmatrix}$$
find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

## Before calculating: the concepts

A square matrix fails to be invertible precisely when its determinant is zero.

## 1. Translate noninvertibility into an equation

The parameter occurs in both diagonal positions. Multiply those entries to get $t^2$, then subtract the product of the off-diagonal entries, $1\cdot2$. The singular values are the roots of the resulting determinant polynomial.

## 2. Solve the determinant equation

The diagonal products are $t\cdot t=t^2$ and $1\cdot2=2$. Hence

$$\det A(t)=t^2-2.$$

Noninvertibility requires

$$t^2-2=0\quad\Longleftrightarrow\quad t^2=2\quad\Longleftrightarrow\quad \boxed{t=\sqrt2\ \text{or}\ t=-\sqrt2}.$$

For every other real value, $t^2-2\ne0$, so the matrix is invertible. Both roots are required: squaring removes the sign of $t$.

## 3. Explain how the determinant detects lost information

At a singular parameter, a nonzero input can be sent to the zero vector. Such a transformation cannot have an inverse: applying a supposed inverse would have to recover both that nonzero input and the zero input from the same output.

Here the determinant condition $t^2=2$ makes $R_2=tR_1$, so the second row supplies no independent information. The explicit zero-output vector in the verification below demonstrates that failure for both parameter values. For $t^2\ne2$, the inverse formula would instead have the valid nonzero denominator $t^2-2$. Thus the determinant separates an actual failure of invertibility from a mere difficulty in performing a calculation.

## 4. Verification

At either excluded value $t^2=2$, and

$$tR_1=t(t,1)=(t^2,t)=(2,t)=R_2.$$

Thus the rows are dependent at both values. Equivalently, the nonzero vector $v=(1,-t)^T$ satisfies

$$A(t)v=\begin{pmatrix}t-t\\2-t^2\end{pmatrix}=0.$$

As an ordinary allowed value, $t=0$ gives determinant $-2$, confirming that the matrix can be invertible even when its diagonal entries are zero.
