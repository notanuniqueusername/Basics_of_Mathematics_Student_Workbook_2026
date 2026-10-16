# Problem 7. Integration by Parts as Reversing the Product Rule

## The question

Compute
$$\int xe^x\,dx.$$
First write the product differentiation rule and, on that basis, explain the meaning of the integration-by-parts formula. Verify the result by differentiation.

## Before calculating: derive integration by parts

The product rule is $(uv)'=u'v+uv'$. Integrating and rearranging gives

$$\int u\,dv=uv-\int v\,du.$$

Choose the polynomial factor to differentiate so that it becomes simpler, and the exponential to integrate because its antiderivative is immediate.

Integration by parts transfers differentiation from one factor to another while replacing the other by an antiderivative. It is useful when that transfer simplifies the remaining integral. The formula is an identity derived from the product rule, so the subtraction sign and the boundary product $uv$ are both necessary, not optional adjustments.

## 1. Choose the factors

$$u=x,\quad du=dx,\qquad dv=e^x\,dx,\quad v=e^x.$$

## 2. Apply the formula

$$\int xe^x\,dx=xe^x-\int e^x\,dx=xe^x-e^x+C.$$

Thus

$$\boxed{\int xe^x\,dx=e^x(x-1)+C}.$$

The remaining integral is simpler because differentiating $x$ has reduced its degree to zero. The domain is all real $x$.

## 3. Show exactly why the chosen factors simplify the problem

Differentiating the polynomial factor $x$ lowers its degree to zero, so the remaining integral becomes simply $\int e^x dx$. Integrating $e^x$ does not introduce a new function type or a more complicated expression.

If instead one differentiated $e^x$ and integrated $x$, the remainder would contain $x^2e^x/2$, whose polynomial factor has higher degree than the original. That choice is not algebraically invalid, but it does not make progress toward an easier integral.

The final answer $xe^x-e^x+C$ can be read as a correction to the naive guess $xe^x$: differentiating that guess adds an unwanted $e^x$, and subtracting its antiderivative removes exactly the extra contribution. This gives an intuitive explanation for the integration-by-parts correction.

## 4. Verification

Differentiate using the product rule:

$$\frac{d}{dx}[e^x(x-1)+C]=e^x(x-1)+e^x\cdot1=e^xx.$$

The extra $+e^x$ from differentiating $x-1$ cancels the $-e^x$ already inside the first term. This cancellation explains why the correction term is required: $xe^x$ alone would differentiate to $(x+1)e^x$, not $xe^x$.

At $x=0$, the derivative is zero as the integrand requires, providing a quick check of the subtraction sign.
