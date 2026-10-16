# Exercise 6. A System with a Parameter — Which Cases Actually Occur?

## The question

Analyze, depending on the parameter $a$, the system
$$\begin{cases}x+y=2,\\ax+ay=4.\end{cases}$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

## Before calculating: the concepts

Analyze consistency before dividing by an expression involving a parameter.

## 1. Eliminate without dividing by the parameter

The second left-hand side is $a$ times the first for every value of $a$, including $a=0$. Subtract $a$ times the first augmented row from the second. This operation remains valid for every parameter and avoids accidentally excluding a case by division.

## 2. Separate the consistent and inconsistent cases

Keep the parameter symbolic and perform a row replacement valid for all $a$:

$$\left[\begin{array}{cc|c}1&1&2\\a&a&4\end{array}\right]\xrightarrow{R_2\leftarrow R_2-aR_1}\left[\begin{array}{cc|c}1&1&2\\0&0&4-2a\end{array}\right].$$

**If $a=2$:** the last row is $0=0$. The only independent equation is $x+y=2$. With $y=s$,

$$\boxed{(x,y)=(2-s,s),\quad s\in\mathbb R}.$$

**If $a\ne2$:** the last row is $0=4-2a$ with nonzero right-hand side. This is impossible, so there is no solution.

**Exactly one solution:** never occurs. The two coefficient rows are proportional for every $a$, so elimination never produces two pivots.

## 3. Explain why uniqueness is impossible

There is never a second independent coefficient row. If the right-hand sides are compatible, only one equation in two unknowns remains and a variable is free. If they are incompatible, no solution exists. This is why the requested classification has only two occurring types, despite three types being possible for linear systems in general.

## 4. Verification

At $a=2$, the family satisfies both equations:

$$(2-s)+s=2,\qquad 2(2-s)+2s=4.$$

For any $a\ne2$, the first equation forces $ax+ay=a(x+y)=2a$, and $2a\ne4$. This checks inconsistency for all other parameters at once. In particular, the sometimes-missed case $a=0$ becomes $0=4$, so it is also inconsistent. No division by $a$ was used, and no parameter value was lost.
