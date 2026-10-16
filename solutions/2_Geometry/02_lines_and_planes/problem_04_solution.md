# Exercise 4. Plane Through Three Points

## The question

Find the equation of the plane through
$$A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).$$
First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

## Before calculating: construct the normal from directions

Two independent displacement vectors between three noncollinear points lie in their plane. Their nonzero cross product supplies a plane normal.

A nonzero cross product verifies noncollinearity at the same time that it constructs the normal. Three points alone do not always determine a plane uniquely: if their two displacement directions were proportional, infinitely many planes would pass through their common line. The calculation must therefore retain and interpret the nonzero result.

## 1. Construct the directions and normal

$$a=B-A=(-1,1,0),\qquad b=C-A=(-1,0,1).$$

$$a\times b=(1\cdot1-0\cdot0,0(-1)-(-1)1,(-1)0-1(-1))=(1,1,1).$$

The cross product is nonzero, so the points are noncollinear and determine one plane.

## 2. Write the point-normal equation

Using $A=(1,0,0)$,

$$(1,1,1)\cdot(x-1,y,z)=0,$$

hence

$$\boxed{x+y+z=1}.$$

Reversing the order of the cross product would negate all coefficients and produce an equivalent equation.

## 3. Relate the plane equation to coordinate intercepts

The original points lie one unit along the three coordinate axes, so a plane with equation $x+y+z=1$ has exactly the prescribed intercepts. This is a geometric check of the algebra, not an alternative assumption used to skip the cross product.

To see the whole plane, write

$$X=A+sa+tb=(1-s-t,s,t).$$

The coordinates sum to $1$ for every $s,t$. Conversely, if $x+y+z=1$, choosing $s=y$ and $t=z$ makes $1-s-t=x$. Thus every solution of the equation is obtained from the two constructed directions. The plane equation and the point-direction description are exactly equivalent.

## 4. Verification

The three point substitutions give $1+0+0=1$, $0+1+0=1$, and $0+0+1=1$.

Also $(1,1,1)\cdot(-1,1,0)=0$ and $(1,1,1)\cdot(-1,0,1)=0$, checking the normal independently. A general point $A+sa+tb=(1-s-t,s,t)$ has coordinate sum $1$, showing the entire plane spanned by these two directions agrees with the equation.

**Distinguish the plane from the triangle it contains.** In the representation $A+sa+tb$, arbitrary real $s,t$ describe the full infinite plane. Restricting instead to $s\ge0$, $t\ge0$, and $s+t\le1$ would describe only the filled triangle with vertices $A,B,C$. The plane equation $x+y+z=1$ imposes no such inequalities. For example, $(2,-1,0)$ satisfies it and belongs to the plane but lies outside the triangle. This distinction matters when using a sketch of three points: the requested plane continues beyond their bounded triangular outline.
