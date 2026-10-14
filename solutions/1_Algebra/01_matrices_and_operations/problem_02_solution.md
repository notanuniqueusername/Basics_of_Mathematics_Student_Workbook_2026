# Exercise 2. Addition and Scalar Multiplication

## The question

We are given

$$A=\begin{pmatrix}1&2\\-1&3\end{pmatrix},\qquad B=\begin{pmatrix}4&-2\\0&5\end{pmatrix}.$$

1. Compute $A+B$, $A-B$, and $3A-2B$.
2. Explain why matrix addition is possible only for matrices of the same size.

## Before calculating: the rule

Addition, subtraction, and scalar multiplication all work **entry by entry**.

- $(A+B)_{ij}=a_{ij}+b_{ij}$
- $(A-B)_{ij}=a_{ij}-b_{ij}$
- $(cA)_{ij}=c\cdot a_{ij}$ (the scalar $c$ multiplies every entry)

Nothing is "mixed" between different positions. The entry in row $i$, column $j$ of the result depends only on the entries in row $i$, column $j$ of the inputs.

## 1. Compute $A+B$

Add the entries in matching positions:

$$A+B=\begin{pmatrix}1+4&2+(-2)\\-1+0&3+5\end{pmatrix}=\begin{pmatrix}5&0\\-1&8\end{pmatrix}.$$

## 2. Compute $A-B$

Subtract the entries in matching positions:

$$A-B=\begin{pmatrix}1-4&2-(-2)\\-1-0&3-5\end{pmatrix}=\begin{pmatrix}-3&4\\-1&-2\end{pmatrix}.$$

Note that $2-(-2)=4$. Subtracting a negative number is the most likely place for a sign error here.

## 3. Compute $3A-2B$

First apply the scalars, then subtract.

$$3A=\begin{pmatrix}3&6\\-3&9\end{pmatrix},\qquad 2B=\begin{pmatrix}8&-4\\0&10\end{pmatrix}.$$

$$3A-2B=\begin{pmatrix}3-8&6-(-4)\\-3-0&9-10\end{pmatrix}=\begin{pmatrix}-5&10\\-3&-1\end{pmatrix}.$$

## 4. Why the sizes must match

Since the operation works entry by entry, every entry of $A$ needs a partner in $B$ at the same position.

Suppose $A$ is $2\times2$ and $B$ is $2\times3$. Then the entries $b_{13}$ and $b_{23}$ have no partners in $A$, because $A$ has no third column. The sum $a_{13}+b_{13}$ would require an entry $a_{13}$ that does not exist. So the sum is simply not defined.

The same reasoning applies to subtraction. Scalar multiplication has no such restriction, because a single number is paired with every entry, so it works for any size.

## 5. Verification

Each result can be checked by undoing the operation.

- $(A+B)-B$ should give back $A$:
$$\begin{pmatrix}5&0\\-1&8\end{pmatrix}-\begin{pmatrix}4&-2\\0&5\end{pmatrix}=\begin{pmatrix}1&2\\-1&3\end{pmatrix}=A.\ ✓$$

- $(A-B)+B$ should give back $A$:
$$\begin{pmatrix}-3&4\\-1&-2\end{pmatrix}+\begin{pmatrix}4&-2\\0&5\end{pmatrix}=\begin{pmatrix}1&2\\-1&3\end{pmatrix}=A.\ ✓$$

- $3A-2B$ can be rebuilt a different way, from the two results above. We want $x(A+B)+y(A-B)=3A-2B$, which needs $x+y=3$ and $x-y=-2$, so $x=\tfrac12$ and $y=\tfrac52$:
$$\tfrac12\begin{pmatrix}5&0\\-1&8\end{pmatrix}+\tfrac52\begin{pmatrix}-3&4\\-1&-2\end{pmatrix}=\begin{pmatrix}\tfrac52-\tfrac{15}{2}&0+10\\-\tfrac12-\tfrac52&4-5\end{pmatrix}=\begin{pmatrix}-5&10\\-3&-1\end{pmatrix}.\ ✓$$

This matches the direct calculation, so the three results are consistent with each other.
