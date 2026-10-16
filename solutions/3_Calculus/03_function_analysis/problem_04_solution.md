# Problem 4. A Function with Two Vertical Asymptotes

## The question

Analyze
$$f(x)=\frac1{x^2-1}.$$
Determine the domain, asymptotes, sign, and monotonicity on the intervals of the domain. Explain why each interval must be analyzed separately.

## Before calculating: poles split the domain into three intervals

The denominator factors as $(x-1)(x+1)$, so $\boxed{D_f=\mathbb R\setminus\{-1,1\}}$. Values or derivative signs cannot be carried through an excluded point as if the graph were continuous there.

The square in the derivative denominator is positive wherever the function is defined, but the original denominator is not. Function signs and derivative signs therefore require different charts. Keeping these separate prevents the common error of using the denominator's original sign when determining monotonicity.

## 1. Sign and asymptotes

The numerator is positive. The denominator is positive for $|x|>1$ and negative for $|x|<1$. Thus $f>0$ outside $[-1,1]$ and $f<0$ inside $(-1,1)$; there are no zeros.

The vertical asymptotes and one-sided limits are

$$x\to-1^-:f\to+\infty,\quad x\to-1^+:f\to-\infty,$$

$$x\to1^-:f\to-\infty,\quad x\to1^+:f\to+\infty.$$

Since $f(x)\to0^+$ as $x\to\pm\infty$, $y=0$ is the horizontal asymptote.

## 2. Differentiate and classify

$$f'(x)=-\frac{2x}{(x^2-1)^2}.$$

The squared denominator is positive, so $f'>0$ for $x<0$ and $f'<0$ for $x>0$, with the poles still excluded. Increasing intervals are $(-\infty,-1)$ and $(-1,0)$; decreasing intervals are $(0,1)$ and $(1,\infty)$. At $x=0$, the derivative changes $+\to-$, giving local maximum $\boxed{(0,-1)}$.

## 3. Separate the central branch from the outer branches

For $|x|<1$, $f=-1/(1-x^2)$, so its largest value on that entire central component is $-1$ at zero; it falls without bound near either endpoint. For $|x|>1$, $f$ is positive, tending to $0$ at infinity and to $+\infty$ near the poles.

Consequently the range is $(-\infty,-1]\cup(0,\infty)$, and $(0,-1)$ cannot be a global maximum over the disconnected full domain because positive values occur on the outer components.

This distinction clarifies the extremum statement: “local maximum” refers to nearby domain points, not every branch. The symmetry $f(-x)=f(x)$ pairs the outer branches and the two pole behaviors, providing a useful geometric consistency check.

## 4. Verification

Test $x=-2,-1/2,1/2,2$: derivative signs are respectively $+,+,-,-$, checking every connected monotonic interval. The function is even, $f(-x)=f(x)$, and $f'$ is odd, agreeing with left-right reflection symmetry. Also for $|x|<1$, $f(x)=-1/(1-x^2)\le-1$, independently confirming the central local maximum. There is no global maximum or minimum because of the unbounded pole behavior.
