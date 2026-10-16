# Exercise 14. A Matrix That Is Its Own Inverse

## The question

Assume that a square matrix $A$ satisfies
$$A^2=I.$$
Show that
$$A^{-1}=A.$$
Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

## Before calculating: the concepts

A matrix $B$ is the inverse of $A$ if $AB=BA=I$.

## 1. Return to the definition of an inverse

The equation $A^2=I$ is the same as $AA=I$. The candidate inverse is therefore already present: it is $A$ itself. Because both factors are the same matrix, this one equality supplies both orders required by the inverse definition.

## 2. Prove the claim and choose an example

The defining equations for an inverse $B$ are $AB=I$ and $BA=I$. Choose $B=A$. The assumption $A^2=I$ gives

$$AB=AA=A^2=I,\qquad BA=AA=A^2=I.$$

Thus $\boxed{A^{-1}=A}$.

For a concrete example, take

$$A=\begin{pmatrix}0&1\\1&0\end{pmatrix}.$$

It differs from $I$ and $-I$ because its diagonal entries are zero and its off-diagonal entries are $1$. Its action is $(x,y)^T\mapsto(y,x)^T$, so applying it twice restores the original coordinates.

## 3. Interpret the example

The example matrix interchanges the two coordinates. Applying it twice interchanges them twice and therefore returns the original vector. This provides a concrete transformation with $A^2=I$ that is different from leaving every vector unchanged or negating every vector.

## 4. Verification

Multiply the example by itself, entry by entry:

$$A^2=\begin{pmatrix}0\cdot0+1\cdot1&0\cdot1+1\cdot0\\1\cdot0+0\cdot1&1\cdot1+0\cdot0\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}=I.$$

As a vector check, $A(2,-3)^T=(-3,2)^T$ and $A(-3,2)^T=(2,-3)^T$. The determinant also obeys the necessary condition $(\det A)^2=\det(A^2)=1$; for this example $\det A=-1$, which indeed squares to $1$.
