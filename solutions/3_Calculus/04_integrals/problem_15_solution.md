# Problem 15. Recovering a Function from Its Derivative and a Condition

## The question

The function $F$ satisfies
$$F'(x)=2xe^{x^2}$$
and
$$F(0)=3.$$

1. Recognize the method needed to find the function $F$.
2. Determine the entire family of functions with the given derivative.
3. Use the condition $F(0)=3$ to determine the correct constant.
4. Verify the final result by differentiation and substitution of $x=0$.

## Before calculating: integrate first, then use the condition

The derivative $2xe^{x^2}$ contains an exponential of $x^2$ multiplied by the inner derivative $2x$. Use substitution to find the whole antiderivative family; the extra value condition selects one member.

The initial condition is imposed only after finding the full antiderivative family. It determines an additive constant, not a new coefficient of the varying part. The derivative condition controls slopes on the whole domain, while the value condition fixes one height; together they can determine a unique function on a connected interval.

## 1. Recover the family

Choose $u=x^2$, so $du=2x\,dx$:

$$F(x)=\int2xe^{x^2}\,dx=\int e^u\,du=e^u+C.$$

Thus

$$\boxed{F(x)=e^{x^2}+C}.$$

This family is defined for every real $x$. The constant cannot be determined from the derivative alone because its derivative is zero.

## 2. Impose the prescribed value

$$F(0)=e^0+C=1+C=3.$$

Therefore $C=2$ and

$$\boxed{F(x)=e^{x^2}+2}.$$

The coefficient of the exponential is not arbitrary: multiplying it by a different constant would change the derivative. Only an additive constant is free.

## 3. Explain why both conditions must be checked separately

A function such as $e^{x^2}+10$ has the correct derivative but fails $F(0)=3$. Conversely, a constant function $F=3$ has the required initial value but the wrong derivative away from zero. Neither condition alone identifies the requested function.

The family $e^{x^2}+C$ makes the two roles separate: substitution and integration determine the nonconstant part, then $1+C=3$ determines the placement. The resulting $F=e^{x^2}+2$ has minimum value $3$ at zero because $e^{x^2}\ge1$.

Its derivative $2xe^{x^2}$ is negative for $x<0$ and positive for $x>0$, agreeing with this minimum and providing an additional qualitative consistency check on the recovered function. The domain is all real numbers, so one initial value fixes the constant throughout the entire connected domain.

## 4. Verification

Differentiate the selected function:

$$\frac{d}{dx}(e^{x^2}+2)=e^{x^2}\cdot2x=2xe^{x^2}.$$

Substitute the initial point: $F(0)=1+2=3$. Both conditions are satisfied independently. Finally, any other solution has the same derivative, so its difference from this $F$ is constant on $\mathbb R$; equality at $0$ forces that difference to be zero. This proves uniqueness, not just existence.
