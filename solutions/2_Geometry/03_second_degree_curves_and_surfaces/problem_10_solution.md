# Exercise 10. Paraboloids

## The question

Compare
$$z=x^2+y^2$$
and
$$z=x^2-y^2.$$
For each surface, describe the cross-sections $x=0$, $y=0$, and $z=c$, then make a qualitative sketch.

## Before calculating: compare the signs in vertical sections

Fixing one coordinate gives a planar cross-section. For surfaces written as $z=f(x,y)$, the signs of the squared terms distinguish a bowl, with the same bending in both coordinate directions, from a saddle, with opposite bending.

A surface is not fully determined visually by one convenient slice. Two perpendicular vertical slices reveal whether curvature agrees or opposes, while horizontal slices show how the level sets fit together. A saddle has no local minimum at its central point because some nearby directions increase height while others decrease it.

## 1. Compare all requested sections

| Section | $z=x^2+y^2$ | $z=x^2-y^2$ |
|---|---|---|
| $x=0$ | $z=y^2$, upward parabola | $z=-y^2$, downward parabola |
| $y=0$ | $z=x^2$, upward parabola | $z=x^2$, upward parabola |
| $z=c>0$ | Circle, radius $\sqrt c$ | Hyperbola $x^2-y^2=c$, opening along $x$ |
| $z=0$ | One point, the origin | Two lines $y=\pm x$ |
| $z=c<0$ | Empty | Hyperbola $y^2-x^2=-c$, opening along $y$ |

## 2. Sketch and identify the shapes

```text
Bowl (elliptic paraboloid)      Saddle (hyperbolic paraboloid)
         z                               z
         |   /                           |  /   z=x^2 at y=0
      \  |  /                         ---O---->
       \ | /                           / | \
        \O/                         z=-y^2 at x=0
    horizontal slices: circles      horizontal slices: hyperbolas
```

These are cross-section guides to the three-dimensional shapes, not perspective drawings to scale. The bowl has minimum height $0$; the saddle takes both positive and negative heights arbitrarily close to the origin.

## 3. Use directional sections to explain the saddle

For the bowl, points $(t,0,t^2)$ and $(0,t,t^2)$ both rise above the origin for nonzero $t$. In any vertical plane through the axis, setting $x=r\cos\phi$, $y=r\sin\phi$ yields $z=r^2$, so the upward shape is the same in every horizontal direction.

For the saddle, the same directional substitution gives

$$z=r^2(\cos^2\phi-\sin^2\phi)=r^2\cos2\phi.$$

The coefficient can be positive, negative, or zero. At $\phi=0$ the section curves up; at $\phi=\pi/2$ it curves down; at $\phi=\pi/4$ the section is a straight line at height zero. This explains the two diagonal zero-level lines and the saddle's mixed curvature directly from the equation.

## 4. Verification

At $(x,y)=(1,0)$ both surfaces have $z=1$. At $(0,1)$, the bowl has $z=1$ while the saddle has $z=-1$. At $(1,1)$, their heights are $2$ and $0$. These points check the opposite vertical curvatures and the diagonal zero-height lines of the saddle.
