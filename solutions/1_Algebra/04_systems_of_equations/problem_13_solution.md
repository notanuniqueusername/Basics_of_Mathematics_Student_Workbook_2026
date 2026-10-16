# Exercise 13. Does Every Equation Add New Information?

## The question

Consider the system
$$x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.$$
Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## Before calculating: the concepts

An equation is redundant if it follows from the others, including its right-hand side.

## 1. Test the third equation for redundancy

Before solving, subtract the second equation from the first, taking the right-hand sides with them. The $x_2$ terms cancel, leaving exactly the third equation. Thus satisfying the first two automatically guarantees the third.

## 2. Find the parametric solution

Denote the equations by $E_1,E_2,E_3$. Subtract $E_2$ from $E_1$, including their right-hand sides:

$$(x_1+x_2)-(x_2+x_3)=10-8\quad\Longrightarrow\quad x_1-x_3=2.$$

This is exactly $E_3$, so it is redundant. The corresponding row operation $R_3\leftarrow R_3-R_1+R_2$ gives

$$\left[\begin{array}{ccc|c}1&1&0&10\\0&1&1&8\\0&0&0&0\end{array}\right].$$

There are two independent equations. Choose $x_2=s$. From $E_1$, $x_1=10-s$; from $E_2$, $x_3=8-s$. Thus

$$\boxed{(x_1,x_2,x_3)=(10-s,s,8-s),\quad s\in\mathbb R}.$$

Using $x_2$ as the parameter is valid even though column two is a pivot column in this displayed echelon form: the two independent equations can both be solved for the other two coordinates in terms of $x_2$. A nonpivot coordinate would give an equivalent parametrization.

## 3. Explain the number of independent equations

The first two coefficient rows are not multiples of one another, so they are independent. The third follows from them. Therefore there are two independent equations in three unknowns, leaving one free variable. The redundant equation can be removed without changing any solution, but it is still useful as a check.

## 4. Verification

Substitute into every equation:

$$(10-s)+s=10,\qquad s+(8-s)=8,$$

$$(10-s)-(8-s)=10-s-8+s=2.$$

The cancellation in the third equality shows explicitly that $E_3$ adds no condition on $s$. Taking $s=0$ gives $(10,0,8)$; taking $s=1$ gives $(9,1,7)$, so the solution is not unique. The first two coefficient rows are independent because neither is a multiple of the other. Therefore two independent restrictions, not three, determine the solution set.
