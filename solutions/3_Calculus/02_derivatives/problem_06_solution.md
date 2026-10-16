# Problem 6. Product Rule and Trigonometry

## The question

For
$$f(x)=x\sin x+\cos x$$
compute the derivative and simplify the result. Then compute $f'(0)$ and interpret the direction of the tangent line at that point.

## Before calculating: differentiate the product before simplifying

The term $x\sin x$ is a product. Use $(\sin x)'=\cos x$ and $(\cos x)'=-\sin x$, with arguments in radians.

A sum of functions is differentiated termwise, but an individual term can still require its own rule. Here $x\sin x$ requires the product rule while $\cos x$ uses a basic trigonometric derivative. Simplification comes after those rules are applied, so cancellations are visible and can be justified rather than guessed.

## 1. Apply the rules

$$(x\sin x)'=1\cdot\sin x+x\cos x.$$

Therefore

$$f'(x)=\sin x+x\cos x-\sin x=\boxed{x\cos x}.$$

The two sine terms cancel; omitting the $\sin x$ contribution from the product rule would prevent that cancellation.

## 2. Interpret the derivative at zero

$$\boxed{f'(0)=0},\qquad f(0)=0+1=1.$$

The tangent is horizontal at $(0,1)$, with equation $\boxed{y=1}$. A zero derivative is neither positive nor negative and does not by itself prove an extremum.

## 3. Explain the cancellation and the tangent geometrically

The product rule contributes $\sin x$ from differentiating $x$, and $x\cos x$ from differentiating the sine factor. Differentiating the separate cosine term contributes $-\sin x$. These first and last terms cancel because they are exact opposites.

At zero, $f(0)=1$ and $f'(0)=0$, so the tangent model is the constant height $1$. The exact height difference can be written

$$f(h)-1=h\sin h+\cos h-1.$$

The first contribution is of order $h^2$, and the second is also of order $h^2$ by the half-angle identity. Their sum is negligible relative to $h$, explaining the horizontal tangent. A horizontal tangent describes a local slope, not a claim that the function remains constant away from the contact point.

## 4. Verification

Use the definition at zero:

$$\frac{f(h)-f(0)}h=\sin h+\frac{\cos h-1}{h}.$$

The first term tends to zero. For the second, $\cos h-1=-2\sin^2(h/2)$, so its quotient tends to zero as well, using $\sin(h/2)/(h/2)\to1$. Thus the difference quotient tends to $0$, agreeing with the derivative. Near zero, $\cos x>0$, so $f'$ has the sign of $x$: the horizontal tangent here is in fact at a local minimum.
