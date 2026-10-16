# Problem 12. Several Rules at Once

## The question

For
$$f(x)=(x^2+1)^3e^x$$
compute the derivative. Before calculating, write down a plan: which rule applies to the whole expression and which rule applies to one of its factors. Finally, organize the result by factoring out common factors.

## Before calculating: apply the outermost rule first

The whole expression is a product $u(x)v(x)$ with $u=(x^2+1)^3$ and $v=e^x$. Use the product rule for the whole expression and the chain rule inside $u$.

When rules are combined, identifying the expression's outside structure prevents missing a whole contribution. The top-level operation here is multiplication, not cubing, so the product rule must be applied before focusing on the power inside the first factor. Factoring afterward makes the result easier to interpret without changing which rules justified it.

## 1. Differentiate each factor

$$u'=3(x^2+1)^2\cdot2x=6x(x^2+1)^2,\qquad v'=e^x.$$

The factor $2x$ is required because the cubed quantity is $x^2+1$, not $x$ itself.

## 2. Assemble and factor

$$f'=6x(x^2+1)^2e^x+(x^2+1)^3e^x.$$

Extract the common factors:

$$\boxed{f'(x)=e^x(x^2+1)^2\bigl(6x+x^2+1\bigr)=e^x(x^2+1)^2(x^2+6x+1)}.$$

Factoring does not change the derivative and makes its sign depend only on the last quadratic, since the other factors are positive.

## 3. Explain each factor in the organized derivative

The common factor $e^x$ appears in both product-rule terms because differentiating the exponential leaves it unchanged. The factor $(x^2+1)^2$ appears in the differentiated cube and divides the undifferentiated cube as well. After extracting them, the first term leaves $6x$ and the second leaves $x^2+1$.

Thus the remaining factor is $x^2+6x+1$, rather than just $6x$. At zero, that undifferentiated-factor contribution is the only nonzero one, producing $f'(0)=1$.

This decomposition is useful for checking the result: multiplying the factored expression back out must recover both original product-rule terms, and neither common factor can be dropped merely because it is positive in a sign analysis.

## 4. Verification

The original function is positive everywhere, so logarithmic differentiation provides an independent check:

$$\ln f=3\ln(x^2+1)+x\quad\Longrightarrow\quad\frac{f'}f=\frac{6x}{x^2+1}+1.$$

Multiplying by $f=(x^2+1)^3e^x$ reproduces the same two terms and factored answer. At $x=0$, $f'(0)=1$, checking that the exponential contribution remains even when the inner derivative vanishes.
