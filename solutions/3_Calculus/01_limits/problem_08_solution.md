# Exercise 8. A Square Root in a Function Limit

## The question

Compute
$$\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}$$
by rationalizing the numerator. Compare the idea with Exercise 3 involving a sequence.

## Before calculating: use the conjugate near a finite point

The real domain requires $x\ge0$ and the denominator excludes $x=4$. Near $4$, the square root is well-defined on both sides. Rationalization replaces the indeterminate form $0/0$ by an equivalent expression with a nonzero limiting denominator.

For a real square-root expression, both algebraic identities and domain restrictions matter. Multiplying by the conjugate is safe near $4$ because $\sqrt x+2$ is positive and never zero. Canceling $x-4$ then uses $x\ne4$, exactly the punctured-neighborhood condition permitted in a limit calculation.

## 1. Rationalize the numerator

For $x\ne4$,

$$\frac{\sqrt x-2}{x-4}\cdot\frac{\sqrt x+2}{\sqrt x+2}=\frac{x-4}{(x-4)(\sqrt x+2)}=\frac1{\sqrt x+2}.$$

## 2. Evaluate the limit

The new denominator approaches $2+2=4$, so

$$\boxed{\lim_{x\to4}\frac{\sqrt x-2}{x-4}=\frac14}.$$

In the sequence square-root exercise the initial form was $\infty-\infty$; here it is $0/0$. Both calculations use the same identity to expose a cancellable algebraic difference.

## 3. Quantify the error and relate the graph to a secant slope

Rationalize once more in the error expression:

$$\left|\frac1{\sqrt x+2}-\frac14\right|=\frac{|x-4|}{4(\sqrt x+2)^2}.$$

For $x\ge0$ the denominator is at least $16$, so the error is at most $|x-4|/16$. This gives a direct estimate proving approach to $1/4$ from either side.

Geometrically, the original quotient is the slope of the secant joining $(4,2)$ to $(x,\sqrt x)$. Its limiting value is therefore the tangent slope of the square-root curve at $(4,2)$. The rationalization proves that slope without first assuming a derivative formula, so the later derivative comparison is a consistency check rather than circular reasoning.

## 4. Verification

The difference from the answer is

$$\frac1{\sqrt x+2}-\frac14=\frac{2-\sqrt x}{4(\sqrt x+2)}\longrightarrow0.$$

For $x<4$ the simplified value is greater than $1/4$, and for $x>4$ it is smaller, so the two sides approach the same value from opposite directions. Also the expression is the difference quotient of $\sqrt x$ at $4$, consistent with derivative $1/(2\sqrt4)=1/4$ once that derivative is known.
