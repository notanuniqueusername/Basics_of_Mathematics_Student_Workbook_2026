# Problem 11. Choose the Method First

## The question

For each integral, first write which method you choose and how you recognize it, and then compute:
1. $\int\sin(3x)\,dx$,
2. $\int x\ln x\,dx$,
3. $\int\frac{x}{\sqrt{x^2+1}}\,dx$.

## Before calculating: select the mechanism from the structure

Use substitution when an inner derivative is present, and integration by parts when differentiating one factor simplifies a product. Domain restrictions remain part of an indefinite-integral answer.

Different-looking integrals can share a substitution structure, while similar-looking products may require different methods. The decision is whether a derivative of an inner expression is already present, or whether transferring differentiation to one factor will simplify a product. The logarithm additionally restricts the second integral to positive inputs before any method is applied.

## 1. Sine of a linear function: substitution

Choose $u=3x$, $du=3dx$:

$$\int\sin3x\,dx=\frac13\int\sin u\,du=\boxed{-\frac13\cos3x+C}.$$

## 2. A polynomial times a logarithm: integration by parts

For $x>0$, choose $u=\ln x$, $du=dx/x$, $dv=x\,dx$, and $v=x^2/2$:

$$\int x\ln x\,dx=\frac{x^2}{2}\ln x-\frac12\int x\,dx=\boxed{\frac{x^2}{2}\ln x-\frac{x^2}{4}+C}.$$

Differentiating the logarithm turns the remaining product into a simple power.

## 3. Compare the three method decisions directly

In the sine integral, the linear inner function has constant derivative $3$, so a compensating factor $1/3$ is all substitution needs. In the logarithmic product, neither factor is an obvious inner derivative multiplier, but differentiating $\ln x$ reduces it to $1/x$ and simplifies the product after integration by parts.

In the root denominator integral, the numerator $x$ is half the derivative of $x^2+1$, giving substitution coefficient $1/2$. Integrating the transformed $u^{-1/2}$ then introduces a factor $2$, which cancels that coefficient.

These explanations identify the sources of all prefactors and distinguish method selection from the mechanical evaluation that follows. The later differentiation checks confirm the choices did not lose a chain-rule factor or logarithmic domain restriction.

## 4. An inner derivative divided by a root: substitution

Set $u=x^2+1$, $du=2x\,dx$:

$$\int\frac{x}{\sqrt{x^2+1}}\,dx=\frac12\int u^{-1/2}\,du=\boxed{\sqrt{x^2+1}+C}.$$

## 5. Verification

Differentiate the three answers:

$$(-\cos3x/3)'=\sin3x,$$

$$\left(\frac{x^2}{2}\ln x-\frac{x^2}{4}\right)'=x\ln x+\frac x2-\frac x2=x\ln x,$$

$$\left(\sqrt{x^2+1}\right)'=\frac{2x}{2\sqrt{x^2+1}}.$$

The first and third formulas hold for all real $x$; the logarithmic one holds on $(0,\infty)$, the original domain.
