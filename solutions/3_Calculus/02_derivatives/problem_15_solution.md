# Problem 15. The Difference Quotient as a Check of the Derivative

## The question

Choose one function from the problem set and a point $x_0$ at which the derivative exists. Compute $f'(x_0)$ exactly, and then calculate
$$\frac{f(x_0+h)-f(x_0)}h$$
for $h=1$, $0.1$, and $0.01$. Compare the values with $f'(x_0)$ and explain why the difference quotient approaching a single number is consistent with the definition of the derivative, while a few computations do not replace a limit argument.

## Before calculating: choose a function with an exact quotient

Choose $f(x)=x^2$ from Problem 11 and $x_0=2$. Its derivative exists and equals $2x$, so the exact target value is $\boxed{f'(2)=4}$.

A difference quotient is a secant slope over a nonzero increment; a derivative is the limit of such slopes as that increment tends to zero. The values need not equal the derivative for finite $h$. To assess an approximation, it helps to derive an exact error expression before calculating decimals, rather than infer convergence solely from a short table.

## 1. Simplify before inserting numbers

For $h\ne0$,

$$\frac{f(2+h)-f(2)}h=\frac{(2+h)^2-4}h=\frac{4h+h^2}h=4+h.$$

The algebra avoids subtracting nearly equal numerical values and shows the approximation error exactly.

## 2. Compute the requested values

| $h$ | $f(2+h)$ | Difference quotient | Error from $4$ |
|---|---|---|---|
| $1$ | $9$ | $5$ | $1$ |
| $0.1$ | $4.41$ | $4.1$ | $0.1$ |
| $0.01$ | $4.0401$ | $4.01$ | $0.01$ |

These secant slopes approach the tangent slope as the increment shrinks.

## 3. Quantify the approximation error and its two sides

The exact quotient is $4+h$, so the error in approximating $f'(2)=4$ is $h$ and its absolute magnitude is $|h|$. Reducing $h$ by a factor of ten therefore reduces this particular error by exactly a factor of ten, explaining the pattern in the table.

For positive increments the secant slopes exceed the derivative; for negative increments they lie below it. Given a tolerance $\varepsilon$, every nonzero increment with $|h|<\varepsilon$ gives an error smaller than $\varepsilon$, proving the two-sided limit.

This error formula is special to the chosen quadratic, not a universal rule for finite differences. The general definition requires errors to vanish, but their rate and direction depend on the function and point.

## 4. Verification and proof

The exact identity gives $|(4+h)-4|=|h|\to0$. Thus the derivative limit is $4$, including negative increments, not only the positive values in the table. For example $h=-0.01$ gives $3.99$, also approaching $4$.

A finite number of computations cannot establish what happens for every sufficiently small increment or exclude unequal one-sided behavior. Here the table is consistent with the derivative definition, while the identity $4+h$ and its two-sided limit supply the proof. The selected point is in the domain, and all nearby increments are valid because a polynomial is defined on all of $\mathbb R$.
