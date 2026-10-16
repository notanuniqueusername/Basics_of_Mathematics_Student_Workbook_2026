# Problem 3. The Product Rule — Why Is It Needed?

## The question

For
$$f(x)=(x^2+1)e^x$$
compute the derivative. Then compare the correct result with the incorrect idea
$$f'(x)\stackrel{?}{=}(2x)e^x$$
and explain which term is missing.

## Before calculating: a product has two changing factors

For $f=uv$, the product rule is $f'=u'v+uv'$. Differentiating just the first factor treats the second as constant, which is incorrect when it also depends on $x$.

The product rule can be motivated by splitting the increment of $uv$ into a change in the first factor and a change in the second. Both changes contribute to first order. Treating one varying factor as constant suppresses a genuine contribution, even if the other factor's derivative has been computed correctly.

## 1. Differentiate both factors

Let $u=x^2+1$ and $v=e^x$. Then $u'=2x$ and $v'=e^x$. Therefore

$$f'(x)=2xe^x+(x^2+1)e^x=\boxed{e^x(x^2+2x+1)=e^x(x+1)^2}.$$

## 2. Identify the missing term

The proposed expression $2xe^x$ includes only $u'v$. It omits

$$uv'=(x^2+1)e^x,$$

which is nonzero for every real $x$. Thus the incorrect expression does not accidentally become correct at any real point.

## 3. Derive the two-term structure from an increment

Write $u=x^2+1$ and $v=e^x$. The exact identity

$$u(x+h)v(x+h)-u(x)v(x)=[u(x+h)-u(x)]v(x+h)+u(x)[v(x+h)-v(x)]$$

shows the two contributions. Divide by $h$ and let $h\to0$. The first term tends to $u'(x)v(x)$, using continuity of $v$, and the second tends to $u(x)v'(x)$.

For this function both terms are needed. At zero the first contribution vanishes because $u'(0)=0$, while the second equals $1$. That makes zero an especially effective diagnostic point for the incorrect proposed formula: it isolates exactly the term the mistaken calculation omitted.

## 4. Verification

At $x=0$, the correct derivative is $1$, whereas the proposed one gives $0$. The definition confirms the nonzero slope:

$$\frac{f(h)-f(0)}h=\frac{(h^2+1)e^h-1}h=\frac{e^h-1}h+he^h\longrightarrow1+0=1.$$

This separately detects the omitted exponential contribution. The factored formula also shows $f'(x)\ge0$, with zero only at $x=-1$, consistently with the sum-of-terms calculation.

**Check what the factored derivative says at its zero.** The formula $e^x(x+1)^2$ vanishes at $x=-1$, but it is positive on both sides because the exponential is positive and the squared factor is nonnegative. Thus this stationary point is not a local maximum or minimum. This illustrates why a derivative formula can reveal more than a single slope, but its zeros still require sign interpretation. The function increases through the stationary point, so identifying $f'(-1)=0$ alone would not justify calling it a turning point.
