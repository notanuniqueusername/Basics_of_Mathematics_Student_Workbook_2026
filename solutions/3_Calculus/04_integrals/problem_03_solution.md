# Problem 3. Recognizing Basic Antiderivatives

## The question

Compute
$$\int\left(2e^x+3\cos x-4\sin x\right)\,dx.$$
Match each term with a known derivative and verify the entire result with one differentiation.

## Before calculating: match known derivatives

Use $(e^x)'=e^x$, $(\sin x)'=\cos x$, and $(\cos x)'=-\sin x$. Linearity permits integrating the three terms separately. Trigonometric arguments are measured in radians.

Basic antiderivative matching works because the derivative of a constant multiple is the same constant times the derivative. Linearity permits the matching terms to be added. In particular the minus sign in $(\cos x)'=-\sin x$ must be used in reverse carefully: a negative sine term corresponds to a positive cosine term.

## 1. Match each term

| Integrand term | Antiderivative | Reason |
|---|---|---|
| $2e^x$ | $2e^x$ | Natural exponential differentiates to itself |
| $3\cos x$ | $3\sin x$ | Sine differentiates to cosine |
| $-4\sin x$ | $4\cos x$ | Cosine derivative contributes a minus sign |

## 2. Combine the family

$$\boxed{\int(2e^x+3\cos x-4\sin x)\,dx=2e^x+3\sin x+4\cos x+C}.$$

Only one arbitrary constant is needed: separate constants from the three terms could be combined into a single real number. The domain is all real $x$.

## 3. Explain why direct integration is the appropriate method

No term is a product of unrelated varying factors or a nontrivial composition requiring a compensating inner derivative. Each is already a constant multiple of one known derivative, so substitution or integration by parts would add notation without simplifying anything.

The reconstruction can be checked term by term: $2e^x$ differentiates to the required exponential, $3\sin x$ to the required cosine, and $4\cos x$ to the required negative sine. Their common domain is the real line, allowing one additive constant for the entire family.

The sign check is especially important in the last term. If the answer contained $-4\cos x$, its derivative would produce $+4\sin x$, changing rather than matching the original integrand. Matching the outside coefficient alone without differentiating its candidate would miss that error.

## 4. Verification

Differentiate in one calculation:

$$\frac{d}{dx}(2e^x+3\sin x+4\cos x+C)=2e^x+3\cos x-4\sin x.$$

At zero, the derivative of the proposed antiderivative is $2+3-0=5$, equal to the integrand's value there. The full differentiation proves the identity for every $x$; the point evaluation is only a quick sign check. Choosing $-4\cos x$ instead would give $+4\sin x$, the wrong sign.
