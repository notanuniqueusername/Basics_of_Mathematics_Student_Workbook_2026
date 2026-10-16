# Exercise 4. Powers and Oscillation

## The question

Analyze
$$\left(\frac23\right)^n,\qquad \left(\frac32\right)^n,\qquad (-1)^n,\qquad \frac{(-1)^n}{n}.$$
For each sequence, describe the type of behavior and justify your answer.

## Before calculating: magnitude and oscillation are different issues

A geometric sequence $q^n$ tends to zero when $|q|<1$ and grows without bound when $q>1$. An oscillating sign prevents convergence only if its magnitude does not vanish.

A convergent real sequence must eventually stay arbitrarily close to one fixed number. Oscillation is compatible with this only if its amplitude shrinks. Looking at absolute values isolates the amplitude, while subsequences can detect incompatible persistent values. These are complementary tools: a vanishing absolute value proves convergence, and distinct subsequential limits disprove it.

## 1. Classify the four sequences

| Sequence | Behavior | Reason |
|---|---|---|
| $(2/3)^n$ | Converges to $0$ | Positive geometric decay |
| $(3/2)^n$ | Diverges to $+\infty$ | Positive geometric growth |
| $(-1)^n$ | No limit | Even terms $1$, odd terms $-1$ |
| $(-1)^n/n$ | Converges to $0$ | Sign oscillates but magnitude vanishes |

For the last sequence,

$$-\frac1n\le\frac{(-1)^n}{n}\le\frac1n.$$

Both bounds tend to zero, so the squeeze theorem proves the result.

## 2. Justify growth and nonconvergence

Bernoulli's inequality gives $(3/2)^n=(1+1/2)^n\ge1+n/2\to\infty$. Taking reciprocals also gives $(2/3)^n\le1/(1+n/2)\to0$.

If $(-1)^n$ converged, all subsequences would have the same limit. Its even and odd subsequences are constant at different values, making convergence impossible.

## 3. Distinguish boundedness, convergence, and divergence to infinity

The sequence $(-1)^n$ is bounded between $-1$ and $1$ but does not converge, so boundedness alone is insufficient. The sequence $(-1)^n/n$ is also bounded, but its even and odd subsequences both approach zero, consistently with the squeeze proof.

For a direct tolerance statement, $|(-1)^n/n-0|=1/n<\varepsilon$ whenever $n>1/\varepsilon$, independent of parity. In contrast, no interval of radius less than $1$ around a single number can contain both $1$ and $-1$ eventually.

The sequence $(3/2)^n$ is not merely nonconvergent: its lower bound $1+n/2$ eventually exceeds every prescribed threshold. That stronger property justifies the specific notation $+\infty$.

## 4. Verification

At $n=4,5$, the last two sequences take values $1,-1$ and $1/4,-1/5$, respectively. This illustrates the distinction: the first oscillation retains a fixed gap, while the second is confined to an interval shrinking to zero. The examples support the proofs above; they do not replace them.
