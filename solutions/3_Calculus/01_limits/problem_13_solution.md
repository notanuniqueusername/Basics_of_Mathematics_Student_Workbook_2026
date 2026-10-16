# Exercise 13. Fundamental Trigonometric Limit

## The question

Using
$$\lim_{x\to0}\frac{\sin x}{x}=1,$$
compute
$$\lim_{x\to0}\frac{\sin5x}{x},\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}.$$
In each case, show how you reduce the expression to the fundamental limit.

## Before calculating: preserve the scaled argument

The fundamental limit $\sin t/t\to1$ uses angles measured in radians. Introduce matching arguments in numerator and denominator; any compensating constants must remain outside the fundamental-limit factors.

The supplied sine limit is a two-sided statement in radians. It applies after replacing its argument by any quantity tending to zero, including $5x$, $2x$, or $3x$. When dividing by another such ratio, one must also note its nonzero limit; a quotient of limits is not valid automatically when the denominator tends to zero.

## 1. First limit

For $x\ne0$,

$$\frac{\sin5x}{x}=5\frac{\sin5x}{5x}.$$

Since $5x\to0$,

$$\boxed{\lim_{x\to0}\frac{\sin5x}{x}=5\cdot1=5}.$$

## 2. Second limit

For sufficiently small nonzero $x$, $\sin3x\ne0$. Rewrite

$$\frac{\sin2x}{\sin3x}=\frac23\frac{\sin2x}{2x}\frac{3x}{\sin3x}.$$

Both sine ratios approach $1$, and their reciprocals are allowed because their limiting value is nonzero. Therefore

$$\boxed{\lim_{x\to0}\frac{\sin2x}{\sin3x}=\frac23}.$$

## 3. Explain how the constants can be checked before calculation

Near zero, each sine behaves like its own argument, not necessarily like $x$. Thus the first quotient compares $5x$ with $x$ and should have scale $5$. The second compares $2x$ with $3x$ and should have scale $2/3$.

The formal factorizations justify that prediction by multiplying these constants by factors tending to $1$. They also show why substituting $x=0$ directly is uninformative: both original quotients have the pattern $0/0$, but their nearby ratios retain the relative argument scales.

For either positive or negative sufficiently small $x$, the sine of each scaled argument has the same sign as that argument. This checks positivity of both limiting answers and guards against a sign introduced by an incorrect rearrangement.

## 4. Verification

For the first, subtract $5$: the error is $5(\sin5x/(5x)-1)\to0$. For the second, both $\sin2x$ and $\sin3x$ have the sign of $x$ sufficiently near zero, so the quotient is positive from either side, consistent with $2/3$.

The approximation $\sin(kx)\sim kx$ predicts these same answers, but the factorizations above are what justify that approximation through the supplied fundamental limit. Omitting the factors $5$ or $2/3$ would lose the argument scaling.
