# Exercise 15. Classifying Three Systems

## The question

For each of the following systems, perform only as much elimination as necessary to recognize its type:

1. $\begin{cases}x+y=2,\\x-y=0,\end{cases}$
2. $\begin{cases}x+y=2,\\2x+2y=4,\end{cases}$
3. $\begin{cases}x+y=2,\\2x+2y=5.\end{cases}$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

## Before calculating: the concepts

Eliminate only enough to identify pivots, zero rows, or contradictions.

## 1. Use the same elimination idea three times

For each system, remove $x$ from the second row using the first. In case one subtract the first row once; in cases two and three subtract it twice. The resulting second row is enough to distinguish a pivot, a harmless zero row, and a contradiction.

## 2. Classify the three reduced systems

### System 1

Subtract row one from row two:

$$\left[\begin{array}{cc|c}1&1&2\\1&-1&0\end{array}\right]\longrightarrow\left[\begin{array}{cc|c}1&1&2\\0&-2&-2\end{array}\right].$$

Two nonzero pivots give exactly one solution. The last row gives $y=1$, then $x=1$.

### System 2

Subtract twice row one from row two:

$$\left[\begin{array}{cc|c}1&1&2\\2&2&4\end{array}\right]\longrightarrow\left[\begin{array}{cc|c}1&1&2\\0&0&0\end{array}\right].$$

There is no contradiction, but only one pivot for two variables. Therefore there are infinitely many solutions: $(x,y)=(2-s,s)$.

### System 3

Apply the same replacement:

$$\left[\begin{array}{cc|c}1&1&2\\2&2&5\end{array}\right]\longrightarrow\left[\begin{array}{cc|c}1&1&2\\0&0&1\end{array}\right].$$

The last row is $0=1$, so there is no solution. No further elimination is needed in any of the three cases.

## 3. Relate each outcome to its solution set

A nonzero coefficient in the last equation determines the remaining variable, giving uniqueness. A fully zero augmented row imposes no restriction, leaving one free variable and infinitely many solutions. A zero coefficient row with a nonzero constant is impossible, giving no solution. These three different last rows explain all three classifications.

## 4. Verification

**System 1:** $(1,1)$ gives $1+1=2$ and $1-1=0$.

**System 2:** for every real $s$, $(2-s)+s=2$ and $2(2-s)+2s=4$. Distinct values of $s$ give distinct pairs.

**System 3:** the first equation forces $2x+2y=2(x+y)=4$, contradicting the required $5$.

The classifications are therefore, respectively, one solution, infinitely many solutions, and no solution. A zero coefficient row alone is not enough to distinguish the last two cases: its augmented constant must also be inspected.
