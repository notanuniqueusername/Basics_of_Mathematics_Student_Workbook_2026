# Exercise 1. Dominant Terms in a Sequence

## The question

Compute
$$\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.$$
Explain why the highest-degree terms determine the result.

## Before calculating: divide by the dominant power

Direct substitution of infinity is not arithmetic. For a quotient of polynomials, divide numerator and denominator by the highest power in the denominator, then use ordinary limit laws if the new denominator has a nonzero limit.

A sequence limit concerns the entire tail, not a finite collection of early values. Dividing by $n^2$ is valid for positive indices and turns the divergent polynomial pieces into quantities with finite limits. The quotient limit law can then be used because the transformed denominator tends to a nonzero number; that condition must be checked explicitly.

## 1. Normalize the quotient

For positive $n$,

$$\frac{4n^2-3n+1}{2n^2+5n-7}=\frac{4-3/n+1/n^2}{2+5/n-7/n^2}.$$

As $n\to\infty$, $1/n\to0$ and $1/n^2\to0$. The normalized numerator approaches $4$ and the denominator approaches $2\ne0$. Therefore

$$\boxed{\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}=2}.$$

The lower-degree contributions vanish relative to $n^2$, explaining why the leading coefficients determine the answer.

## 2. Address the domain

The denominator factors as $(n-1)(2n+7)$, so $n=1$ is excluded. A sequence limit depends only on sufficiently large indices; omitting this initial undefined term does not affect the result. We may regard the sequence as defined for integers $n\ge2$.

## 3. Turn the error formula into a quantitative bound

For $n\ge2$, $2n^2+5n-7\ge2n^2$ and $13n-15\le13n$. The exact error therefore satisfies

$$|a_n-2|=\frac{13n-15}{2n^2+5n-7}\le\frac{13}{2n}.$$

Given any tolerance $\varepsilon>0$, choosing an integer $N>13/(2\varepsilon)$ ensures $|a_n-2|<\varepsilon$ for every $n\ge N$. This gives an explicit definition-based justification of the limit.

The bound is not claimed to be the best possible estimate. Its purpose is to control all later terms at once, illustrating precisely what the dominant-term calculation establishes and what a finite numerical table would not establish.

## 4. Verification

Subtract the proposed limit:

$$\frac{4n^2-3n+1}{2n^2+5n-7}-2=\frac{-13n+15}{2n^2+5n-7}.$$

After division by $n^2$, this becomes $(-13/n+15/n^2)/(2+5/n-7/n^2)\to0$. Thus the original expression really differs from $2$ by a vanishing quantity; it approaches from below for all $n\ge2$.
