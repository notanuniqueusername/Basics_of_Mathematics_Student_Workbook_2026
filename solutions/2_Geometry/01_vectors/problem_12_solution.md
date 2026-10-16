# Exercise 12. A Normal Vector to a Plane

## The question

Given $A=(1,0,2)$, $B=(2,1,0)$, and $C=(0,3,1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

## Before calculating: constructing a plane normal

Differences of points in a plane give directions lying in that plane. The cross product of two nonparallel plane directions is a nonzero vector perpendicular to the plane. If the cross product vanished, the three points would be collinear and would not determine a unique plane.

A plane normal is defined only up to multiplication by a nonzero scalar. It must be perpendicular to two independent in-plane directions, not just one: a single direction has an entire plane of perpendicular vectors and cannot determine the plane's orientation. The nonzero cross product supplies both required perpendicularities at once.

## 1. Construct two directions

$$a=B-A=(2-1,1-0,0-2)=(1,1,-2),$$

$$b=C-A=(0-1,3-0,1-2)=(-1,3,-1).$$

## 2. Form the cross product

$$n=a\times b=(1(-1)-(-2)3,(-2)(-1)-1(-1),1\cdot3-1(-1))=\boxed{(5,3,4)}.$$

This is nonzero, so it is a valid normal and the three given points are noncollinear. Any nonzero scalar multiple, including $(-5,-3,-4)$, would describe the same normal direction.

## 3. Show why the normal equation describes the intended plane

Any point generated from the three data points has form

$$X=A+s(B-A)+t(C-A)=(1+s-t,s+3t,2-2s-t).$$

Taking the dot product with $n=(5,3,4)$ gives

$$5(1+s-t)+3(s+3t)+4(2-2s-t)=13,$$

because the coefficients of both $s$ and $t$ cancel. Thus the equation $5x+3y+4z=13$ holds throughout the plane spanned by the two directions.

The right-hand side is $n\cdot A=13$, not zero: the required plane does not pass through the origin. This explains why a correct normal by itself is insufficient to locate the plane; an anchor point is also required.

## 4. Verification

$$n\cdot a=5+3-8=0,\qquad n\cdot b=-5+9-4=0.$$

The resulting plane can be written $n\cdot((x,y,z)-A)=0$, or

$$5(x-1)+3y+4(z-2)=0\quad\Longleftrightarrow\quad5x+3y+4z=13.$$

All points check: $A$ gives $5+8=13$, $B$ gives $10+3=13$, and $C$ gives $9+4=13$. These point checks verify that the normal belongs to the intended plane, rather than merely to some parallel plane.
