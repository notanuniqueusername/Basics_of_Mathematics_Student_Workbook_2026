# Exercise 13. Undoing a Composite Transformation

## The question

The matrices
$$S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad H=\begin{pmatrix}1&1\\0&1\end{pmatrix}$$
describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

## Before calculating: the concepts

For column vectors, $HS$ applies $S$ first, then $H$. Undo the operations in reverse order.

## 1. Record the transformation order

For a column vector, the rightmost matrix acts first. In $T=HS$, the scaling $S$ acts before the shear $H$. The inverse must remove the shear first, using $H^{-1}$, and then remove the scaling, using $S^{-1}$. Written as a product, this is $S^{-1}H^{-1}$.

## 2. Compute the direct and factored inverses

**Method 1: form $T$ and invert it.**

$$T=HS=\begin{pmatrix}1\cdot2+1\cdot0&1\cdot0+1\cdot1\\0\cdot2+1\cdot0&0\cdot0+1\cdot1\end{pmatrix}=\begin{pmatrix}2&1\\0&1\end{pmatrix}.$$

For $M=\begin{pmatrix}a&b\\c&d\end{pmatrix}$ with nonzero determinant, the inverse rule is

$$M^{-1}=\frac1{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}.$$

Here $\det T=2\cdot1-1\cdot0=2$. Swap the diagonal entries $2,1$, negate the off-diagonal entries $1,0$, and divide by $2$:

$$T^{-1}=\frac12\begin{pmatrix}1&-1\\0&2\end{pmatrix}=\begin{pmatrix}1/2&-1/2\\0&1\end{pmatrix}.$$

**Method 2: undo the factors in reverse order.** The scaling $S$ sends $(x,y)^T$ to $(2x,y)^T$, so its inverse uses reciprocal diagonal factors $1/2$ and $1$. The shear $H$ sends $(x,y)^T$ to $(x+y,y)^T$, so its inverse subtracts the second coordinate from the first. Thus

$$S^{-1}=\begin{pmatrix}1/2&0\\0&1\end{pmatrix},\qquad H^{-1}=\begin{pmatrix}1&-1\\0&1\end{pmatrix}.$$

Multiplying in reverse order gives

$$S^{-1}H^{-1}=\begin{pmatrix}(1/2)1&(1/2)(-1)\\0&1\end{pmatrix}=\boxed{\begin{pmatrix}1/2&-1/2\\0&1\end{pmatrix}}.$$

The two answers agree. In contrast, the other order gives

$$H^{-1}S^{-1}=\begin{pmatrix}1(1/2)&(-1)1\\0&1\end{pmatrix}=\begin{pmatrix}1/2&-1\\0&1\end{pmatrix},$$

whose upper right entry differs.

## 3. Compare the off-diagonal entries

The correct inverse has upper right entry $-1/2$; the product in the other order has upper right entry $-1$. This difference matters whenever the input has a nonzero second coordinate. For example, the correct inverse sends $(0,1)^T$ to $(-1/2,1)^T$, which $T$ sends back to $(0,1)^T$.

## 4. Verification

Check the correct inverse $C$:

$$TC=\begin{pmatrix}2(1/2)&2(-1/2)+1\cdot1\\0&1\end{pmatrix}=I,\qquad CT=\begin{pmatrix}1&(1/2)1+(-1/2)1\\0&1\end{pmatrix}=I.$$

For the incorrect product $W=H^{-1}S^{-1}$,

$$TW=\begin{pmatrix}1&2(-1)+1\cdot1\\0&1\end{pmatrix}=\begin{pmatrix}1&-1\\0&1\end{pmatrix}\ne I.$$

A vector makes the failure visible: $W(0,1)^T=(-1,1)^T$, then $T(-1,1)^T=(-1,1)^T$, which does not recover $(0,1)^T$. The correct inverse sends $(0,1)^T$ to $(-1/2,1)^T$, which $T$ sends back to $(0,1)^T$.
