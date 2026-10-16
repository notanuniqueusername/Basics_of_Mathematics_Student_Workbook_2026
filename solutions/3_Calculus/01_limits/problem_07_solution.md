# Exercise 7. Limit at a Point and Canceling a Factor

## The question

Compute
$$\lim_{x\to3}\frac{x^2-4x+3}{x-3}.$$
Explain why the value of the function at $x=3$ is not needed to compute the limit.

## Before calculating: a limit uses nearby points

Direct substitution gives $0/0$, an indeterminate form. Factorization can remove a common vanishing factor, but cancellation is valid only away from the excluded point. That is sufficient for a limit.

Cancellation replaces the original expression by an equal expression only where the canceled factor is nonzero. A limit ignores the value at the approach point but still uses arbitrarily close valid inputs. This is why canceling $x-3$ is legitimate for the limit while declaring the original function equal to $x-1$ at every real number would be false.

## 1. Factor and cancel

$$x^2-4x+3=(x-1)(x-3).$$

For $x\ne3$,

$$\frac{x^2-4x+3}{x-3}=x-1.$$

The original expression and the simpler function agree on a punctured neighborhood of $3$, even though only the latter is defined at $3$.

## 2. Take the limit

By continuity of the polynomial $x-1$,

$$\boxed{\lim_{x\to3}\frac{x^2-4x+3}{x-3}=3-1=2}.$$

There is no need to assign the original function a value at $3$. Defining that value to be $2$ would produce a continuous extension; choosing another value would change continuity but not the limit.

## 3. Explain the removable discontinuity and extension

The graph away from $x=3$ is exactly the line $y=x-1$, with the point $(3,2)$ missing. There is no vertical blowup because nearby values remain near $2$. Defining a new function $g$ by the original formula for $x\ne3$ and $g(3)=2$ fills the hole and gives $g(x)=x-1$ everywhere.

If instead one assigned the value $g(3)=10$, the limit would still be $2$ but the new function would not be continuous at $3$. This separates the three ideas involved: the original domain excludes $3$, the nearby behavior determines the limit, and a chosen point value determines whether the extended function is continuous there.

## 4. Verification

For all $x\ne3$,

$$\left|\frac{x^2-4x+3}{x-3}-2\right|=|x-3|.$$

Given $\varepsilon>0$, taking $0<|x-3|<\varepsilon$ makes the error less than $\varepsilon$. This is a direct limit proof. For a numerical check, $x=2.99$ gives $1.99$ and $x=3.01$ gives $2.01$, consistent with approach from both sides.
