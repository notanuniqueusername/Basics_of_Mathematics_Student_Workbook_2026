# Exercise 9. Ellipsoid and Its Cross-Sections

## The question

Consider
$$\frac{x^2}{9}+\frac{y^2}{4}+\frac{z^2}{16}=1.$$
Give the semiaxis lengths, describe the cross-section $z=0$, and explain how the cross-sections $z=c$ change for $|c|<4$.

## Before calculating: slices reduce dimension

An ellipsoid $x^2/a^2+y^2/b^2+z^2/c^2=1$ has semiaxis lengths $a,b,c$. Fixing $z$ leaves a planar equation; the sign of its right-hand side decides whether the slice is an ellipse, a point, or empty.

A section at $z=c$ is a curve lying in a specific horizontal plane, not just an equation in $x,y$ without location. The ellipse's center is therefore written $(0,0,c)$. The three-dimensional semiaxes describe the full ellipsoid, whereas the two section semiaxes depend on height and need not equal the central ones.

## 1. Read the semiaxes and central slice

$$\boxed{a_x=3,\quad a_y=2,\quad a_z=4}.$$

At $z=0$, the section is the ellipse

$$\boxed{\frac{x^2}{9}+\frac{y^2}{4}=1},$$

with semiaxes $3$ and $2$ in that horizontal plane.

## 2. Describe the general horizontal section

At $z=c$,

$$\frac{x^2}{9}+\frac{y^2}{4}=1-\frac{c^2}{16}=k.$$

For $|c|<4$, $k>0$. Dividing by $k$ gives

$$\frac{x^2}{9k}+\frac{y^2}{4k}=1.$$

Thus the section is centered at $(0,0,c)$ with semiaxes $3\sqrt{k}$ and $2\sqrt{k}$. Both shrink as $|c|$ grows, maintaining ratio $3:2$. At $|c|=4$ the section is a single point, and for $|c|>4$ there are no real points.

## 3. Explain the square-root shrinkage and endpoint cases

Let $k=1-c^2/16$. A slice endpoint on its horizontal axis satisfies $x^2/9=k$, hence $|x|=3\sqrt k$; similarly $|y|=2\sqrt k$. This derivation explains why the length factor is $\sqrt k$, not $k$ itself.

At $c=\pm4$, $k=0$ and both coordinates must vanish, so the ellipse collapses to the top or bottom point of the ellipsoid. Beyond those heights, the right side is negative but the left side is a sum of nonnegative terms, making the slice impossible. Heights $c$ and $-c$ give congruent sections because only $c^2$ appears. The largest section is at $c=0$, where the shrinkage factor is $1$.

## 4. Verification

At $c=0$, the formula returns the original semiaxes. At $c=2\sqrt3$, $k=1/4$, giving semiaxes $3/2$ and $1$. The slice endpoint $(3/2,0,2\sqrt3)$ satisfies $1/4+0+3/4=1$. This verifies the square-root scaling; using $k$ itself as the length factor would be incorrect.
