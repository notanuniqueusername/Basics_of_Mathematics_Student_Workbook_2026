# Problem 8. Choosing the Factors in Integration by Parts

## The question

Compute
$$\int x\cos x\,dx.$$
Before calculating, justify why it is convenient to differentiate $x$ and integrate $\cos x$, rather than the other way around.

## Before calculating: choose a degree-reducing factor

Use integration by parts with $u=x$, since its derivative becomes $1$, and $dv=\cos x\,dx$, whose antiderivative is $\sin x$. Reversing the choice would introduce $x^2\sin x$ and make the remaining integral more complicated.

The integration-by-parts choice should be justified by what happens to the remainder. A polynomial factor becomes simpler when differentiated, while a sine or cosine remains elementary when integrated. This is a strategy based on structure, not a rule that whichever factor happens to be written first must be chosen as $u$.

## 1. Record the differentials

$$u=x,\quad du=dx,\qquad dv=\cos x\,dx,\quad v=\sin x.$$

## 2. Apply integration by parts

$$\int x\cos x\,dx=x\sin x-\int\sin x\,dx.$$

Since $\int\sin x\,dx=-\cos x$,

$$\boxed{\int x\cos x\,dx=x\sin x+\cos x+C}.$$

The plus sign before cosine comes from subtracting its negative antiderivative. All terms are defined for every real $x$.

## 3. Track the correction sign through the whole calculation

The product term is $uv=x\sin x$. Subtracting the remainder gives $x\sin x-\int\sin x\,dx$. Since the antiderivative of sine is negative cosine, the two minus signs produce a positive correction:

$$x\sin x-(-\cos x)=x\sin x+\cos x.$$

Differentiating the product term alone gives $\sin x+x\cos x$, so the extra sine must be canceled. The derivative of the positive correction $\cos x$ is exactly $-\sin x$, accomplishing that cancellation.

This reconstruction explains the answer from the derivative rule rather than merely confirming it numerically. It also distinguishes this integral from $\int x\sin x\,dx$, where the corresponding trigonometric signs would differ.

## 4. Verification

$$\frac{d}{dx}[x\sin x+\cos x+C]=\sin x+x\cos x-\sin x=x\cos x.$$

The unwanted sine contributions cancel exactly. At $x=0$ the derivative and integrand are both zero; at $x=\pi$ they both equal $-\pi$. These point checks are consistent with the full symbolic verification, which proves the result throughout the domain. As in any indefinite integral, different choices of $C$ give vertical shifts of the same antiderivative shape.
