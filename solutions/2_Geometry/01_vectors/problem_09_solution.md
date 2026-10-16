# Exercise 9. Cross Product as a Perpendicular Direction

## The question

For $u=(1,2,0)$ and $v=(0,1,3)$ compute $u\times v$. Use dot products to check perpendicularity to both vectors, compute $v\times u$, and compare the results.

## Before calculating: cross product and orientation

For $u,v\in\mathbb R^3$, the cross product is $(u_2v_3-u_3v_2,u_3v_1-u_1v_3,u_1v_2-u_2v_1)$. It is perpendicular to both inputs, and reversing their order negates the result.

The cross product's magnitude is $\|u\|\|v\|\sin\theta$, the parallelogram area, while its orientation follows the right-hand rule. A nonzero product therefore proves the two inputs are not parallel. Orthogonality alone fixes a normal line but not the length or one of its two orientations, so checking only dot products would not verify the entire cross product.

## 1. Calculate the cross product

$$u\times v=(2\cdot3-0\cdot1,0\cdot0-1\cdot3,1\cdot1-2\cdot0)=\boxed{(6,-3,1)}.$$

The second component uses $u_3v_1-u_1v_3$; this sign is easy to reverse when expanding a formal determinant.

## 2. Reverse the arguments

$$v\times u=(1\cdot0-3\cdot2,3\cdot1-0\cdot0,0\cdot2-1\cdot1)=\boxed{(-6,3,-1)}.$$

Hence $v\times u=-(u\times v)$. The normal direction reverses, but its length and the plane to which it is normal remain the same. The right-hand rule distinguishes the two orientations.

## 3. Explain the signs through cofactor expansion

The formal determinant mnemonic is

$$u\times v=\begin{vmatrix}\mathbf i&\mathbf j&\mathbf k\\1&2&0\\0&1&3\end{vmatrix}=\mathbf i(2\cdot3-0\cdot1)-\mathbf j(1\cdot3-0\cdot0)+\mathbf k(1\cdot1-2\cdot0).$$

The middle cofactor is subtracted, producing $-3$, not $+3$. The result has length $\sqrt{46}$, so the spanned parallelogram has that area. Reversing the arguments reverses the normal orientation but preserves $\sqrt{46}$. This distinction explains why $v\times u$ is the negative vector rather than an unrelated perpendicular vector of the same magnitude.

## 4. Verification

Test both required perpendicularities:

$$(6,-3,1)\cdot(1,2,0)=6-6+0=0,$$

$$(6,-3,1)\cdot(0,1,3)=0-3+3=0.$$

Check its magnitude using $\|u\times v\|^2=\|u\|^2\|v\|^2-(u\cdot v)^2$: the right side is $5\cdot10-2^2=46$, while the result gives $6^2+(-3)^2+1^2=46$. Thus direction and magnitude both check.

**Separate normal direction from area magnitude.** Any nonzero multiple of $(6,-3,1)$ would be perpendicular to both inputs, but most would have the wrong magnitude for their cross product. In particular $2(6,-3,1)$ would pass both zero-dot-product tests while doubling the parallelogram area incorrectly. The identity yielding squared norm $46$ rules this out. Conversely the negative vector has the correct magnitude but the reversed orientation, which is why computing $v\times u$ separately matters. A complete cross-product check therefore considers all three properties: perpendicularity, magnitude, and argument order.
