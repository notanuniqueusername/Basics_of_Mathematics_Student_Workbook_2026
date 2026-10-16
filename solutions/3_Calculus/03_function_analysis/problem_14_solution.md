# Problem 14. Reconstructing Information from the Derivative

## The question

It is known that
$$f'(x)=(x-1)(x+2).$$
Determine the monotonicity and the locations of the extrema, and sketch a possible qualitative shape of the function. Then, for
$$g(x)=\frac{x^3}{3}+\frac{x^2}{2}-2x$$
verify that $g'(x)=(x-1)(x+2)$, and compare the specific graph with the earlier qualitative sketch.

## Before calculating: derivative data leaves a vertical-shift freedom

Knowing $f'$ fixes increasing and decreasing intervals, but not the absolute heights of $f$. Two antiderivatives on $\mathbb R$ differ by a constant, so all possible graphs have the same shape with vertical shifts.

A derivative determines differences in function values through integration but leaves an additive constant undetermined. Consequently the horizontal locations and character of extrema are fixed by derivative signs, whereas their absolute heights require one function value or a specified representative such as $g$. The sample polynomial supplies that missing vertical placement.

## 1. Analyze the given derivative

For $f'(x)=(x-1)(x+2)$, the zeros are $-2$ and $1$.

| $x$ | $(-\infty,-2)$ | $-2$ | $(-2,1)$ | $1$ | $(1,\infty)$ |
|---|---|---|---|---|---|
| $f'$ | $+$ | $0$ | $-$ | $0$ | $+$ |

Thus $f$ increases, then decreases, then increases. There is a local maximum at $x=-2$ and local minimum at $x=1$. Their heights cannot be obtained from $f'$ alone.

## 2. Verify the supplied example

$$g'(x)=x^2+x-2=(x-1)(x+2).$$

Therefore $g$ has exactly the predicted monotonicity. Its extremum values are

$$g(-2)=-\frac83+2+4=\frac{10}{3},\qquad g(1)=\frac13+\frac12-2=-\frac76.$$

Every possible original $f$ is $g+C$.

## 3. Quantify what is fixed even before the vertical shift is known

All possible functions are $g+C$, so their extremum heights are $10/3+C$ and $-7/6+C$. Although neither height is fixed individually, their difference is:

$$\left(\frac{10}{3}+C\right)-\left(-\frac76+C\right)=\frac92.$$

Thus the drop from the local maximum to the local minimum is determined entirely by the derivative. The inflection argument is also fixed: differentiating $f'=x^2+x-2$ gives $f''=2x+1$, changing sign at $x=-1/2$.

For the supplied $g$, $g(-1/2)=13/12$, and shifting by $C$ shifts that height by the same amount. These relationships explain exactly which parts of the qualitative sketch are universal and which belong only to the selected representative.

## 4. Sketch and checks

```text
 y
         * max at x=-2
        / \
       /   \             /
 -----/-----\-----------/------ x
             \___*____/
                 min at x=1
```

The sketch's vertical placement is arbitrary for $f$; for $g$ use the heights $10/3$ and $-7/6$. Test points $-3,0,2$ give derivative values $4,-2,4$, confirming the sign chart. Also $g''=2x+1$ is $-3$ at $-2$ and $3$ at $1$, independently confirming the extrema.
