# Problem 7. A Trigonometric Composition

## The question

For
$$f(x)=\sin(x^2+1)$$
compute the derivative. Explicitly identify the outer function, the inner function, and the derivative of the inner function. Finally, determine the sign of $f'(0)$.

## Before calculating: trigonometric chain rule

For a composition $\sin(g(x))$, differentiate the outer sine to cosine at the same inner argument, then multiply by $g'(x)$. Do not change the argument when differentiating the outside layer.

The chain rule for sine requires multiplying the cosine at the inner input by the inner derivative. The value of the outer derivative and the value of the inner derivative can have different signs or one can vanish. Evaluating the product requires both factors; inspecting only the trigonometric factor cannot determine its sign.

## 1. Identify the layers

$$F(u)=\sin u,\quad F'(u)=\cos u,$$

$$g(x)=x^2+1,\quad g'(x)=2x.$$

## 2. Compute the derivative

$$\boxed{f'(x)=\cos(x^2+1)\cdot2x=2x\cos(x^2+1)}.$$

Both the original function and its derivative have domain $\mathbb R$.

## 3. Use the local structure around zero to check the interpretation

The function is even because $f(-x)=\sin((-x)^2+1)=f(x)$. If an even function is differentiable at zero, its derivative there must vanish: equal height changes on opposite sides produce opposite one-sided secant slopes.

The explicit formula $2x\cos(x^2+1)$ is odd, agreeing with that symmetry. Since $\cos1>0$ and cosine is continuous, there is an interval around zero where the cosine factor stays positive. The derivative then has the sign of $x$: negative on the left and positive on the right. This supplies a full local minimum argument, rather than incorrectly treating a zero derivative alone as proof of a minimum.

## 4. Evaluate and interpret the requested sign

$$f'(0)=2\cdot0\cdot\cos1=\boxed{0}.$$

It has zero sign, not a positive sign merely because $\cos1>0$. The tangent at $(0,\sin1)$ is horizontal. Since cosine remains positive near the argument $1$, the nearby derivative changes from negative to positive, giving a local minimum.

## 5. Verification

The mean value theorem for sine gives $\sin(1+h^2)-\sin1=h^2\cos\xi_h$ for some intermediate $\xi_h$. Hence

$$\left|\frac{f(h)-f(0)}h\right|=|h\cos\xi_h|\le|h|\to0.$$

This checks the derivative at zero directly and makes clear why the vanishing factor $2x$ cannot be ignored.
