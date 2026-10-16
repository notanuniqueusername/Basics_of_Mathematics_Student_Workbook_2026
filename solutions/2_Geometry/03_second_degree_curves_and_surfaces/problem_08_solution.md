# Exercise 8. Sphere

## The question

Reduce
$$x^2+y^2+z^2-4x+2y-6z-2=0$$
to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

## Before calculating: a sphere uses three completed squares

The canonical equation is $(x-h)^2+(y-k)^2+(z-l)^2=r^2$, with center $(h,k,l)$. All three squared-coordinate coefficients are equal, so no directional rescaling is needed here.

A sphere is the set of points at a fixed distance from one center. Its equation follows by squaring that distance, so the constant on the right is radius squared. Completing three squares must keep all three compensating constants, including the original constant term, or the resulting radius will be wrong even if the center is correct.

## 1. Complete the squares

$$x^2-4x=(x-2)^2-4,$$

$$y^2+2y=(y+1)^2-1,\qquad z^2-6z=(z-3)^2-9.$$

Substitution gives

$$(x-2)^2+(y+1)^2+(z-3)^2-4-1-9-2=0.$$

Hence

$$\boxed{(x-2)^2+(y+1)^2+(z-3)^2=16}.$$

The center is $\boxed{(2,-1,3)}$ and radius $\boxed{4}$.

## 2. Construct two sphere points

Move four units in the positive and negative $x$ directions from the center:

$$P=(6,-1,3),\qquad Q=(-2,-1,3).$$

Their displacements from the center are $(4,0,0)$ and $(-4,0,0)$, each of length $4$.

## 3. Read the translation as a distance equation

With shifted coordinates $X=x-2$, $Y=y+1$, and $Z=z-3$, the canonical equation becomes

$$X^2+Y^2+Z^2=16.$$

Thus every sphere point has displacement of length $4$ from $(2,-1,3)$. The extreme coordinates are $x=2\pm4$, $y=-1\pm4$, and $z=3\pm4$, giving six axis-direction endpoints. The two points chosen above use the horizontal pair $x=6,-2$.

At the center, the original polynomial equals $4+1+9-8-2-18-2=-16$, consistent with the translated form $X^2+Y^2+Z^2-16$. It is not zero there, because the center lies inside the sphere rather than on its surface.

## 4. Verification in the original equation

At $P$, the original left-hand side is

$$36+1+9-24-2-18-2=0.$$

At $Q$, it is

$$4+1+9+8-2-18-2=0.$$

Both canonical substitutions give $16+0+0=16$. Expanding the completed squares also recovers the original linear coefficients $-4,2,-6$, checking the signs of all three center coordinates.

**Check a section through the center.** In the plane $z=3$, the canonical equation reduces to $(x-2)^2+(y+1)^2=16$, a circle with radius $4$. The points already selected are its horizontal endpoints. Its vertical endpoints $(2,3,3)$ and $(2,-5,3)$ also satisfy the sphere equation. This checks the middle center coordinate's sign: the midpoint of those two $y$ coordinates is $-1$, matching the center, whereas misreading $y+1$ as a center coordinate $+1$ would produce the wrong section.
