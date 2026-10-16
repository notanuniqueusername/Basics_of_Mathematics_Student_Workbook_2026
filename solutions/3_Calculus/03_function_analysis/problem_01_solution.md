# Problem 1. A Cubic Polynomial

## The question

Analyze the monotonicity and extrema of
$$f(x)=x^3-3x^2+2.$$
Sketch the graph based on the results and mark the critical points.

## Before calculating: derivative sign determines monotonicity

The polynomial has domain $\mathbb R$. Critical points occur where its derivative vanishes; the derivative's sign on the intervening intervals determines their character. Zeros of the derivative alone do not tell us whether a point is a maximum or minimum.

The sign of $f'$ controls direction of change on intervals, while a change of sign classifies a turning point. The second derivative, when used for the sketch, answers a separate question about curvature. End behavior and actual function values are needed to place the graph vertically; derivative zeros by themselves provide only horizontal locations.

## 1. Differentiate and build the sign chart

$$f'(x)=3x^2-6x=3x(x-2).$$

The critical arguments are $0$ and $2$.

| $x$ | $(-\infty,0)$ | $0$ | $(0,2)$ | $2$ | $(2,\infty)$ |
|---|---|---|---|---|---|
| $f'$ | $+$ | $0$ | $-$ | $0$ | $+$ |
| $f$ | Increasing | Local maximum | Decreasing | Local minimum | Increasing |

Thus the extrema are $\boxed{(0,2)\text{ maximum},\ (2,-2)\text{ minimum}}$. Neither is global because the cubic is unbounded in both directions.

## 2. Add graph landmarks and sketch

Factor $f(x)=(x-1)(x^2-2x-2)$, giving roots $1-\sqrt3,1,1+\sqrt3$. Also $f''=6x-6$, so the inflection point is $(1,0)$. The end limits are $-\infty$ on the left and $+\infty$ on the right.

```text
 y
 2          * maximum (0,2)
           / \
 0 -------/---\---*-----------/---- x
         /     \ (1,0)      /
-2               \___*___/  minimum (2,-2)
```

The schematic marks the turns; the exact three intercepts are listed above.

## 3. Explain the intercept factorization and central symmetry

Since $f(1)=0$, division by $x-1$ gives $x^2-2x-2$. Solving that quadratic gives $x=1\pm\sqrt3$, accounting for all three real intercepts. In increasing order they are approximately $-0.732$, $1$, and $2.732$.

The substitution $x=1+h$ gives $f(1+h)=h^3-3h$. Replacing $h$ by $-h$ negates the value, so the graph has half-turn symmetry about $(1,0)$. The maximum $(0,2)$ and minimum $(2,-2)$ are paired by exactly that symmetry. These relationships constrain the sketch: the curve must cross the axis once before the maximum, once between the turns, and once after the minimum, consistently with its end limits and monotonicity.

## 4. Verification

Test $x=-1,1,3$: derivative values are $9,-3,9$, confirming the three signs. Directly $f(0)=2$ and $f(2)=8-12+2=-2$. Writing $x=1+h$ gives $f(1+h)=h^3-3h$, an odd function of $h$, confirming central symmetry about the inflection point $(1,0)$.
