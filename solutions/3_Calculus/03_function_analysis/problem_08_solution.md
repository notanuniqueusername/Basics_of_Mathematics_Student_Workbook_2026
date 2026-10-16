# Problem 8. The Second Derivative

## The question

For
$$f(x)=x^4-4x^2$$
find the local extrema, intervals of convexity and concavity, and inflection points. Sketch the graph and mark all the identified features on it.

## Before calculating: distinguish extrema from inflection points

The first derivative controls rising and falling; the second controls curvature. Here “convex” means $f''>0$ (curving upward) and “concave” means $f''<0$ (curving downward). An inflection requires a curvature sign change, not just a zero second derivative.

A local maximum can occur at a height also attained elsewhere, and a global minimum can occur at more than one argument. Curvature and extremum tests are distinct: $f''=0$ identifies possible inflections, while an actual sign change is needed. We use convex for upward curvature and concave for downward curvature throughout the analysis.

## 1. Find the extrema

$$f'(x)=4x^3-8x=4x(x^2-2).$$

Its zeros are $-\sqrt2,0,\sqrt2$. The derivative signs are $-,+,-,+$ on the four successive intervals. Hence

$$\boxed{(\pm\sqrt2,-4)\text{ are global minima},\qquad(0,0)\text{ is a local maximum}}.$$

Global minimality also follows from $f(x)=(x^2-2)^2-4\ge-4$.

## 2. Determine curvature

$$f''(x)=12x^2-8=4(3x^2-2).$$

Let $a=\sqrt{2/3}$. The function is convex on $(-\infty,-a)$ and $(a,\infty)$, concave on $(-a,a)$, and has inflection points

$$\boxed{\left(\pm\sqrt{\frac23},-\frac{20}{9}\right)}.$$

Indeed at $x^2=2/3$, $f=4/9-8/3=-20/9$.

## 3. Use exact landmark ordering to organize the sketch

The positive landmark arguments satisfy $0<\sqrt{2/3}<\sqrt2<2$, and the negative side is their mirror image. Thus each outer inflection lies between the central peak and its neighboring minimum, while each outer root lies beyond that minimum.

The factorization $f=x^2(x-2)(x+2)$ shows that the graph touches the axis at zero but crosses it at $\pm2$. The completed square $f=(x^2-2)^2-4$ proves the two minima share the same global height. Together these facts specify the W-shape more precisely than a generic sketch: the middle turn is on the axis, the two valleys are below it, and both unbounded tails rise. The inflection ordinates $-20/9$ lie strictly between $-4$ and $0$, consistently with their positions along the descending and ascending portions.

## 4. Sketch and verify

The function is even, has zeros $-2,0,2$, and tends to $+\infty$ at both ends.

```text
 y
 | \          local max          /
0+--*------___*(0,0)___---------*--- x
 |   \   i/           \i     /
-4     *                 *
    (-√2,-4)          (√2,-4)
 i: inflections at x=±√(2/3), y=-20/9
```

The schematic marks the two valleys and central peak; the exact inflection coordinates are given above. Check $f''(0)=-8<0$ and $f''(\pm\sqrt2)=16>0$, confirming the extremum types. Testing curvature at $x=0$ and $x=\pm1$ gives negative and positive signs, verifying both inflection changes.
