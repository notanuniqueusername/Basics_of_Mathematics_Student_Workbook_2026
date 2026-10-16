# Exercise 14. A Small Change in the Right-Hand Side

## The question

Compare the systems
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3\end{cases}$$
and
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3.1.\end{cases}$$
Check the consistency of each system and explain why a small change in one number can change the type of the system.

## Before calculating: the concepts

Adding equations produces a necessary consistency condition. A redundant coefficient row must also have a compatible right-hand side.

## 1. Solve the two equations shared by both systems

Add $x+y=2$ and $2x-y=1$. This cancels $y$ and gives $3x=3$, hence $x=1$. The first equation gives $y=1$. Since these two equations are present in both systems, any solution of either system must be this same point.

## 2. Compare the two third equations

For the first system, add equations one and two:

$$(x+y)+(2x-y)=2+1\quad\Longrightarrow\quad 3x=3.$$

This gives $x=1$ and then $y=2-x=1$. Its third equation is precisely the sum already obtained, so it adds no restriction. The first system has the unique solution $\boxed{(1,1)}$.

For the second system, the first two equations are unchanged and still force $(1,1)$. But the third demands $3x=3.1$, which this pair cannot satisfy.

In augmented-matrix language, subtracting rows one and two from row three produces

$$\text{first system: }(0,0\mid3-2-1)=(0,0\mid0),$$

$$\text{second system: }(0,0\mid3.1-2-1)=(0,0\mid0.1).$$

The first is harmless; the second is the contradiction $0=0.1$. Thus the second system has $\boxed{\text{no solution}}$.

## 3. Explain the effect of the changed constant

The third coefficient row is the sum of the first two. Its constant must therefore be the sum $2+1=3$ for consistency. Replacing $3$ by $3.1$ breaks that exact relation. A small change can destroy consistency because the condition is an equality, not a tolerance interval.

## 4. Verification

For $(1,1)$, the first two left-hand sides are

$$1+1=2,\qquad 2\cdot1-1=1.$$

The third is $3\cdot1=3$, matching the first system but not the second. Conversely, if the changed equation held, it would force $x=3.1/3=31/30$, whereas the sum of the first two forces $x=1$.

More generally, replacing the third constant by $3+\varepsilon$ gives the necessary condition $0=\varepsilon$. Consistency occurs only at $\varepsilon=0$; any nonzero change, however small, makes this exact system inconsistent.
