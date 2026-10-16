# Problem 11. A Parameter and the Number of Extrema

## The question

For
$$f_a(x)=x^3-3ax$$
depending on $a$, determine the number of critical points and their character. Separate the parameter cases and justify why the structure of the graph changes.

## Before calculating: a parameter can change the number of derivative roots

The domain is $\mathbb R$ for every real $a$. Critical points satisfy $f_a'=0$, but their character must be determined from sign changes, including the repeated-root case.

Parameter cases should be separated before taking square roots. The equation $x^2=a$ has two real solutions only for positive $a$, one repeated solution at zero, and none for negative $a$. Repeated derivative roots can leave the sign unchanged, so their character must be analyzed rather than inferred from their existence.

## 1. Differentiate and separate cases

$$f_a'(x)=3x^2-3a=3(x^2-a).$$

**If $a>0$:** the critical arguments are $\pm\sqrt a$. The derivative is positive outside them and negative between them. Thus $-\sqrt a$ is a local maximum and $\sqrt a$ a local minimum, with

$$\boxed{f_a(-\sqrt a)=2a^{3/2},\qquad f_a(\sqrt a)=-2a^{3/2}}.$$

**If $a=0$:** $f_0=x^3$ and $f'_0=3x^2\ge0$. There is one critical point at $0$, but no extremum, because the derivative is positive on both sides. It is a stationary inflection point.

**If $a<0$:** $x^2-a>0$ for every $x$. There are no critical points and the function is strictly increasing.

## 2. Explain the structural change

For positive $a$, the two distinct real roots of the derivative enclose a decreasing interval. At $a=0$ they merge, leaving a double zero with no sign change. For negative $a$ there are no real roots. A zero derivative does not necessarily imply an extremum.

## 3. Explain the transition at the parameter threshold

For $a>0$, the two stationary points are separated by distance $2\sqrt a$, and their heights differ by $4a^{3/2}$. As $a\downarrow0$, both separations shrink to zero, so the peak and valley merge at the origin.

At $a=0$, the derivative becomes $3x^2$, which is nonnegative and positive on either side of zero. The decreasing interval has disappeared; the remaining stationary point is therefore not an extremum. For $a<0$, the derivative is strictly positive even at zero, removing the stationary point entirely.

The function remains odd for every parameter, since $f_a(-x)=-f_a(x)$. When the two extrema exist they must therefore be centrally symmetric, matching their arguments $\pm\sqrt a$ and opposite heights.

## 4. Verification

The second derivative is $f_a''=6x$. At $a>0$, it is negative at $-\sqrt a$ and positive at $\sqrt a$, confirming the maximum/minimum classification. At $a=0$, $x^3$ changes sign and increases through $0$, confirming it is not a turning point. The sample $a=-1$ gives $f'=3(x^2+1)>0$, illustrating the final case.
