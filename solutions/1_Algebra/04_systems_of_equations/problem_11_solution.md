# Exercise 11. A Parameter in a System of Three Equations

## The question

Analyze the number of solutions depending on $t$:
$$\begin{cases}x+y+z=1,\\x+ty+z=2,\\x+y+tz=3.\end{cases}$$
Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## Before calculating: the concepts

Separate parameter values that make a pivot zero before dividing by it.

## 1. Subtract the common equation

All three equations have coefficient $1$ on $x$, and share several other terms. Subtract the first equation from each of the other two. The constants become $2-1=1$ and $3-1=2$, while the remaining coefficients are both $t-1$.

## 2. Handle the ordinary and exceptional parameters

Form the augmented matrix and subtract row one from each lower row:

$$\left[\begin{array}{ccc|c}1&1&1&1\\1&t&1&2\\1&1&t&3\end{array}\right]\longrightarrow\left[\begin{array}{ccc|c}1&1&1&1\\0&t-1&0&1\\0&0&t-1&2\end{array}\right].$$

These replacements are valid for every real $t$.

**Case $t\ne1$.** Both lower pivots are nonzero, so

$$y=\frac1{t-1},\qquad z=\frac2{t-1}.$$

Use the first equation to recover $x$:

$$x=1-y-z=1-\frac3{t-1}=\frac{t-4}{t-1}.$$

There is exactly one solution,

$$\boxed{(x,y,z)=\left(\frac{t-4}{t-1},\frac1{t-1},\frac2{t-1}\right),\quad t\ne1}.$$

**Case $t=1$.** The last two rows give $0=1$ and $0=2$. Thus there is no solution. There is no value producing infinitely many solutions.

## 3. Explain why the exceptional case is separate

Division by $t-1$ is valid only when $t\ne1$. At $t=1$, return to the reduced equations before division. They become contradictions, not equations that permit arbitrary $y$ or $z$. This distinction rules out an infinite family at the exceptional value. For $t\ne1$, the two remaining pivots determine $y,z$, and the first equation determines $x$.

## 4. Verification

For $t\ne1$, verify the three original equations symbolically:

$$x+y+z=\frac{t-4+1+2}{t-1}=1,$$

$$x+ty+z=\frac{t-4+t+2}{t-1}=\frac{2t-2}{t-1}=2,$$

$$x+y+tz=\frac{t-4+1+2t}{t-1}=\frac{3t-3}{t-1}=3.$$

At $t=1$, all three left-hand sides equal $x+y+z$, while their required values are $1,2,3$, so consistency is impossible. This verifies the exceptional case directly, without substituting into a formula whose denominator would be zero.
