# Problem 2. Powers, Roots, and the Domain

## The question

Compute
$$\int\left(2\sqrt{x}+\frac{3}{x^2}-x^{1/3}\right)\,dx.$$
First rewrite the terms as powers, determine the domain of the original expression, and verify the result by differentiation.

## Before calculating: rewrite and keep the original domain

The square root requires $x\ge0$, and $3/x^2$ excludes zero. The real cube root is defined for every real number, but the intersection of all restrictions is $\boxed{x>0}$.

The power rule for antiderivatives excludes exponent $-1$ because division by $p+1$ would then divide by zero. None of the exponents here is exceptional. On positive inputs the fractional powers are unambiguous real expressions; this domain was already forced by the original square root and reciprocal and must be retained after integration.

## 1. Rewrite as powers

$$2\sqrt x+\frac3{x^2}-x^{1/3}=2x^{1/2}+3x^{-2}-x^{1/3}.$$

None of the exponents is $-1$, so the power antiderivative rule applies to each term on $(0,\infty)$.

## 2. Integrate each term

$$\int2x^{1/2}\,dx=2\frac{x^{3/2}}{3/2}=\frac43x^{3/2},$$

$$\int3x^{-2}\,dx=3\frac{x^{-1}}{-1}=-3x^{-1},$$

$$\int-x^{1/3}\,dx=-\frac{x^{4/3}}{4/3}=-\frac34x^{4/3}.$$

Therefore

$$\boxed{\int\left(2\sqrt x+\frac3{x^2}-x^{1/3}\right)dx=\frac43x^{3/2}-\frac3x-\frac34x^{4/3}+C,\quad x>0}.$$

## 3. Track exponent changes and signs without skipping a term

For the root term, increasing $1/2$ by one gives $3/2$, and dividing $2$ by $3/2$ produces $4/3$. For the reciprocal term, increasing $-2$ by one gives $-1$, so division by that new exponent changes the coefficient $3$ to $-3$. For the cube-root term, increasing $1/3$ gives $4/3$, and division changes its coefficient $-1$ to $-3/4$.

At $x=1$, the integrand is $2+3-1=4$. Differentiating the proposed answer gives three contributions $2,3,-1$ there, matching term by term. A negative antiderivative term is perfectly consistent with a positive derivative contribution, as the reciprocal term illustrates. The sign is determined by the derivative, not by the function's height.

## 4. Verification

$$\frac{d}{dx}\left(\frac43x^{3/2}-3x^{-1}-\frac34x^{4/3}+C\right)=2x^{1/2}+3x^{-2}-x^{1/3}.$$

In particular, differentiating the negative reciprocal produces the positive integrand term $3/x^2$, checking the most likely sign error. The formula is used only for $x>0$; writing powers has not removed the square-root restriction or the pole at zero.
