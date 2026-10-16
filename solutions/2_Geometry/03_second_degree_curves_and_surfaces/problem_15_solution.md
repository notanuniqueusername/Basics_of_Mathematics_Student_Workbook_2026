# Exercise 15. Recognition and Sketch Without a Given Name

## The question

Consider the two equations:

$$4x^2+9y^2-8x+36y+4=0,$$

$$4x^2+y^2=z^2.$$

For the first equation, reduce it to canonical form, recognize the curve, give its most important features, and make a sketch.

For the second equation, do not begin by using a ready-made name for the surface. First describe the cross-sections $z=c$ and the cross-sections by the planes $x=0$ and $y=0$, paying attention to the different scales along the axes. Only then identify the surface and make a sketch.

## Before calculating: use a different mechanism for each equation

For the planar curve, complete squares to reveal its center and scales. For the spatial equation, inspect cross-sections before naming the shape, as requested.

The first equation requires translating coordinates before reading lengths; the second already has its vertex at the origin but different coefficients in the two horizontal directions. Completing squares and slicing are complementary tools: one reveals a shifted planar curve, while the other reconstructs a three-dimensional shape from simpler sections.

## 1. Reduce and sketch the curve

$$4[(x-1)^2-1]+9[(y+2)^2-4]+4=0,$$

so $4(x-1)^2+9(y+2)^2=36$ and

$$\boxed{\frac{(x-1)^2}{9}+\frac{(y+2)^2}{4}=1}.$$

It is an ellipse centered at $(1,-2)$ with horizontal and vertical semiaxes $3$ and $2$. Its axis endpoints are $(-2,-2),(4,-2),(1,0),(1,-4)$.

```text
            (1,0)
               *
           .---|---.
 (-2,-2) *-----C-----* (4,-2)
           '---|---'
               *
            (1,-4)     C=(1,-2)
```

## 2. Determine the spatial shape through sections

For $4x^2+y^2=z^2$, fix $z=c\ne0$:

$$\frac{x^2}{c^2/4}+\frac{y^2}{c^2}=1.$$

The section is an ellipse with semiaxes $|c|/2$ along $x$ and $|c|$ along $y$. At $c=0$ it reduces to the origin.

At $x=0$, the section is $y=\pm z$. At $y=0$, it is $z=\pm2x$. These are straight lines with different scales in the two vertical planes. Only now identify the surface: it is an elliptic double cone, narrower in the $x$ direction than the $y$ direction.

```text
Cone cross-section guides; both meet at the origin
 y=0: z=±2x       x=0: z=±y
       z                 z
      \|/              \ | /
 ------O------ x    -----O----- y
      /|\              / | \
```

## 3. Check the scales before drawing either object

For the ellipse, the original polynomial becomes

$$4(x-1)^2+9(y+2)^2-36.$$

The horizontal endpoints therefore have displacement $\pm3$ from $x=1$, while the vertical endpoints have displacement $\pm2$ from $y=-2$. The different shifts and semiaxes must both be reflected in the sketch; an ellipse centered at the origin would be incorrect.

For the cone, at height $c=2$ the section is $x^2+y^2/4=1$, with horizontal semiaxis $1$ and vertical-in-the-slice semiaxis $2$. At $c=4$ these lengths double to $2$ and $4$. This proportional growth gives straight generators from the vertex. At negative heights the same section sizes occur, proving the existence of a lower half and explaining why the final name is a double cone.

## 4. Verification

The ellipse endpoint $(4,-2)$ gives $64+36-32-72+4=0$ in the original equation. For the cone at $z=2$, the endpoints $(\pm1,0,2)$ and $(0,\pm2,2)$ satisfy $4x^2+y^2=4$. This checks the unequal semiaxes and excludes a circular cone interpretation.
