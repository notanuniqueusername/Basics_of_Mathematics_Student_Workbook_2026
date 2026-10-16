# Problem 3. A Rational Function

## The question

Analyze the domain, zeros, asymptotes, and monotonicity of
$$f(x)=\frac{x+1}{x-2}.$$
Finally, sketch a graph consistent with all the information obtained.

## Before calculating: separate the domain at a pole

The denominator excludes $x=2$. Polynomial division isolates the asymptotes and simplifies both limits and differentiation:

$$f(x)=1+\frac3{x-2}.$$

The domain's connected components must be analyzed separately because the function is discontinuous at the pole. A negative derivative on both components does not compare points across the excluded value. Asymptotic limits locate the branches, while the derivative determines how each branch moves within its own interval.

## 1. Domain, zero, and asymptotes

$$\boxed{D_f=\mathbb R\setminus\{2\},\qquad x\text{-intercept }(-1,0)}.$$

The vertical asymptote is $x=2$: $f\to-\infty$ as $x\to2^-$ and $f\to+\infty$ as $x\to2^+$. At either infinity, $3/(x-2)\to0$, giving horizontal asymptote $y=1$. The vertical intercept is $(0,-1/2)$.

## 2. Monotonicity and sketch

$$f'(x)=-\frac3{(x-2)^2}<0\qquad(x\ne2).$$

Thus $f$ decreases separately on $(-\infty,2)$ and $(2,\infty)$, with no extrema. It is not decreasing on the whole disconnected domain across the pole.

```text
 y        x=2
          :\
 1 ·······:·\________····  y=1
     ____ :
 0 --*----\:---------------- x
   (-1,0) \:
          :
```

The left branch stays below $1$ and the right above $1$.

## 3. Locate signs and branch positions precisely

The zero at $x=-1$ splits the left branch's sign. For $x<-1$, both numerator and denominator are negative, so $f>0$; for $-1<x<2$, only the denominator is negative, so $f<0$. For $x>2$, both are positive.

The decomposition also gives $f-1=3/(x-2)$, so the left branch is always below its horizontal asymptote and the right always above it. In particular, the function never attains the value $1$; its range is $\mathbb R\setminus\{1\}$.

This exact information resolves the sketch beyond simply labeling two asymptotes. It explains how a decreasing left branch can cross zero before tending to $-\infty$, while the decreasing right branch remains positive and approaches $1$ from above.

## 4. Verification

The quotient rule gives $f'=((x-2)-(x+1))/(x-2)^2=-3/(x-2)^2$, agreeing with the decomposed form. At $x=1,3$, the values are $-2,4$, confirming the opposite sides of the asymptote. The relation $(x-2)(f(x)-1)=3$ checks every graph point and shows symmetry about $(2,1)$.
