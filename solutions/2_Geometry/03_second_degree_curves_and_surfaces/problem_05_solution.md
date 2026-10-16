# Exercise 5. Hyperbola and Asymptotes

## The question

For
$$\frac{x^2}{16}-\frac{y^2}{9}=1,$$
find the intercepts with the $x$-axis, the asymptotes, and make a sketch. Explain why the asymptotes describe the behavior of the curve far from the center.

## Before calculating: the positive term fixes the opening direction

For $x^2/a^2-y^2/b^2=1$, the branches open along $x$, the vertices are $(\pm a,0)$, and the asymptotes are $y=\pm(b/a)x$. The asymptotes describe large-distance behavior, not points of the curve.

An asymptote need not intersect the curve. Its role is that the separation from the curve tends to zero along an unbounded branch. The hyperbola's asymptote slopes depend on the ratio of semiaxis lengths, $b/a$, rather than on the squared ratio of the denominators. The vertices are the closest branch points to the center.

## 1. Find intercepts and asymptotes

Here $a=4$, $b=3$. Setting $y=0$ gives $x=\pm4$; setting $x=0$ would require $-y^2/9=1$, impossible. Thus

$$\boxed{\text{vertices }(\pm4,0),\qquad y=\pm\frac34x\text{ are the asymptotes}}.$$

## 2. Explain the far-field behavior

Solve for $y$:

$$y=\pm\frac34\sqrt{x^2-16},\qquad |x|\ge4.$$

Since $\sqrt{x^2-16}/|x|=\sqrt{1-16/x^2}\to1$, the branch slopes approach the asymptote slopes. In fact $|x|-\sqrt{x^2-16}=16/(|x|+\sqrt{x^2-16})\to0$, so the vertical gaps also tend to zero.

## 3. Construct the asymptote guide rectangle

Use the rectangle with corners $(\pm4,\pm3)$. Its diagonals through the origin have slopes $\pm3/4$, giving the two asymptotes. Place the vertices at the midpoints $(\pm4,0)$ of the vertical sides, then draw each branch moving outward toward the diagonal directions.

The asymptotes are not part of the hyperbola: substituting $y=\pm3x/4$ makes $x^2/16-y^2/9=0$, not $1$. For $|x|>4$, the formula $|y|=(3/4)\sqrt{x^2-16}$ is smaller than $(3/4)|x|$, locating each branch inside its pair of asymptote rays. This specifies which side of the guide lines the curve occupies and makes the sketch more informative than a pair of generic branches.

## 4. Sketch and verify

```text
                 y
       \   )     |     (   /
        \ )      |      ( /
 --------*-------O-------*-------- x
       (-4,0)         (4,0)
        / )      |      ( \
       /   )     |     (   \
```

The diagonal straight directions are the asymptotes. The vertices give $16/16=1$ in the equation. A non-axis point $(4\sqrt2,3)$ gives $32/16-9/9=2-1=1$, checking the right branch and its positive opening direction.
