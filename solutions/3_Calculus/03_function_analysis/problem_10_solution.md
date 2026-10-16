# Problem 10. Complete Function Analysis

## The question

Perform a complete analysis of
$$f(x)=\frac{x}{x^2+1}.$$
Include the domain, symmetry, zeros, limits, monotonicity, extrema, and convexity. Finally, produce a sketch based only on this information.

## Before calculating: organize the complete analysis

The denominator $x^2+1$ is positive everywhere, so the domain is $\mathbb R$. The function is odd because $f(-x)=-f(x)$; the only zero and vertical intercept is $(0,0)$.

For a complete analysis, each conclusion must be tied to the appropriate calculation: the denominator gives the domain, parity gives symmetry, limits give asymptotes, $f'$ gives monotonicity, and $f''$ gives curvature. The different zeros of these derivatives generally mark different features and should not be merged into one undifferentiated list.

## 1. Limits, monotonicity, and extrema

At both infinities $f(x)\to0$, from below on the left and above on the right. Thus $y=0$ is a horizontal asymptote; there are no vertical poles.

$$f'(x)=\frac{(x^2+1)-2x^2}{(x^2+1)^2}=\frac{1-x^2}{(x^2+1)^2}.$$

It is negative on $(-\infty,-1)$ and $(1,\infty)$, positive on $(-1,1)$. Thus

$$\boxed{(-1,-1/2)\text{ is the global minimum},\qquad(1,1/2)\text{ is the global maximum}}.$$

## 2. Curvature and inflection points

Differentiating $f'=(1-x^2)(1+x^2)^{-2}$ gives

$$f''(x)=-2x(1+x^2)^{-2}-4x(1-x^2)(1+x^2)^{-3}=\frac{2x(x^2-3)}{(1+x^2)^3}.$$

Its signs on the intervals split by $-\sqrt3,0,\sqrt3$ are $-,+,-,+$. Therefore the graph is convex on $(-\sqrt3,0)$ and $(\sqrt3,\infty)$, concave on $(-\infty,-\sqrt3)$ and $(0,\sqrt3)$.

The three inflection points are

$$\boxed{(-\sqrt3,-\sqrt3/4),\quad(0,0),\quad(\sqrt3,\sqrt3/4)}.$$

## 3. Assemble the left-to-right landmark order

The special arguments occur in the order

$$-\sqrt3<-1<0<1<\sqrt3.$$

From the far left the graph approaches zero from below, curves downward, then changes to upward curvature at $-\sqrt3$ while still decreasing. It reaches its minimum at $-1$, increases through the origin, and changes curvature there. It continues increasing to the maximum at $1$, then decreases, changing to upward curvature again at $\sqrt3$ before approaching zero from above.

This narrative checks that the derivative and curvature charts can coexist in one graph: an inflection need not be a turning point, and a turning point need not be an inflection. Odd symmetry reproduces the entire right-hand description from the left and pairs the equal-magnitude extremum heights.

## 4. Sketch

```text
 y
 1/2                       * maximum
                          / \
 0 ·····\_______________/O---\________···· x
         \             /
 -1/2     \____*______/
             minimum
 landmarks: min x=-1, max x=1; inflections x=-√3,0,√3
```

The curve crosses its horizontal asymptote at the origin, which is allowed. Exact landmarks and derivative signs determine the sketch rather than the schematic's scale.

## 5. Verification

The bound $x^2+1\ge2|x|$ gives $|f(x)|\le1/2$, with equality only when $|x|=1$, confirming both global extrema. Odd symmetry pairs the extrema and outer inflections, while the origin is fixed. Testing $f''$ at $-2,-1,1,2$ gives the signs $-,+,-,+$, confirming every curvature interval.
