# Exercise 1. Vector Operations and Their Meaning

## The question

For $u=(2,-1,3)$ and $v=(-1,4,2)$ compute
$$u+v,\qquad u-v,\qquad 3u-2v.$$
Then verify that $(u+v)-v=u$, and explain geometrically what adding two vectors means.

## Before calculating: component operations

For vectors of the same dimension, addition and subtraction pair corresponding coordinates; scalar multiplication multiplies every coordinate. A vector describes a displacement, independent of its starting point.

Componentwise operations preserve coordinate positions: the first entries combine with the first entries, and so on. For $u=(u_1,u_2,u_3)$ and $v=(v_1,v_2,v_3)$, $\alpha u+\beta v=(\alpha u_1+\beta v_1,\alpha u_2+\beta v_2,\alpha u_3+\beta v_3)$. This is the vector version of the entrywise matrix operations in the reference set.

## 1. Add and subtract

$$u+v=(2+(-1),-1+4,3+2)=\boxed{(1,3,5)},$$

$$u-v=(2-(-1),-1-4,3-2)=\boxed{(3,-5,1)}.$$

Subtracting $-1$ in the first coordinate adds $1$; the minus sign must act on all coordinates of $v$.

## 2. Form the linear combination

First compute $3u=(6,-3,9)$ and $2v=(-2,8,4)$. Then

$$3u-2v=(6-(-2),-3-8,9-4)=\boxed{(8,-11,5)}.$$

## 3. Explain scaling and check the combination another way

The vector $3u$ follows the same direction as $u$ and has three times its length. The term $-2v$ follows the opposite direction to $v$ and has twice its length. Adding those two displacements gives $3u-2v$.

We can also group the computation as $u+2(u-v)$:

$$u+2(u-v)=(2,-1,3)+2(3,-5,1)=(2+6,-1-10,3+2)=(8,-11,5).$$

This checks the linear combination using the already computed difference, rather than repeating the original pair of scalar multiplications. The identity follows from distributivity: $u+2(u-v)=u+2u-2v$.

## 4. Geometric meaning

To add, place the tail of $v$ at the head of $u$. The vector from the original starting point to the final point is $u+v$. Equivalently, it is the diagonal of the parallelogram spanned by $u,v$. Subtraction adds the opposite vector, while scaling changes length and possibly orientation.

## 5. Verification

Undo addition:

$$(u+v)-v=(1-(-1),3-4,5-2)=(2,-1,3)=u.$$

Independently, rebuild the linear combination from the sum and difference:

$$\tfrac12(u+v)+\tfrac52(u-v)=\tfrac12(1,3,5)+\tfrac52(3,-5,1)=(8,-11,5).$$

Both calculations confirm the signs and coordinate positions.

**Undo the other operations as well.** Adding $v$ back to the difference gives $(3,-5,1)+(-1,4,2)=(2,-1,3)=u$. Adding $2v$ back to the linear combination gives $(8,-11,5)+(-2,8,4)=(6,-3,9)=3u$. Dividing the latter result by $3$ recovers $u$ again. These reverse-operation checks separately verify subtraction and the scalar combination, so correctness of the sum is not being used as evidence for unrelated results. All three calculations use the same coordinate order, preserving their geometric displacement interpretation.
