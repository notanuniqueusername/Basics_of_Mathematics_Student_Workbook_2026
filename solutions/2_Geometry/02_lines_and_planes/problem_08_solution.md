# Exercise 8. Intersection Point of a Line and a Plane

## The question

Find the intersection point of
$$(x,y,z)=(1,0,2)+t(1,2,-1)$$
with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

## Before calculating: substitution finds the parameter

A point is common to the line and plane when the coordinates supplied by the line satisfy the plane equation. A nonzero coefficient of the line parameter ensures a unique intersection.

Substitution reduces the spatial intersection problem to one scalar equation because the line already imposes all its coordinate relations. Once the valid parameter is found, the resulting coordinates automatically lie on the line, but an explicit displacement check is still useful for catching arithmetic mistakes during substitution back.

## 1. Substitute the parametric coordinates

The line gives $x=1+t$, $y=2t$, and $z=2-t$. Hence

$$(1+t)+2t+(2-t)=4\quad\Longrightarrow\quad3+2t=4.$$

Thus $t=1/2$.

## 2. Recover the point

$$x=\frac32,\qquad y=1,\qquad z=\frac32.$$

Therefore

$$\boxed{L\cap\Pi=\left\{\left(\frac32,1,\frac32\right)\right\}}.$$

The direction is $v=(1,2,-1)$ and the normal is $n=(1,1,1)$; their dot product is $2\ne0$, explaining the nonzero parameter coefficient.

## 3. Interpret the coefficient of the parameter

The plane residual at the anchor is $1+0+2-4=-1$. Each unit increase in the parameter changes the residual by $n\cdot v=1+2-1=2$. The equation for reaching the plane is therefore $-1+2t=0$, which gives $t=1/2$.

This scalar residual viewpoint explains the uniqueness: the nonzero slope $2$ allows exactly one crossing. It also predicts the sign of the parameter before solving. The anchor is on the negative-residual side, and positive parameter changes increase the residual, so a positive parameter is necessary. The computed point has exactly the required displacement in that direction.

## 4. Verification

The coordinate sum at the point is $3/2+1+3/2=4$, so it lies in the plane.

Its displacement from the line anchor is

$$\left(\frac32,1,\frac32\right)-(1,0,2)=\left(\frac12,1,-\frac12\right)=\frac12(1,2,-1),$$

so it also lies on the line. These are separate membership checks; satisfying only the plane equation would not identify the required point.

**Check the intersection's invariance under reparametrization.** Using direction $2v$ instead gives $X(s)=p+s(2v)$ for the same geometric line. The substituted plane equation becomes $3+4s=4$, so $s=1/4$. Its displacement is $(1/4)(2v)=v/2$, exactly the previous displacement at $t=1/2$. Thus the point is unchanged even though its parameter differs. This is a useful consistency check: an intersection is a geometric location, while the parameter value depends on the chosen direction-vector scale and has no intrinsic meaning by itself.
