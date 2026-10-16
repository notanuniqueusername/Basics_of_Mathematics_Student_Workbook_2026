# Exercise 7. Choosing a Method Deliberately

## The question

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix
   $$\begin{cases}2x-y=3,\\4y=8;\end{cases}$$
2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

## Before calculating: the concepts

Choose a method using the matrix structure, the available computations, and the number of right-hand sides.

## 1. Assess what is already available

The first situation already has a triangular coefficient matrix, so the final variable can be read first. In the second, a previously known inverse removes the need for new elimination. In the third, there is only one right-hand side, so computing a full inverse would calculate more information than is needed.

## 2. Choose and justify each method

### Case 1: one triangular system

The last equation gives $4y=8$, hence $y=2$. Substitute upward:

$$2x-y=3\quad\Longrightarrow\quad 2x-2=3\quad\Longrightarrow\quad x=\frac52.$$

Thus $\boxed{(x,y)=(5/2,2)}$. Back substitution uses the existing triangular structure directly.

### Case 2: three right-hand sides and a known inverse

Use the given inverse three times:

$$x_1=A^{-1}b_1,\qquad x_2=A^{-1}b_2,\qquad x_3=A^{-1}b_3.$$

Equivalently, calculate all three columns together:

$$[x_1\ x_2\ x_3]=A^{-1}[b_1\ b_2\ b_3].$$

The inverse is reusable, and computing it again would be unnecessary.

### Case 3: one $3\times3$ system with no inverse supplied

Form $[A\mid b]$, use Gaussian elimination to create echelon form, then back-substitute if all variables have pivots. If a contradiction or free variable appears, interpret it instead of assuming uniqueness. There is no need to compute all columns of $A^{-1}$ to find one solution vector. The elimination operations on $A$ could be reused for later right-hand sides if needed.

## 3. Identify what can be reused

For repeated right-hand sides, the same inverse or the same elimination factorization can be applied repeatedly. The constants change, but the operations dictated by the coefficient matrix do not. Here the inverse is specifically already supplied in case two, so reusing it is an appropriate choice. Case three does not promise invertibility; elimination will also reveal any free variables or contradictions if they arise.

## 4. Verification

For case 1,

$$2\left(\frac52\right)-2=5-2=3,\qquad 4\cdot2=8.$$

For case 2, each formula satisfies $Ax_i=A(A^{-1}b_i)=(AA^{-1})b_i=b_i$. The three-column expression also has consistent dimensions: $(n\times n)(n\times3)=n\times3$.

For case 3, each row operation is reversible and is applied to the right-hand side as well as the coefficients, so it preserves the solution set. No numerical solution is claimed without numerical data; the requested result is the method and its justification.
