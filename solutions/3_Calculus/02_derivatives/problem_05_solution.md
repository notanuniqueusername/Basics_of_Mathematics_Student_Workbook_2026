# Problem 5. The Chain Rule as Working Through Layers

## The question

For
$$f(x)=(3x^2-2x+1)^5$$
identify the inner and outer functions, compute their derivatives, and combine the result according to the chain rule. Explain the origin of the additional factor.

## Before calculating: identify the two layers

The chain rule says $(F(g(x)))'=F'(g(x))g'(x)$. The outside derivative describes sensitivity to the inner value; multiplication by $g'$ accounts for how quickly that inner value changes with $x$.

A composition differs from a product: the output of one function becomes the input of another. In chain-rule notation, $F'(g(x))$ retains the whole original inner expression as its argument. Only after this outside differentiation is the inner derivative multiplied in. Confusing the layers can lead either to a missing factor or to an incorrectly changed argument.

## 1. Differentiate the inner and outer functions

$$g(x)=3x^2-2x+1,\quad g'(x)=6x-2,$$

$$F(u)=u^5,\quad F'(u)=5u^4.$$

## 2. Combine the factors

Evaluate the outer derivative at the inner expression and multiply:

$$\boxed{f'(x)=5(3x^2-2x+1)^4(6x-2)}.$$

The factor $6x-2$ comes from the inner derivative. Omitting it would differentiate with respect to the inner variable rather than with respect to $x$. The formula is defined for every real $x$.

## 3. Explain the additional factor as a rate conversion

Let $u=g(x)$. A small change in $x$ changes $u$ at rate $du/dx=6x-2$. The output $u^5$ changes with $u$ at rate $dF/du=5u^4$. Multiplying the two rates gives

$$\frac{df}{dx}=\frac{dF}{du}\frac{du}{dx}=5u^4(6x-2).$$

Substitute $u=3x^2-2x+1$ only after identifying both factors. At $x=1/3$, the inner expression has its minimum and its rate is zero, so the whole composition has zero derivative there. The outside factor remains positive because $3x^2-2x+1=3(x-1/3)^2+2/3>0$. This confirms that the inner rate controls the sign and the zero of the derivative in this example.

## 4. Verification

At $x=0$, $g(0)=1$ and $g'(0)=-2$, so the formula gives $f'(0)=-10$. The definition gives the same result: since $g(h)=1-2h+3h^2$, the binomial expansion of $g(h)^5$ has linear term $5(-2h)=-10h$, and all remaining nonconstant terms have degree at least two. Thus $(f(h)-f(0))/h\to-10$.

At $x=1/3$, $g'=0$ and $g=2/3>0$, so $f'=0$. This also confirms that the inner factor controls the zero slope.
