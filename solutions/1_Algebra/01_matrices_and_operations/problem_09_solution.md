# Exercise 9. Composing Transformations

## The question

We are given

$$S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad R=\begin{pmatrix}0&-1\\1&0\end{pmatrix},\qquad x=\begin{pmatrix}1\\2\end{pmatrix}.$$

$S$ is a nonuniform scaling (stretches the $x$-direction by 2), and $R$ is a $90^\circ$ counterclockwise rotation. Compute $RSx$ and $SRx$, compare, and explain geometrically why the order matters.

## Before calculating: how to read a product of transformations

A matrix acts on a vector by multiplication from the left. So in $RSx$, the vector $x$ meets $S$ first, and the result then meets $R$:

$$RSx=R(Sx):\quad\text{first } S,\ \text{then } R.$$

Products of transformations are read **right to left**, the same way nested functions are: $f(g(x))$ applies $g$ first.

First, a quick check of what each matrix does to the basic vectors, since the columns of a matrix are the images of $e_1,e_2$ (Exercise 5):

- $S e_1=(2,0)$, $Se_2=(0,1)$: the $x$-direction is stretched, the $y$-direction is untouched.
- $Re_1=(0,1)$, $Re_2=(-1,0)$: $e_1$ turns into $e_2$, and $e_2$ turns into $-e_1$, which is a quarter turn counterclockwise.

## 1. Compute $RSx$ (scale first, then rotate)

Scale:

$$Sx=\begin{pmatrix}2\cdot1+0\cdot2\\0\cdot1+1\cdot2\end{pmatrix}=\begin{pmatrix}2\\2\end{pmatrix}.$$

Rotate:

$$R(Sx)=\begin{pmatrix}0\cdot2+(-1)\cdot2\\1\cdot2+0\cdot2\end{pmatrix}=\begin{pmatrix}-2\\2\end{pmatrix}.$$

So $RSx=\begin{pmatrix}-2\\2\end{pmatrix}$.

## 2. Compute $SRx$ (rotate first, then scale)

Rotate:

$$Rx=\begin{pmatrix}0\cdot1+(-1)\cdot2\\1\cdot1+0\cdot2\end{pmatrix}=\begin{pmatrix}-2\\1\end{pmatrix}.$$

Scale:

$$S(Rx)=\begin{pmatrix}2\cdot(-2)+0\cdot1\\0\cdot(-2)+1\cdot1\end{pmatrix}=\begin{pmatrix}-4\\1\end{pmatrix}.$$

So $SRx=\begin{pmatrix}-4\\1\end{pmatrix}$.

## 3. Compare

$$RSx=\begin{pmatrix}-2\\2\end{pmatrix}\neq\begin{pmatrix}-4\\1\end{pmatrix}=SRx.$$

The two orders end at different points, so the transformations do not commute.

## 4. Why the order matters geometrically

The key is that $S$ treats the two axes **differently**, while $R$ changes which direction is which.

- **Scale, then rotate.** Starting at $(1,2)$, scaling stretches the horizontal part and gives $(2,2)$. Then the rotation turns this vector a quarter turn, to $(-2,2)$. The stretch happened along the original $x$-axis.
- **Rotate, then scale.** Starting at $(1,2)$, the rotation gives $(-2,1)$. Now the horizontal direction contains what used to be the vertical part of $x$, so the stretch by 2 acts on the old $y$-component: $(-2,1)\to(-4,1)$. The stretch happened along the old $y$-axis.

So the same stretch is applied to different parts of the vector, depending on whether the rotation came first. If $S$ had been a uniform scaling, such as $2I$, the order would not matter, because stretching equally in all directions does not care which way the vector points. The failure of commutativity comes entirely from $S$ favoring one direction.

The same conclusion appears in the matrices themselves:

$$RS=\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}2&0\\0&1\end{pmatrix}=\begin{pmatrix}0&-1\\2&0\end{pmatrix},\qquad SR=\begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}0&-1\\1&0\end{pmatrix}=\begin{pmatrix}0&-2\\1&0\end{pmatrix}.$$

These are different matrices, so $RS\ne SR$.

## 5. Verification

**Apply the product matrices directly to $x$.** Composition should equal multiplication by the product matrix:

$$RS\,x=\begin{pmatrix}0&-1\\2&0\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}-2\\2\end{pmatrix}.\ ✓$$

$$SR\,x=\begin{pmatrix}0&-2\\1&0\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}-4\\1\end{pmatrix}.\ ✓$$

**Length check.** A rotation preserves length, so $\|RSx\|$ should equal $\|Sx\|$, and $\|Rx\|$ should equal $\|x\|$:

$$\|Sx\|=\sqrt{2^2+2^2}=\sqrt8=\|RSx\|=\sqrt{(-2)^2+2^2}.\ ✓$$

$$\|x\|=\sqrt5=\|Rx\|=\sqrt{(-2)^2+1^2}.\ ✓$$

**Determinant check.** $\det S=2$ and $\det R=1$, so both products should have determinant $2$ (area doubles, in either order):

$$\det(RS)=0\cdot0-(-1)\cdot2=2,\qquad \det(SR)=0\cdot0-(-2)\cdot1=2.\ ✓$$

The areas scale the same way in both orders, yet the resulting transformations differ, which is the same pattern we saw in Exercise 4.
