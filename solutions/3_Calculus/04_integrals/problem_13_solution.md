# Problem 13. An Integral Depending on the Upper Limit

## The question

Let
$$F(x)=\int_0^x(t^2+1)\,dt.$$
Determine $F(x)$, compute $F'(x)$, and compare the result with the integrand. Explain in your own words why the height of the function describes the local rate of increase of the accumulated area.

## Before calculating: the upper endpoint is variable

The variable $t$ is a dummy integration variable; $x$ determines how far accumulation extends. The fundamental theorem of calculus states that integrating a continuous function up to $x$ gives a function whose derivative is that integrand at $x$.

The variable-limit integral defines a new function of its endpoint. The dummy symbol $t$ distinguishes the integration variable from the final input $x$. For negative endpoints, the oriented integral remains well-defined; “accumulated area” must then be understood as signed accumulation, not necessarily a positive geometric area from the origin.

## 1. Evaluate the accumulation function

$$F(x)=\left[\frac{t^3}{3}+t\right]_0^x=\boxed{\frac{x^3}{3}+x}.$$

The formula is valid for all real $x$. For $x<0$, the orientation reverses: $\int_0^x=-\int_x^0$, so $F$ is negative even though the integrand is positive.

## 2. Differentiate and interpret

$$\boxed{F'(x)=x^2+1}.$$

A small increase $h$ in the endpoint adds a thin signed strip with width $h$ and height close to $x^2+1$. Its area is approximately $(x^2+1)h$, explaining why the integrand's height gives the local rate of accumulation.

## 3. Derive the rate interpretation from a short added interval

By additivity of oriented integrals,

$$F(x+h)-F(x)=\int_x^{x+h}(t^2+1)\,dt.$$

Dividing by $h$ gives the average integrand height on the short interval, with the same interpretation for negative $h$ after orientation is accounted for. As the interval shrinks, continuity makes every height in it approach $x^2+1$, so its average approaches that value too.

This is the mechanism behind the fundamental theorem here. It explains why the derivative is the original integrand evaluated at the endpoint, rather than its antiderivative or its derivative. The explicit polynomial calculation later checks the theorem's prediction through an exact difference quotient and also verifies the initial value $F(0)=0$.

## 4. Verification

The initial condition is $F(0)=0$, matching an integral over a zero-length interval. More precisely, direct expansion gives

$$\frac{F(x+h)-F(x)}h=x^2+1+xh+\frac{h^2}{3}\longrightarrow x^2+1.$$

This confirms the derivative through its definition. Since $F'(x)>0$ everywhere, accumulation increases as the endpoint moves right, including when it moves through negative values of $x$; this agrees with the oriented-integral interpretation.
