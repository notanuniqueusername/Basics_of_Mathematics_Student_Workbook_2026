# Exercise 10. Continuity of a Piecewise Function

## The question

Find $a$ so that
$$f(x)=\begin{cases}ax+1,&x<2,\\x^2-1,&x\ge2\end{cases}$$
is continuous at $x=2$. Explicitly compare the left-hand limit, right-hand limit, and function value.

## Before calculating: continuity matches three quantities

Continuity at $2$ requires the left limit, right limit, and defined value $f(2)$ to exist and agree. The branch with $x\ge2$ determines the value at the joining point.

The branch that includes equality determines $f(2)$, while the branches on either side determine their respective one-sided limits. Matching only the branch formulas at the endpoint is sufficient here because both are continuous polynomials on their sides; in a more general piecewise problem those one-sided limits would need separate calculation.

## 1. Compute the three quantities

The left branch is linear, so

$$\lim_{x\to2^-}f(x)=2a+1.$$

The right branch is polynomial, so

$$\lim_{x\to2^+}f(x)=2^2-1=3,\qquad f(2)=3.$$

## 2. Choose the parameter

Set $2a+1=3$. Then $2a=2$ and

$$\boxed{a=1}.$$

For any other $a$, the left and right limits differ, producing a jump at $2$. Each branch is continuous on its own interval, so the joining point is the only continuity issue.

## 3. Explain what the selected parameter does and does not guarantee

At $a=1$, the left branch has endpoint height $2a+1=3$, matching both the right limit and the assigned value. The graph therefore joins without a gap. Its slopes need not match: the left derivative is $1$, while the right derivative at $2$ is $2\cdot2=4$.

Thus the continuous function found here is not differentiable at the join. This is not a contradiction: the question asks for matching heights, not matching slopes. If $a\ne1$, the jump size from left limit to right value is $3-(2a+1)=2-2a$, showing directly why no other parameter can produce continuity. The parameter equation is linear with one solution, so the chosen value is unique.

## 4. Verification

At $a=1$, the left branch is $x+1$ and both branches approach $3$. For a direct error check,

$$|f(x)-3|=|x-2|\quad(x<2),$$

$$|f(x)-3|=|x^2-4|=|x-2||x+2|\quad(x\ge2).$$

When $|x-2|<1$, $|x+2|<5$, so choosing $\delta=\min(1,\varepsilon/5)$ ensures $|f(x)-f(2)|<\varepsilon$ from either side. This verifies continuity rather than only the equality of the symbolic endpoint formulas.
