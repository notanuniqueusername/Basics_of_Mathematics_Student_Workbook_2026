# Problem 10. Definite Integral and Checking the Result

## The question

Before carrying out the exact calculation, estimate the possible range of values of the integral
$$\int_0^2(x^2+1)\,dx,$$
using
$$1\le x^2+1\le5$$
on $[0,2]$. Only then compute the integral exactly, compare the result with the earlier estimate, and explain what type of computational error such a check can detect.

## Before calculating: estimate before finding an antiderivative

If $m\le f\le M$ on an interval of length $b-a$, then $m(b-a)\le\int_a^bf\le M(b-a)$. Here the supplied bounds are $1$ and $5$, and the interval length is $2$.

Bounds on the integrand yield bounds on the integral only after multiplication by the interval length. Here the width is $2$, so the function-height bounds $1$ and $5$ become area bounds $2$ and $10$. Omitting that width would compare unlike quantities and could make a correct exact answer appear inconsistent with the estimate.

## 1. Predict the range

Integrating the inequalities gives

$$\boxed{2\le\int_0^2(x^2+1)\,dx\le10}.$$

The lower and upper comparison rectangles have areas $2$ and $10$.

## 2. Compute exactly

$$\int_0^2(x^2+1)\,dx=\left[\frac{x^3}{3}+x\right]_0^2=\frac83+2=\boxed{\frac{14}{3}}.$$

Since $14/3\approx4.6667$, the result lies inside the predicted range. The function is nonnegative, so the integral also equals its geometric area above the axis.

## 3. Explain what the antiderivative and estimate each establish

The candidate $F=x^3/3+x$ has derivative $x^2+1$, so it supplies a valid primitive. Evaluating at the upper endpoint gives $8/3+2$, while the lower endpoint contributes zero. This exact endpoint calculation identifies the value $14/3$.

The prior rectangle estimate uses no antiderivative and therefore provides independent information about its plausible size. For example, reversing endpoint order would give $-14/3$, immediately contradicting positivity and the lower bound. Failing to divide the cubic antiderivative by $3$ could produce $10$, which is on the coarse bound but is excluded by the sharper split bound $3\le I\le7$.

An estimate's strength depends on its sharpness. It can reject inconsistent answers, but even a value passing both bounds still requires the exact primitive verification.

## 4. Verification and usefulness of the estimate

Differentiating $x^3/3+x$ returns $x^2+1$, checking the antiderivative. A sharper split uses $[0,1]$ and $[1,2]$: the function lies between $1,2$ on the first and $2,5$ on the second, giving $3\le\int_0^2f\le7$, also consistent with $14/3$.

A negative answer or a value above $10$ would certainly reveal an error, such as reversed endpoint subtraction or an incorrect integration factor. A value inside the bounds is only a consistency check, not proof of correctness; the antiderivative and endpoint evaluation supply the exact calculation.
