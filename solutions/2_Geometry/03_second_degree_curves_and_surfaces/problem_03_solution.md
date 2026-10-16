# Exercise 3. Ellipse

## The question

For
$$\frac{x^2}{25}+\frac{y^2}{9}=1,$$
find the semiaxis lengths, the intercepts with the coordinate axes, and make a sketch. Explain along which axis the ellipse is more stretched and how this is visible in the equation.

## Before calculating: denominators are squared semiaxes

An axis-aligned ellipse $x^2/a^2+y^2/b^2=1$ has center at the origin and semiaxis lengths $a,b$, not $a^2,b^2$. Its intercepts follow by setting the other coordinate to zero.

The denominators give squared semiaxis lengths because each squared coordinate is divided by the square of its maximum coordinate magnitude. The ellipse is the image of the unit circle under horizontal scaling by $5$ and vertical scaling by $3$. This connects canonical equations with the diagonal scaling matrices from the reference solutions.

## 1. Read the semiaxes and intercepts

$$\boxed{a=5,\qquad b=3}.$$

At $y=0$, $x^2/25=1$, so the horizontal intercepts are $(\pm5,0)$. At $x=0$, $y^2/9=1$, so the vertical intercepts are $(0,\pm3)$.

The ellipse is more stretched along $x$, since $25>9$ gives $5>3$. Its full width is $10$ and height is $6$.

## 2. Sketch using those four endpoints

```text
                 y
              (0,3)
                *
          .-----|-----.
 (-5,0) *-------O-------* (5,0)   x
          '-----|-----'
                *
             (0,-3)
```

The sketch is symmetric about both coordinate axes. No point lies outside $-5\le x\le5$ or $-3\le y\le3$, because each nonnegative term in the equation is at most $1$.

## 3. Explain the ellipse as a scaled circle

Start with a point $(X,Y)$ on $X^2+Y^2=1$ and set $x=5X$, $y=3Y$. Then

$$\frac{x^2}{25}+\frac{y^2}{9}=X^2+Y^2=1.$$

Conversely, every point of the ellipse gives a unit-circle point by $X=x/5$, $Y=y/3$. This proves the scaling description exactly. It also shows the ellipse is a smooth closed curve rather than merely four disconnected intercept points.

The parametric points $(5\cos t,3\sin t)$ trace the full boundary as $t$ runs through $[0,2\pi]$. At $t=0,\pi/2,\pi,3\pi/2$ they give the four marked endpoints, fixing both the shape and scale of the sketch.

## 4. Verification

Each intercept makes one term equal $1$ and the other zero. A non-axis point is $(3,12/5)$:

$$\frac{3^2}{25}+\frac{(12/5)^2}{9}=\frac9{25}+\frac{16}{25}=1.$$

This point lies in the first quadrant within the bounding rectangle, consistent with the sketched arc. Equivalently, the parametrization $(5\cos t,3\sin t)$ satisfies the equation by $\cos^2t+\sin^2t=1$.
