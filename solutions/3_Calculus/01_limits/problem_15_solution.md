# Exercise 15. Observation Versus Proof

## The question

Choose one sequence and one function from this set. For the sequence, compute several values for increasingly large $n$. For the function, prepare a table of values with arguments approaching the limit point from the left and right. Sketch the behavior of both objects.

Compare the observation with the analytical result and explain why a finite number of calculations or a sketch does not constitute a proof that the limit exists.

## Before calculating: choose examples with exact simplifications

Use the sequence from Exercise 1 and the function from Exercise 7. Their analytical limits are $2$ and $2$, respectively. Tables show finite observations; proofs must control every sufficiently large index or every sufficiently nearby argument.

A plot or table samples the function and can suggest a conjecture, but a limit quantifies over every sufficiently close valid input. The two chosen examples are particularly useful because exact algebra produces error formulas that can be compared with every displayed number. The sketches are qualitative; their labels and tables carry the numerical scales.

## 1. Observe a sequence approaching its limit

Let $a_n=(4n^2-3n+1)/(2n^2+5n-7)$ for $n\ge2$.

| $n$ | $a_n$ (approximately) |
|---|---|
| $2$ | $1.000000$ |
| $10$ | $1.526749$ |
| $100$ | $1.937296$ |
| $1000$ | $1.993524$ |

```text
 a_n
 2  ····················· limit
                  •   •
            •
 1    •
      2    10    100   1000      n (not to scale)
```

Analytically, dividing by $n^2$ gives $(4-3/n+1/n^2)/(2+5/n-7/n^2)\to2$.

## 2. Observe a two-sided function limit

For $f(x)=(x^2-4x+3)/(x-3)$, use $f(x)=x-1$ when $x\ne3$.

| $x<3$ | $f(x)$ | $x>3$ | $f(x)$ |
|---|---|---|---|
| $2.9$ | $1.9$ | $3.1$ | $2.1$ |
| $2.99$ | $1.99$ | $3.01$ | $2.01$ |
| $2.999$ | $1.999$ | $3.001$ | $2.001$ |

```text
 f(x)
   |        /     line y=x-1
 2 |-------o      missing point (3,2)
   |      /
 --+------|------------ x
          3
```

## 3. Use the exact errors to explain the observations

For the sequence, the exact signed error is negative for all $n\ge2$:

$$a_n-2=\frac{-13n+15}{2n^2+5n-7}<0.$$

Its magnitude is at most $13/(2n)$, so all later terms, not merely those in the table, lie within any desired tolerance once $n$ is sufficiently large. The table's below-limit values are therefore explained analytically.

For the function, $f(3+h)=2+h$ whenever $h\ne0$. The left table uses negative $h$ and the right table positive $h$, giving equal-sized errors on opposite sides. This identity also explains the missing point at the center of the sketch. The finite observations and exact proofs agree, but only the latter control unlisted inputs and establish the claimed limits.

## 4. Verification and the role of proof

The exact error is $|f(x)-2|=|x-3|$, so choosing $0<|x-3|<\varepsilon$ proves convergence from both sides. For the sequence, $a_n-2=(-13n+15)/(2n^2+5n-7)\to0$.

The tables and sketches agree with these results but examine only finitely many inputs. They cannot exclude unusual behavior between samples or after the last listed index. Exact identities and limit laws supply the all-input argument that the observations lack.
