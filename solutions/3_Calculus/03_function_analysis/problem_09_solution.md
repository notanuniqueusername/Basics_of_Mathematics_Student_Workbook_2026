# Problem 9. An Oblique Asymptote

## The question

Analyze the asymptotes of
$$f(x)=\frac{x^2+1}{x-1}.$$
Perform polynomial division and explain why the remainder term vanishes for large $|x|$.

## Before calculating: divide polynomials before taking limits

For an oblique asymptote $y=mx+b$, the required condition is $f(x)-(mx+b)\to0$ at the relevant infinity. A vertical asymptote instead concerns divergence at a finite domain exclusion.

An oblique asymptote is a statement about the difference from a line, not about the quotient of function values tending to one. A function can have the same dominant growth as a line while maintaining a nonvanishing offset. Polynomial division finds both the slope and the intercept needed to make the actual difference vanish.

## 1. Perform polynomial division

$$x^2+1=(x-1)(x+1)+2,$$

so for $x\ne1$,

$$\boxed{f(x)=x+1+\frac2{x-1}}.$$

The remainder term tends to zero as $x\to\pm\infty$. Therefore

$$\boxed{y=x+1\text{ is the oblique asymptote at both ends}}.$$

There is no horizontal asymptote, since $f$ grows like the nonconstant line $x+1$.

## 2. Analyze the vertical asymptote

At $x=1$, the numerator is $2\ne0$ and the denominator vanishes. The decomposition gives

$$\lim_{x\to1^-}f(x)=-\infty,\qquad\lim_{x\to1^+}f(x)=+\infty.$$

Thus $\boxed{x=1}$ is the vertical asymptote.

## 3. Determine the slope and intercept directly from limits

The asymptote slope must be

$$m=\lim_{x\to\pm\infty}\frac{f(x)}x=\lim\frac{x^2+1}{x^2-x}=1.$$

Then the intercept is

$$b=\lim_{x\to\pm\infty}(f(x)-x)=\lim\frac{x+1}{x-1}=1.$$

These two calculations independently recover $y=x+1$ and agree with the quotient-and-remainder form. Taking only $m=1$ and writing $y=x$ would miss the constant offset: $f(x)-x\to1$, not zero.

The nonzero remainder also shows the graph never actually crosses its oblique asymptote, since $2/(x-1)$ is never zero at a valid input. This concerns intersection with the line, a separate property from asymptotic approach.

## 4. Verification

Multiplying the divided form by $x-1$ gives $(x+1)(x-1)+2=x^2+1$, checking the quotient and remainder. The exact gap from the sloping line is $2/(x-1)$: it is negative to the left of the pole and positive to the right, and for $|x-1|>2/\varepsilon$ its magnitude is less than $\varepsilon$. This proves the asymptotic closeness, not merely agreement of dominant terms.
