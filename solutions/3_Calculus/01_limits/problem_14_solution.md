# Exercise 14. A $0/0$ Limit with Trigonometry

## The question

Compute
$$\lim_{x\to0}\frac{1-\cos x}{x^2}.$$
Justify the result without using l'Hôpital's rule, using a trigonometric identity and the fundamental limit.

## Before calculating: use a half-angle identity

The form is $0/0$. The identity $1-\cos x=2\sin^2(x/2)$ expresses the numerator in terms of the fundamental sine limit and avoids l'Hôpital's rule entirely.

The power of $x$ in the denominator suggests a second-order small numerator. The half-angle identity expresses $1-\cos x$ as the square of a first-order sine term, making that order visible without differentiation. Using only $\cos x\to1$ would give zero over zero and would lose the scale information needed for the answer.

## 1. Rewrite the quotient

For $x\ne0$,

$$\frac{1-\cos x}{x^2}=\frac{2\sin^2(x/2)}{x^2}=\frac12\left(\frac{\sin(x/2)}{x/2}\right)^2.$$

The factor $1/2$ comes from $2(x/2)^2/x^2=1/2$.

## 2. Apply the known limit

As $x\to0$, the argument $x/2\to0$ and $\sin(x/2)/(x/2)\to1$. Hence

$$\boxed{\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12}.$$

This conclusion uses radians, as does the fundamental trigonometric limit.

## 3. Track the factor of one half and the order of vanishing

The identity gives

$$1-\cos x=2\left(\frac{x}{2}\right)^2\left(\frac{\sin(x/2)}{x/2}\right)^2.$$

The first factor equals $x^2/2$, and the remaining squared ratio tends to $1$. Therefore the numerator is asymptotically $x^2/2$, explaining both its quadratic order and the coefficient in the limit.

A common mistake is to replace $\sin(x/2)$ by $x$ instead of $x/2$; that would introduce a factor-of-four error. Another is to use $1-\cos x\to0$ as if it settled the quotient. The two exact transformations in this solution retain the necessary scaling and avoid both mistakes without invoking l'Hôpital's rule or a Taylor series.

## 4. Verification by another identity

Rationalizing with $1+\cos x$ gives, near zero,

$$\frac{1-\cos x}{x^2}=\frac{1-\cos^2x}{x^2(1+\cos x)}=\frac{(\sin x/x)^2}{1+\cos x}\longrightarrow\frac1{2}.$$

The denominator tends to $2\ne0$, so this second route is valid. The expression is nonnegative on its domain because $1-\cos x\ge0$ and $x^2>0$, consistent with the positive answer.

**Check the symmetry of approach.** The quotient is even on its punctured domain: replacing $x$ by $-x$ leaves both $1-\cos x$ and $x^2$ unchanged. Its left and right values at equal distances from zero are therefore identical, not merely close. Numerically the stable half-angle expression gives about $0.49958347$ at $x=\pm0.1$ and $0.49999583$ at $x=\pm0.01$. Both approach the proved value $0.5$ from below, consistently with $|\sin t|\le|t|$. The table is an illustration; the exact sine-limit transformation proves the result.
