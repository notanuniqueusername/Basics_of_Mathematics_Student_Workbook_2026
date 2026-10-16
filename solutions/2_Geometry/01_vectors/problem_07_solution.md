# Exercise 7. Linear Dependence Without Heavy Computation

## The question

Given
$$u=(1,2,3),\qquad v=(2,4,6),\qquad w=(0,1,1).$$
Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

## Before calculating: a dependence relation

Vectors are linearly dependent if some linear combination equals zero with coefficients not all zero. To prove dependence it is enough to exhibit one such relation; solving a full system is unnecessary.

A dependence relation may use a zero coefficient on some vectors. The condition is that the coefficients are not all zero, rather than that every coefficient be nonzero. This is why an already dependent pair remains dependent when another vector is added, even if the new vector points outside the line spanned by that pair.

## 1. Compare the coordinates

$$2u=2(1,2,3)=(2,4,6)=v.$$

Thus $v$ has exactly the same direction and orientation as $u$, but twice its length.

## 2. Give a dependence involving the entire set

$$\boxed{2u-v+0w=0}.$$

The coefficients $(2,-1,0)$ are not all zero. Therefore $u,v,w$ cannot be linearly independent, regardless of the coordinates of $w$. A subset containing a dependence makes the whole set dependent.

## 3. Describe exactly what the third vector adds

Every combination of the three given vectors can be rewritten as

$$\alpha u+\beta v+\gamma w=(\alpha+2\beta)u+\gamma w.$$

Thus $v$ supplies no extra direction; the same set of outputs is obtained using just $u$ and $w$. To check those remaining two directions are independent, suppose $su+tw=0$. The first coordinate gives $s=0$; the second then gives $t=0$.

Consequently the full triple is dependent but spans a two-dimensional plane. Dependence does not mean that all three vectors must be parallel or that every pair is dependent. The explicit relation $2u-v=0$ is sufficient to settle the exercise without a determinant calculation.

## 4. Describe the geometry

Although $w$ does not repair independence of the triple, it does supply a direction different from $u$. If $w=cu$, its first coordinate would imply $c=0$, but then its second coordinate would also be zero, contrary to $w_2=1$. Hence the span of all three is a plane through the origin, not just a line: $v$ adds nothing beyond $u$, while $w$ adds a second independent direction.

## 5. Verification

Check the relation directly:

$$2(1,2,3)-(2,4,6)+0(0,1,1)=(0,0,0).$$

The zero coefficient of $w$ is allowed. Linear dependence does not require every coefficient to be nonzero; it requires only that at least one coefficient be nonzero, which is satisfied here.
