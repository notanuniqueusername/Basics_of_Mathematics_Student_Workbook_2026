# Problem 13. A Logarithm and an Asymptote

## The question

Perform a complete analysis of
$$f(x)=\frac{\ln x}{x},\qquad x>0.$$
Find the maximum and the behavior at the ends of the domain. Explain which information is necessary for a correct sketch.

## Before calculating: keep the logarithmic domain

The domain is $(0,\infty)$. The numerator changes sign at $1$, while the denominator remains positive. There is no even/odd symmetry because the domain is not symmetric about zero.

The complete description includes the logarithmic domain boundary, signs, a zero, stationary behavior, curvature, and end limits. Knowing only the maximum would not distinguish a graph that tends to zero from one that eventually turns upward without bound. Those global features require limit calculations in addition to the derivative test.

## 1. Zeros, signs, and limits

The only zero is $(1,0)$. The function is negative on $(0,1)$ and positive on $(1,\infty)$.

At $0^+$, write $x=1/t$: $(\ln x)/x=-t\ln t\to-\infty$. Thus $x=0$ is a vertical asymptote. At $+\infty$, write $x=e^u$: $\ln x/x=u/e^u\to0^+$, giving horizontal asymptote $y=0$.

## 2. First and second derivatives

Apply the quotient rule with numerator $u(x)=\ln x$, $u'(x)=1/x$, and denominator $v(x)=x$, $v'(x)=1$:

$$f'(x)=\frac{u'v-uv'}{v^2}=\frac{(1/x)\,x-(\ln x)\cdot1}{x^2}=\frac{1-\ln x}{x^2}.$$

It is positive for $x<e$, zero at e, and negative for $x>e$. Hence the unique global maximum is $\boxed{(e,1/e)}$.

For the second derivative, write $f'(x)=(1-\ln x)x^{-2}$ and use the product rule. The two factor derivatives are $-1/x$ and $-2x^{-3}$:

$$f''(x)=\left(-\frac1x\right)x^{-2}+(1-\ln x)(-2x^{-3})=-x^{-3}-2(1-\ln x)x^{-3}.$$

Collecting the coefficients of $x^{-3}$ gives

$$f''(x)=\bigl(-1-2+2\ln x\bigr)x^{-3}=\frac{2\ln x-3}{x^3}.$$

The graph is concave on $(0,e^{3/2})$ and convex on $(e^{3/2},\infty)$, with inflection point

$$\boxed{\left(e^{3/2},\frac{3}{2e^{3/2}}\right)}.$$

## 3. Justify the end limits and distinguish the inflection from the maximum

For $x\to\infty$, set $x=e^u$. Then $u\to\infty$ and $f=u/e^u$. The bound $e^u\ge u^2/2$ gives $0\le u/e^u\le2/u\to0$.

For $x\to0^+$, $t=1/x\to\infty$ and $f=-t\ln t\to-\infty$. These substitutions prove the two distinct end behaviors explicitly.

The maximum occurs at $e$, while the inflection occurs later at $e^{3/2}>e$. Thus the descending right branch initially remains concave and only later becomes convex as it flattens toward zero. A sketch placing the inflection at the maximum would mix the first- and second-derivative conditions and contradict the exact formulas.

## 4. Sketch and verification

```text
 y
       |       * maximum at e
       |      / \____i_______
0 -----|-----*----------------···· x
       |    (1,0)             y=0 asymptote
       |   /
       |  /
       | /  down to -∞ at 0+
```

The domain boundary, zero, maximum, inflection, and both end limits are necessary landmarks for the complete sketch. Testing $f'(1)=1>0$ and $f'(e^2)=-e^{-4}<0$ confirms the turning point. At e, $f''(e)=-1/e^3<0$, agreeing with a maximum. The substitution-based end limits avoid treating an infinity quotient as ordinary arithmetic.
