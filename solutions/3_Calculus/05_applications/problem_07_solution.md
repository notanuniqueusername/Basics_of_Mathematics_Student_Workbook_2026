# Problem 7. Exponential Growth

## The question

Assume the model
$$
N(t)=N_0e^{kt},\qquad k>0.
$$

1. Verify by differentiation that the model satisfies the relation $N'(t)=kN(t)$.
2. Find the population doubling time.
3. Explain why the doubling time does not depend on $N_0$.

## Before calculating: state the population assumption

Take $N_0>0$ for a genuine positive population and $k>0$ as given. The parameter $k$ has reciprocal-time units. Doubling means multiplying the current population by $2$, not adding a fixed number of individuals.

The proportional-growth equation says the relative rate $N'/N$ is constant, not that the absolute growth rate is constant. Since population itself increases, the number added per unit time also increases. Positive initial population is needed for the ordinary doubling interpretation; the zero-population solution has no distinct time at which it becomes twice a positive starting amount.

## 1. Verify proportional growth

By the chain rule,

$$N'(t)=N_0ke^{kt}=\boxed{kN(t)}.$$

The instantaneous growth rate is proportional to the current size, with constant proportionality $k$.

## 2. Solve for doubling time

Relative to $t=0$, require $N(T)=2N_0$:

$$N_0e^{kT}=2N_0\Longrightarrow e^{kT}=2\Longrightarrow kT=\ln2.$$

Thus

$$\boxed{T=\frac{\ln2}{k}}.$$

The positive initial population cancels, which explains why it does not affect the time. A larger $k$ gives a shorter doubling time.

## 3. Explain why equal time intervals multiply rather than add

For any increment $\Delta$, the model gives

$$N(t+\Delta)=N(t)e^{k\Delta}.$$

Thus the multiplicative factor depends on elapsed time but not on the starting population. Doubling uses the unique positive interval with factor $2$, namely $\Delta=(\ln2)/k$.

After two such intervals the population is $4N_0$, not $3N_0$, because each doubling acts on the current population. This clarifies the distinction from a constant-addition model, where the time needed to add another initial population would generally depend on the current size.

The quantity $kT=\ln2$ is dimensionless, consistently with the exponent $kt$. The formula's inverse dependence on $k$ also has the expected interpretation: doubling the growth-rate parameter halves the time needed for the same multiplicative change.

## 4. Verification

Substitution yields $N(T)=N_0e^{\ln2}=2N_0$. More generally, at any starting time $t$,

$$\frac{N(t+T)}{N(t)}=\frac{N_0e^{k(t+T)}}{N_0e^{kt}}=e^{kT}=2.$$

The same interval doubles the population regardless of its current size or starting time. The units of $\ln2/k$ are time, as required. If $N_0=0$, the model would remain zero and there would be no meaningful distinct doubling event; the positive-population assumption is what makes the cancellation and interpretation appropriate.
