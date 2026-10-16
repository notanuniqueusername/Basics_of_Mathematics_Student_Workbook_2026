# Exercise 13. Intersection of a Sphere and a Plane

## The question

Given the sphere
$$x^2+y^2+z^2=25$$
and the plane $z=3$, find the equation of the intersection curve and its radius. Then describe what happens for $z=c$ depending on $c$.

## Before calculating: intersect by fixing the plane coordinate

The sphere has center $(0,0,0)$ and radius $5$. A horizontal slice at height $c$ has squared radius $25-c^2$, from the Pythagorean relation between sphere radius, height, and slice radius.

The sphere's radius, the distance from its center to the slicing plane, and the slice radius form a right triangle. This provides a geometric origin for $R^2+c^2=25$. The absolute height $|c|$ matters, not its sign, because equally distant planes above and below the center give congruent circles.

## 1. Find the requested intersection

Substitute $z=3$:

$$x^2+y^2+9=25\quad\Longrightarrow\quad x^2+y^2=16.$$

The spatial intersection is

$$\boxed{\{(x,y,3):x^2+y^2=16\}},$$

a circle centered at $(0,0,3)$ of radius $\boxed{4}$. The condition $z=3$ must remain part of its description; $x^2+y^2=16$ alone would describe a cylinder in space.

## 2. Classify all parallel slices

At $z=c$, $x^2+y^2=25-c^2$.

| Height | Intersection |
|---|---|
| $|c|<5$ | Circle, center $(0,0,c)$, radius $\sqrt{25-c^2}$ |
| $|c|=5$ | Single point $(0,0,c)$; tangent plane |
| $|c|>5$ | Empty |

## 3. Describe the circle as a spatial curve

For the requested plane, a full parametrization is

$$\gamma(t)=(4\cos t,4\sin t,3),\qquad0\le t<2\pi.$$

Its third coordinate fixes the plane, and its displacement from the circle center $(0,0,3)$ has length $4$. Substituting into the sphere gives $16\cos^2t+16\sin^2t+9=25$ for every $t$, verifying the entire curve rather than only two sample points.

The circle center is not the sphere center: it is the perpendicular foot of the sphere center onto the plane. Its height $3$ explains why the circle radius is $4$ instead of the sphere radius $5$. At $|c|=5$, the same radius formula collapses the parametrization to a single tangent point.

## 4. Verification

The point $(4,0,3)$ satisfies the plane and sphere: $z=3$ and $16+0+9=25$. Likewise $(0,-4,3)$ satisfies $0+16+9=25$. At the limiting height $c=5$, only $(0,0,5)$ remains. This agrees with the slice-radius formula and with tangency at the sphere's top.
