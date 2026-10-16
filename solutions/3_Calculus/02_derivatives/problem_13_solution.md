# Problem 13. A Multi-Layer Composition

## The question

For
$$f(x)=e^{\sin(x^2)}$$
compute the derivative. First write the layers
$$x\longrightarrow x^2\longrightarrow \sin(x^2)\longrightarrow e^{\sin(x^2)}$$
and explain why differentiation moves through them in the reverse order.

## Before calculating: three nested layers

The layers are $x\mapsto x^2\mapsto\sin(x^2)\mapsto e^{\sin(x^2)}$. The chain rule differentiates the outside function at its current input, then multiplies by the derivative of that input, repeating until reaching $x$.

For several layers, the chain rule is applied repeatedly, once at each interface. Every derivative is evaluated at the input that layer actually receives. The intermediate values $x^2$ and $\sin(x^2)$ must therefore remain inside their appropriate cosine and exponential expressions while the derivative factors are multiplied together.

## 1. Differentiate from outside inward

The exponential contributes $e^{\sin(x^2)}$. The sine layer contributes $\cos(x^2)$. The square layer contributes $2x$. Hence

$$\boxed{f'(x)=e^{\sin(x^2)}\cos(x^2)\,2x}.$$

No layer disappears: each contributes one multiplicative factor. The arguments remain unchanged when the outer layer is differentiated.

## 2. Explain the reverse-order description

Evaluation builds an output by starting with $x$ and applying successive layers. Differentiation analyzes the last operation first, then asks how its input changes, moving back through the composition. The final factors are scalar functions, so their written multiplication order may be rearranged without changing the result.

## 3. Write the derivative using named intermediate variables

Let $u=x^2$, $v=\sin u$, and $y=e^v$. Then

$$\frac{du}{dx}=2x,\qquad\frac{dv}{du}=\cos u,\qquad\frac{dy}{dv}=e^v.$$

Multiplying the rates gives

$$\frac{dy}{dx}=\frac{dy}{dv}\frac{dv}{du}\frac{du}{dx}=e^v\cos u\,2x.$$

Substituting the intermediate variables back produces the stated formula. This notation makes it visible that no layer is missing and explains the reverse-order description: start with the final output's dependence, then follow the dependence back to $x$.

For example, at $x=\sqrt\pi$, the cosine factor is $\cos\pi=-1$ and the exponential factor is $1$, so the derivative is $-2\sqrt\pi$, not merely the outside exponential value.

## 4. Verification

The function is even, so its derivative should be odd. The factors $e^{\sin(x^2)}$ and $\cos(x^2)$ are even, while $2x$ is odd; the formula has exactly the expected symmetry.

Also $f'(0)=0$. Directly, $|\sin(h^2)|\le h^2$ and the mean value theorem for the exponential gives $|e^{\sin(h^2)}-1|\le e h^2$ for small $h$. Dividing by $|h|$ gives a bound $e|h|\to0$, confirming the zero derivative from the definition.
