# Problem 5. The Same Substitution in a Different Context

## The question

Compute
$$\int xe^{x^2}\,dx.$$
First compare the structure with Problem 4 and explain what is common despite the different appearance of the function.

## Before calculating: the same inner derivative pattern

As in the preceding power example, the factor $x$ is proportional to the derivative of the inner expression $x^2$. The outside function is now exponential, but the substitution mechanism is unchanged.

The derivative of $e^{g(x)}$ is $g'(x)e^{g(x)}$, so an integrand proportional to that expression suggests substitution immediately. The constant ratio between the actual multiplier and the inner derivative must be carried through the integral. That ratio, not the outside function type, determines the prefactor in the answer.

## 1. Match the differential carefully

Choose $u=x^2$, so $du=2x\,dx$ and $x\,dx=du/2$. Hence

$$\int xe^{x^2}\,dx=\frac12\int e^u\,du.$$

The factor $1/2$ compensates for the missing $2$ in the original integrand. This step does not require dividing a formula by $x$ at zero.

## 2. Integrate and substitute back

$$\frac12\int e^u\,du=\frac12e^u+C,$$

so

$$\boxed{\int xe^{x^2}\,dx=\frac12e^{x^2}+C}.$$

The domain is $\mathbb R$. Substitution avoids trying to integrate $e^{x^2}$ alone, whose elementary antiderivative is not supplied by the ordinary exponential rule.

## 3. Explain the connection with the preceding substitution

In the power example, the outside function was $u^4$ and the inside was $x^2+1$. Here the outside is $e^u$ and the inside $x^2$. In both, differentiating the inside gives $2x$. The earlier integrand supplied that factor exactly; this one supplies only $x$, so its substitution introduces $1/2$.

This comparison is the method-selection mechanism requested in the problem. It also explains why substituting $u=e^{x^2}$ would work only after recognizing the same differential: $du=2xe^{x^2}dx$, making the original integral $\frac12\int du$. Either choice gives $e^{x^2}/2+C$, but the first names the inner layer more transparently and makes the analogy with the preceding exercise explicit.

## 4. Verification

$$\frac{d}{dx}\left(\frac12e^{x^2}+C\right)=\frac12e^{x^2}\cdot2x=xe^{x^2}.$$

At $x=0$, both the derivative and integrand are zero, confirming validity there. The original integrand is odd; the nonconstant antiderivative $e^{x^2}/2$ is even, consistent with its derivative being odd. Omitting $1/2$ would double the required derivative.
