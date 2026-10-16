# Exercise 11. An n-th Root

## The question

Compute
$$\lim_{n\to\infty}\sqrt[n]{5^n+2^n}.$$
Explain which term dominates and why the transformation looks different from the case of a quotient of polynomials.

## Before calculating: factor inside the nth root

Exponential terms do not behave like polynomial powers. Extract the dominant exponential $5^n$ from inside the root; its nth root is exactly $5$.

Taking an nth root changes the effect of multiplicative factors dramatically: even a fixed factor $2$ becomes $2^{1/n}\to1$. That is why an upper bound differing by a factor $2$ before rooting can still produce a sharp limit after rooting. Ordinary polynomial degree comparisons do not capture this root mechanism.

## 1. Isolate the dominant term

$$\sqrt[n]{5^n+2^n}=\sqrt[n]{5^n\left(1+(2/5)^n\right)}=5\left(1+(2/5)^n\right)^{1/n}.$$

The smaller exponential has ratio $(2/5)^n\to0$. To justify the root factor's limit, use bounds rather than simply inserting the variable exponent into a continuity rule.

## 2. Squeeze the remaining factor

For every positive integer $n$,

$$1\le1+(2/5)^n\le2,$$

so

$$5\le\sqrt[n]{5^n+2^n}\le5\,2^{1/n}.$$

Since $2^{1/n}=e^{(\ln2)/n}\to1$, both bounds tend to $5$. Therefore

$$\boxed{\lim_{n\to\infty}\sqrt[n]{5^n+2^n}=5}.$$

## 3. Check the same limit with logarithms

All terms are positive, so logarithms are legitimate. If $b_n=\sqrt[n]{5^n+2^n}$, then

$$\ln b_n=\ln5+\frac1n\ln\left(1+(2/5)^n\right).$$

Since $0\le\ln(1+(2/5)^n)\le\ln2$, the correction is between $0$ and $(\ln2)/n$, hence tends to zero. Exponentiating gives $b_n\to e^{\ln5}=5$.

This confirms the squeeze argument and locates the entire correction explicitly. The smaller term $2^n$ still affects each finite value, making $b_n>5$, but its effect on the logarithm vanishes. Dominance here means a negligible limiting correction, not that $2^n$ is literally zero.

## 4. Verification and interpretation

The answer is at least the nth root of $5^n$, so it cannot be below $5$. Adding $2^n$ changes the rooted value by at most $5(2^{1/n}-1)$, which tends to zero. This gives an explicit vanishing bound on the error. Unlike polynomial quotients, no ratio of leading polynomial coefficients is involved: the root removes the dominant exponential power itself.

**Explain why the root limit is not a sum of roots.** In general $\sqrt[n]{a+b}$ is not $\sqrt[n]a+\sqrt[n]b$, so adding the separate rooted limits $5+2$ would be invalid. The factorization and bounds show that the answer is the larger exponential base, not their sum. More generally, for positive $a\ge b$, $a\le(a^n+b^n)^{1/n}\le a\,2^{1/n}$, proving the limit is $a$. The present result is that general comparison with $a=5$, $b=2$, and the factor $2^{1/n}$ explains why the smaller term cannot change the limit.
