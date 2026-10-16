# Problem 8. Two Exponential Functions

## The question

For
$$f(x)=e^{2x-3}+5^x$$
compute the derivative. Explain why the factor $2$ appears in the first term and why $\ln5$ appears in the second.

## Before calculating: two sources of extra factors

For a composition $e^{g(x)}$, the chain rule supplies $g'(x)$. For a constant base $a>0$, $a^x=e^{x\ln a}$ supplies the factor $\ln a$. These are related but arise from different inner functions.

The natural exponential $e^u$ is special because its derivative with respect to $u$ is itself. For a different fixed base, rewriting in terms of e exposes an additional constant inner rate. Both terms are defined for all real $x$ because the bases are positive and there are no denominators or logarithms of variable-sign expressions.

## 1. Differentiate the natural exponential

For $g(x)=2x-3$, $g'=2$, so

$$\frac{d}{dx}e^{2x-3}=2e^{2x-3}.$$

The constant $-3$ shifts the exponent but has derivative zero.

## 2. Differentiate the base-five exponential

Write $5^x=e^{x\ln5}$. The inner derivative is $\ln5$, giving

$$\frac{d}{dx}5^x=(\ln5)5^x.$$

Therefore

$$\boxed{f'(x)=2e^{2x-3}+(\ln5)5^x}.$$

## 3. Compare two common incorrect derivatives

Writing only $e^{2x-3}$ for the first derivative would miss how fast the exponent changes: increasing $x$ by $h$ increases that exponent by $2h$. Conversely, the constant shift $-3$ changes the function's height factor $e^{-3}$ but adds no derivative multiplier.

For $5^x$, the exponent in the e-based representation is $x\ln5$, so its rate is $\ln5$, not $5$ and not $1$. Thus a proposed derivative $5^x$ would be correct only for base e, while $5\cdot5^{x-1}$ incorrectly treats the variable exponent as though the expression were a power of $x$.

The difference-quotient check below verifies both constant rates separately, preventing these two structurally different mistakes from being hidden in the final sum.

## 4. Verification

At zero the formula yields $f'(0)=2e^{-3}+\ln5>0$. Directly,

$$\frac{f(h)-f(0)}h=e^{-3}\frac{e^{2h}-1}h+\frac{e^{h\ln5}-1}h.$$

Using $(e^u-1)/u\to1$, the two terms approach $2e^{-3}$ and $\ln5$, respectively. This checks both additional factors. Both derivative terms are positive for every real $x$, so the function is strictly increasing throughout its domain.
