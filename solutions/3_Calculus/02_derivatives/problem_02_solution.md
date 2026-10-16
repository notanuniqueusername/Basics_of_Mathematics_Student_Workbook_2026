# Problem 2. Powers, Roots, and the Domain

## The question

For
$$f(x)=2\sqrt{x}-\frac{3}{x^2}+x^{3/2}$$
1. rewrite the function using powers,
2. determine the domain,
3. compute the derivative,
4. compare the domain of the function with the domain of its derivative.

## Before calculating: rewrite powers and enforce the real domain

Real square roots require $x\ge0$, while the denominator $x^2$ requires $x\ne0$. Their intersection is the domain; rewriting must retain those restrictions.

For a real power on positive inputs, $(x^p)'=px^{p-1}$ applies to the fractional and negative exponents used here. Rewriting roots and reciprocals makes this one rule available, but it does not alter which real inputs the original expression permits. The derivative's domain must be determined after retaining those original restrictions.

## 1. Rewrite and determine the domain

$$f(x)=2x^{1/2}-3x^{-2}+x^{3/2},\qquad\boxed{D_f=(0,\infty)}.$$

The point $0$ is excluded by the original reciprocal term, not merely by a later derivative formula.

## 2. Apply the power rule

$$f'(x)=2\cdot\frac12x^{1/2-1}-3(-2)x^{-2-1}+\frac32x^{3/2-1}.$$

Since the reciprocal derivative exponent is $-2-1=-3$, this simplifies to

$$\boxed{f'(x)=x^{-1/2}+6x^{-3}+\frac32x^{1/2}=\frac1{\sqrt x}+\frac6{x^3}+\frac32\sqrt x}.$$

The domain of the derivative is $\boxed{D_{f'}=(0,\infty)}$, the same as the original function. There is no derivative at zero to consider because the function itself is undefined there.

## 3. Explain the three derivative contributions separately

The term $2x^{1/2}$ contributes $2(1/2)x^{-1/2}$, so its coefficient becomes $1$ and its exponent becomes $-1/2$. The term $-3x^{-2}$ contributes $(-3)(-2)x^{-3}$, explaining both the positive sign and the third power in the denominator. The term $x^{3/2}$ contributes $(3/2)x^{1/2}$.

At $x=1$, the individual contributions are $1$, $6$, and $3/2$, totaling $17/2$. Near zero the reciprocal terms become unbounded, but this does not create a derivative value at zero because the original function is undefined there. Both domains happen to be $(0,\infty)$ in this problem; equality of function and derivative domains is not a general rule for all functions.

## 4. Verification

At $x=1$, $f'(1)=1+6+3/2=17/2>0$. Every term of $f'$ is positive on the domain, so $f$ is strictly increasing there.

Check the reciprocal sign directly: $(-3/x^2)'=(-3)(-2)x^{-3}=+6/x^3$. A negative original coefficient therefore gives a positive derivative contribution, which is a common sign-error point in this exercise.
