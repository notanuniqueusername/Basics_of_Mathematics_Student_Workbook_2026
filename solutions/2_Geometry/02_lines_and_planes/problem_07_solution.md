# Exercise 7. A Line Relative to a Plane

## The question

For
$$L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,$$
determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

## Before calculating: the line–plane test

Substituting $p+tv$ into $n\cdot X=d$ gives $n\cdot p+t(n\cdot v)=d$. If $n\cdot v=0$, either every parameter works or no parameter works, depending on the anchor point.

A zero normal-direction dot product says the line's displacement never changes the plane residual. It does not by itself say the residual is zero. The anchor-point test determines whether the unchanged residual is zero everywhere or nonzero everywhere. These are containment and disjoint parallelism, respectively.

## 1. Test the direction

Here $p=(1,1,0)$, $v=(1,-1,0)$, $n=(1,1,1)$, and $d=2$.

$$n\cdot v=1-1+0=0.$$

Thus the line's direction is parallel to the plane. This alone does not decide whether the line lies in it.

## 2. Test the anchor point

$$n\cdot p=1+1+0=2=d.$$

The anchor is in the plane, so every point of the line is in it:

$$\boxed{L\subset\Pi}.$$

There is no unique intersection point; the common set is the entire line.

## 3. Derive the unchanged residual directly

For a general line point $X(t)=p+tv$, define its plane residual as $r(t)=n\cdot X(t)-d$. Linearity gives

$$r(t)=n\cdot p-d+t(n\cdot v).$$

In this exercise both coefficients vanish: $n\cdot p-d=2-2=0$ and $n\cdot v=0$. Therefore $r(t)=0$ for every real parameter.

This proves containment without checking infinitely many points one by one. It also explains why solving the substituted plane equation leaves an identity $2=2$ rather than a specific value of $t$. An identity means every parameter is allowed; it is not a failed attempt to find a unique intersection.

## 4. Verification

A general point of $L$ is $(1+t,1-t,0)$. Its coordinate sum is

$$(1+t)+(1-t)+0=2$$

for every real $t$. For concrete examples, $t=0$ gives $(1,1,0)$ and $t=1$ gives $(2,0,0)$, both satisfying the plane. An anchor outside the plane with the same direction would instead describe a parallel disjoint line, which explains why both tests were necessary.
