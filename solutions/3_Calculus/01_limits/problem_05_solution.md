# Exercise 5. The Classical Limit Leading to the Number $e$

## The question

Compute
$$\lim_{n\to\infty}\left(1+\frac1n\right)^n.$$
Calculate several values for increasing $n$ and compare the observed behavior with the value of the limit. Explain why a few values do not constitute a proof.

## Before calculating: the classical definition of e

A standard characterization of Euler's number is $e=\lim_{n\to\infty}(1+1/n)^n$. This can serve as the definition of $e$; its existence must then be established, rather than inferred from a finite table.

The symbol e denotes an exact real number, while $2.718281828$ is a decimal approximation. Identifying several matching digits numerically does not define a limit unless one has already established that the sequence converges. Here monotonicity and boundedness provide existence, and the standard notation e names the resulting value.

## 1. Identify the limit and observe values

$$\boxed{\lim_{n\to\infty}\left(1+\frac1n\right)^n=e\approx2.718281828}.$$

| $n$ | $(1+1/n)^n$ |
|---|---|
| $1$ | $2.000000$ |
| $2$ | $2.250000$ |
| $10$ | $2.593742$ |
| $100$ | $2.704814$ |
| $1000$ | $2.716924$ |

The values increase toward $e$, but the table alone does not establish that this continues indefinitely.

## 2. Explain existence without relying on the table

The binomial expansion is

$$\left(1+\frac1n\right)^n=\sum_{k=0}^n\frac1{k!}\prod_{j=0}^{k-1}\left(1-\frac jn\right).$$

For each fixed $k$, its factors increase as $n$ increases, and the next expansion adds a positive term. Thus the sequence is increasing. Each product is at most $1$, so the sequence is bounded above by $\sum_{k=0}^{\infty}1/k!\le3$, using $k!\ge2^{k-1}$ for $k\ge2$. Monotone bounded sequences converge; this limit is e.

## 3. Explain how the all-index argument differs from the table

For $k\le n$, the $k$th binomial term can be written

$$\binom nk\frac1{n^k}=\frac1{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}{n}\right).$$

Each factor is nonnegative and increases when $n$ increases; the next expansion also has a new positive final term. This establishes monotonicity for every index rather than only the tabulated pairs. Bounding each product by $1$ makes the total no larger than the convergent factorial series.

Thus the proof prevents both a later reversal and unbounded growth. The numerical table then illustrates how slowly the sequence approaches its limit: even $n=1000$ does not yet give the displayed first six digits of e.

## 4. Verification and limits of numerical evidence

Every listed value lies between $2$ and $3$, consistently with the proof, and its difference from the stated approximation decreases. A finite list cannot rule out a later change in behavior or identify an exact limit. The monotonicity and bound concern all indices, which is the essential difference between observation and proof.
