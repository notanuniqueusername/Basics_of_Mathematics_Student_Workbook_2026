# Exercise 5. Relative Position of Two Lines

## The question

Analyze the position of
$$L_1:(x,y,z)=(1,1,0)+t(1,2,1),$$
$$L_2:(x,y,z)=(2,0,1)+s(0,1,-1).$$
If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

## Before calculating: classify before guessing an intersection

Spatial lines may intersect, be parallel, coincide, or be skew. Nonparallel directions rule out the parallel cases; consistency of the three coordinate equations determines whether they intersect.

In space, nonparallel lines need not intersect: they can pass at different heights and be skew. Two coordinate equations can agree while the third fails. This differs from the plane, where two nonparallel lines necessarily intersect. The third coordinate must be treated as a genuine compatibility condition, not a redundant check.

## 1. Compare directions

$$v_1=(1,2,1),\qquad v_2=(0,1,-1).$$

They cannot be proportional because their first coordinates are $1$ and $0$. Thus the lines are not parallel or coincident.

## 2. Solve the intersection conditions

Equating coordinates gives

$$1+t=2,\qquad 1+2t=s,\qquad t=1-s.$$

The first equation forces $t=1$; the second then forces $s=3$. But the third would require $1=1-3=-2$, impossible.

Therefore $\boxed{L_1\text{ and }L_2\text{ are skew}}$: they are nonparallel and have no common point.

## 3. Explain the failed candidate and the coplanarity check

The first equation fixes $t=1$ independently of $s$, because the second line has constant $x=2$. With $t$ fixed, matching the $y$ coordinates forces $s=3$. There are no remaining free parameters to repair the incompatible $z$ coordinates. Hence a second choice cannot rescue an intersection.

For a geometric test, $v_1\times v_2=(-3,1,1)$ is normal to the plane of the two direction vectors. If the lines lay in one plane, the anchor displacement $(1,-1,1)$ would be perpendicular to that normal. Its dot product is $-3\ne0$, so it leaves that direction plane. This explains the skew classification geometrically as well as algebraically.

## 4. Verification

The candidate parameters give $L_1(1)=(2,3,1)$ and $L_2(3)=(2,3,-2)$. Their first two coordinates match, but their heights differ by $3$, illustrating why two equations alone cannot establish intersection.

An independent coplanarity test gives $v_1\times v_2=(-3,1,1)$ and $p_2-p_1=(1,-1,1)$. Their dot product is $-3-1+1=-3\ne0$, confirming the lines do not lie in one plane and are skew.
