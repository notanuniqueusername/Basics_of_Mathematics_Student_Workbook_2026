# Problem 9. Definite Integral and Geometric Area

## The question

Compute
$$\int_{-1}^{2}x\,dx.$$
Then separately compute the areas of the parts of the graph below and above the $x$-axis and explain the difference between the definite integral and geometric area.

## Before calculating: signed integral versus unsigned area

A definite integral counts contributions below the axis negatively. Geometric area counts both parts positively, so split at the zero of the integrand, $x=0$.

The fundamental theorem evaluates a definite integral as an antiderivative difference $F(b)-F(a)$. The arbitrary integration constant cancels, so a definite integral has one numerical result. Its sign reflects signed accumulation, whereas geometric area is obtained by integrating the absolute value or adding the nonnegative areas of sign-separated pieces.

## 1. Compute the signed integral

An antiderivative is $x^2/2$. Therefore

$$\boxed{\int_{-1}^2x\,dx=\left[\frac{x^2}{2}\right]_{-1}^2=2-\frac12=\frac32}.$$

## 2. Compute each geometric area

The part below the axis on $[-1,0]$ is a right triangle of base $1$ and height $1$, so its area is $A_-=1/2$.

The part above the axis on $[0,2]$ is a triangle of base $2$ and height $2$, so $A_+=2$.

Thus

$$\boxed{A_{\rm geometric}=A_-+A_+=\frac52},\qquad\int_{-1}^2x\,dx=A_+-A_-.$$

## 3. Explain the endpoint subtraction and the two different totals

The antiderivative has $F(2)=2$ and $F(-1)=1/2$. Although both endpoint values are positive, their difference is $3/2$; the sign contributions are clearer after splitting at zero.

On $[-1,0]$, $F(0)-F(-1)=0-1/2=-1/2$. On $[0,2]$, $F(2)-F(0)=2$. Adding gives the signed total $3/2$, while changing the first contribution's sign gives geometric area $5/2$.

The gap between the two totals is $1$, twice the below-axis area $1/2$. This is a useful general relationship: replacing a negative signed contribution by its positive area adds twice its magnitude. It explains why the two requested quantities legitimately differ even though they come from the same graph and endpoints.

## 4. Verification

Directly splitting the integral gives

$$\int_{-1}^0x\,dx=-\frac12,\qquad\int_0^2x\,dx=2.$$

Their sum is $3/2$, while integrating the absolute value gives $1/2+2=5/2$. This confirms that the difference between area and integral is not a computational discrepancy: they are different quantities whenever the integrand changes sign. The interval endpoints and the zero determine the two triangles exactly.
