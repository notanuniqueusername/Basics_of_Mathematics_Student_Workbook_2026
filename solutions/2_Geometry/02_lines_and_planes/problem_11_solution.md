# Exercise 11. Plane Containing a Line and a Point

## The question

Find the equation of the plane containing
$$(x,y,z)=(1,0,2)+t(1,1,-1)$$
and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

## Before calculating: obtain two directions in the required plane

A plane containing a line must contain its direction $v$. Joining a point on the line to the extra point gives another direction $w$. If they are independent, $v\times w$ is a nonzero normal and the plane is unique.

The vector from the line's anchor to the extra point need not itself be perpendicular to anything; its purpose is to provide another direction in the desired plane. Only their cross product is the normal. If the point were already on the line, these directions would be dependent and the construction would not select a unique plane.

## 1. Construct the normal

Use the line anchor $A=(1,0,2)$ and direction $v=(1,1,-1)$:

$$w=P-A=(0,2,1)-(1,0,2)=(-1,2,-1).$$

$$n=v\times w=(1(-1)-(-1)2,(-1)(-1)-1(-1),1\cdot2-1(-1))=(1,2,3).$$

Since $n\ne0$, the directions are independent.

## 2. Write the plane

$$n\cdot(X-A)=0\quad\Longrightarrow\quad(x-1)+2y+3(z-2)=0.$$

Thus $\boxed{x+2y+3z=7}$.

## 3. Establish uniqueness and check the entire plane family

The extra point is not on the line. Its first coordinate would require $t=-1$, but then the line's second coordinate would be $-1$, not $2$. Thus the extra point truly contributes another independent direction, consistent with the nonzero cross product.

A general point of the resulting plane is

$$X=A+sv+tw=(1+s-t,s+2t,2-s-t).$$

Substituting gives

$$x+2y+3z=1+s-t+2s+4t+6-3s-3t=7.$$

Both parameter coefficients vanish. The original line is the subfamily $t=0$, and the additional point is reached at $s=0,t=1$. This shows exactly how the construction includes both required objects.

## 4. Verification

The extra point gives $0+2\cdot2+3\cdot1=7$. Every line point gives

$$(1+t)+2t+3(2-t)=1+t+2t+6-3t=7.$$

So the whole line, not just its anchor, lies in the plane. Finally $n\cdot v=1+2-3=0$ and $n\cdot w=-1+4-3=0$, independently checking the normal construction.

**Check how normal scaling affects the equation.** Reversing the cross product gives $(-1,-2,-3)$ instead of $(1,2,3)$. Using the same anchor then produces $-x-2y-3z=-7$, exactly the same plane after multiplication by $-1$. Changing the normal's sign without changing the constant would instead produce a different parallel plane. The valid constant is always computed as the chosen normal dotted with the anchor. Here $1+0+6=7$, so the orientation and location checks remain consistent whichever cross-product order is used.
