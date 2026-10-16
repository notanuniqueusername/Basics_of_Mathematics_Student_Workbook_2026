# Problem 6. When Does a Logarithm Appear from an Integral?

## The question

Compute
$$\int\frac{2x}{x^2+5}\,dx.$$
Identify the denominator as a candidate for substitution, compare the numerator with its derivative, and explain the source of the logarithm in the result.

## Before calculating: derivative over the original expression

The pattern $g'(x)/g(x)$ integrates to $\ln|g(x)|$ on intervals where $g\ne0$. Here $g=x^2+5>0$ everywhere, so absolute values are unnecessary after recognizing the sign.

A logarithm arises when the transformed integrand is $1/u$, not merely whenever a fraction appears. The numerator must match the denominator's derivative, up to a constant factor. If it did not, the substitution would leave additional dependence on $x$ and would not complete the calculation in the same way.

## 1. Identify the substitution

$$u=x^2+5,\qquad du=2x\,dx.$$

The numerator exactly matches the derivative of the denominator. Therefore

$$\int\frac{2x}{x^2+5}\,dx=\int\frac1u\,du.$$

## 2. Integrate and use positivity

$$\int\frac1u\,du=\ln|u|+C.$$

Since $u=x^2+5\ge5>0$,

$$\boxed{\int\frac{2x}{x^2+5}\,dx=\ln(x^2+5)+C,\quad x\in\mathbb R}.$$

The logarithm appears because the transformed exponent is $-1$, the exceptional exponent excluded from the ordinary power integration rule.

## 3. Explain the absolute value and why it can be removed here

The general derivative identity is $(\ln|g|)'=g'/g$ wherever $g\ne0$. The absolute value makes the logarithm argument positive even on intervals where $g$ is negative; the formula is applied separately on such intervals.

Here $g=x^2+5$ is positive on the entire real line, so $|g|=g$ everywhere. There are no poles splitting the domain and no separate interval constants to track. The final $\ln(x^2+5)+C$ is therefore a single family valid globally.

The denominator's derivative is exactly $2x$, including its coefficient. Had the numerator been $x$ instead, the answer would need a factor $1/2$. This comparison shows why checking the differential, not just recognizing the denominator's appearance, is essential.

## 4. Verification

$$\frac{d}{dx}\bigl(\ln(x^2+5)+C\bigr)=\frac1{x^2+5}\cdot2x,$$

which is exactly the original integrand. The denominator never vanishes, so the formula holds on one connected domain $\mathbb R$, with a single arbitrary constant. At $x=0$ the derivative is zero; its sign is negative on the left and positive on the right, consistently with the logarithm of a quadratic having its minimum there.
