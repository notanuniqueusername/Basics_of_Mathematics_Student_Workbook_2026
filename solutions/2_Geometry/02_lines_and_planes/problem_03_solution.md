# Exercise 3. Plane Through a Point with a Given Normal Vector

## The question

Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

## Before calculating: normal form of a plane

A plane through $P$ with nonzero normal $n$ consists of all $X$ satisfying $n\cdot(X-P)=0$. Its displacement vectors are perpendicular to $n$.

In $n\cdot(X-P)=0$, the unknown is the entire point $X=(x,y,z)$. The subtraction produces a displacement that lies along the plane. The dot product forces that displacement to be perpendicular to the normal. This form is the three-dimensional counterpart of constructing a planar line from a point and normal.

## 1. Insert the point and normal

$$2(x-1)+(y+2)-(z-3)=0.$$

Each displacement coordinate subtracts the corresponding coordinate of $P$. Since $P_y=-2$, the second term is $y-(-2)=y+2$.

## 2. Simplify the equation

$$2x-2+y+2-z+3=0.$$

Therefore

$$\boxed{2x+y-z+3=0},\qquad\text{equivalently }2x+y-z=-3.$$

The coefficients of $x,y,z$ are the normal vector $(2,1,-1)$. The constant sets the plane's position; the normal fixes its orientation.

## 3. Check the constant and the orientation separately

The required constant is $d=n\cdot P=2(1)+1(-2)+(-1)3=-3$. Thus the plane must have equation $n\cdot X=-3$, consistent with the simplified answer. Choosing $+3$ on the right would produce a different parallel plane.

The normal itself is not an in-plane direction: moving from $P$ to $P+n=(3,-1,2)$ changes the value of $2x+y-z$ from $-3$ to $3$, a difference of $\|n\|^2=6$. This explicitly illustrates its perpendicular role. By contrast, any displacement $a$ satisfying $n\cdot a=0$ keeps $n\cdot(P+a)=-3$, so it stays within the plane.

## 4. Verification

Substituting $P$ gives $2\cdot1+(-2)-3+3=0$, so the plane passes through the required point.

For an independent direction check, choose $a=(1,-2,0)$ and $b=(0,1,1)$. Then $n\cdot a=2-2=0$ and $n\cdot b=1-1=0$. The points $P+a=(2,-4,3)$ and $P+b=(1,-1,4)$ satisfy the plane equation. These independent in-plane directions demonstrate that the stated normal is perpendicular to the entire plane.
