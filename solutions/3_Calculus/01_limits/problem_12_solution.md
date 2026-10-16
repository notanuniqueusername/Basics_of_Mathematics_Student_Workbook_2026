# Exercise 12. Exponential Function Limit

## The question

Compute
$$\lim_{x\to0}(1+3x)^{1/x}.$$
Connect the result with the limit from Exercise 5 and show the appropriate transformation.

## Before calculating: restrict to positive bases

For real powers defined by logarithms, the base must be positive. Near $x=0$, $1+3x>0$ for $x>-1/3$, so both sides of the limit are valid. The form $1^\infty$ is indeterminate.

The classical exponential limit is a pattern that must be matched in both its base increment and its exponent. A coefficient inside the base changes the effective exponent after substitution. The real-power expression is interpreted as $\exp(\ln(1+3x)/x)$, which also makes the positive-base domain requirement explicit.

## 1. Transform to the classical pattern

Set $u=3x$. Then $u\to0$ and $1/x=3/u$, giving

$$(1+3x)^{1/x}=(1+u)^{3/u}=\left((1+u)^{1/u}\right)^3.$$

The continuous-variable classical limit is $\lim_{u\to0}(1+u)^{1/u}=e$. Consequently

$$\boxed{\lim_{x\to0}(1+3x)^{1/x}=e^3}.$$

The coefficient $3$ changes the limiting exponent, so the answer is not merely e.

## 2. Justify the two-sided classical limit

To ensure the argument covers negative as well as positive $u$, write

$$\ln\big((1+u)^{1/u}\big)=\frac{\ln(1+u)}u.$$

Using $\ln(1+u)=\int_0^u(1+t)^{-1}\,dt$, the quotient is the average of the continuous function $(1+t)^{-1}$ between $0$ and $u$, hence tends to $1$ from either side. Exponentiation gives e. This extends the integer sequence pattern to a genuine two-sided function limit.

## 3. Explain both sides and why the answer exceeds one

For small positive $x$, the base exceeds $1$ and the exponent is positive, so the whole expression exceeds $1$. For small negative $x$, the base lies between $0$ and $1$ but the exponent is negative, again making the expression exceed $1$. Both sides are therefore consistent with the answer $e^3>1$.

The substitution $u=3x$ preserves the side of approach because its multiplier is positive. Its effect on the exponent is $1/x=3/u$, not $1/u$. That extra factor is responsible for cubing the classical limiting value. As a further check, replacing $3$ by a general constant $c$ would lead by the same logarithmic argument to $e^c$, illustrating precisely which part of the data determines the answer.

## 4. Verification

Directly, $\ln((1+3x)^{1/x})=3\ln(1+3x)/(3x)\to3$. Continuity of the exponential gives $e^3\approx20.0855$, agreeing with the transformed result. Positivity of the base near zero makes every logarithm used legitimate.
