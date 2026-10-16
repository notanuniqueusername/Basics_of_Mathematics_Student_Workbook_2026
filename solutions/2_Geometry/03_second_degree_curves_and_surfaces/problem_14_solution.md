# Exercise 14. Cone and Cylinder

## The question

Compare
$$x^2+y^2=z^2$$
and
$$x^2+y^2=4.$$
For each surface, describe the cross-sections $z=c$, $x=0$, and $y=0$, make a sketch, and explain why the radius of the cross-section depends on $z$ in the first case but is constant in the second.

## Before calculating: a missing variable means translation freedom

Horizontal sections reveal how radius changes with height. For $x^2+y^2=z^2$, the radius is $|z|$; for $x^2+y^2=4$, the equation is independent of $z$, so the same circle occurs at every height.

A cylinder is invariant under translation along its axis, because its equation omits that axis coordinate. A cone instead changes size with height and has a distinguished vertex. Vertical sections through the axis expose this difference as parallel lines for the cylinder and intersecting lines for the cone.

## 1. Compare all requested sections

| Section | $x^2+y^2=z^2$ | $x^2+y^2=4$ |
|---|---|---|
| $z=c$ | Circle radius $|c|$, or origin at $c=0$ | Circle radius $2$ for every $c$ |
| $x=0$ | Lines $y=z$ and $y=-z$ | Lines $y=2$ and $y=-2$, arbitrary $z$ |
| $y=0$ | Lines $x=z$ and $x=-z$ | Lines $x=2$ and $x=-2$, arbitrary $z$ |

## 2. Identify and sketch

The first is a circular double cone with vertex at the origin. Both positive and negative heights occur. The second is a circular cylinder of radius $2$ about the $z$-axis.

```text
Meridian y=0; rotate about z
 Double cone           Cylinder
      z                    z
   \  |  /              |  |  |
    \ | /               |  |  |
 -----O----- x        --|--O--|-- x
    / | \               |  |  |
   /  |  \              |  |  |
```

## 3. Explain the radius formulas and the two cone halves

At $z=c$, the cone gives $x^2+y^2=c^2$, whose radius is $\sqrt{c^2}=|c|$. Using radius $c$ would be invalid at negative heights, even though the lower half is a genuine part of the surface. Its two halves meet only where $c=0$ and the radius is zero.

For the cylinder, the equation remains $x^2+y^2=4$ no matter how $c$ changes. A point $(x,y,z)$ on it can be translated to $(x,y,z+h)$ for any real $h$ without changing membership. The cone lacks that invariance: translating $(1,0,1)$ upward to $(1,0,2)$ changes $1=1$ into $1=4$, so it leaves the surface. These checks tie the names to exact geometric mechanisms.

## 4. Verification

For the cone, $(3,0,3)$ and $(3,0,-3)$ both satisfy $9=9$, confirming both halves. For the cylinder, $(2,0,c)$ satisfies the equation for every real $c$, showing the fixed radius directly. The cone narrows to a point at height zero, whereas the cylinder retains its full circular section there. The absolute value in the cone radius is essential because a radius cannot be negative.
