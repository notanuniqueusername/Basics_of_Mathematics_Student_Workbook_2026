# Exercise 2. Determinant of a 3×3 Matrix

## The question

For
$$A=\begin{pmatrix}1&2&-1\\0&3&4\\2&1&5\end{pmatrix}$$
compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

## Before calculating: the concepts

Sarrus' rule for a $3\times3$ determinant adds the three downward diagonal products and subtracts the three upward diagonal products. Adding a multiple of another row preserves a determinant.

## 1. Organize Sarrus' rule

Write the downward and upward products in separate sums before subtracting them. Each product uses one entry from every row and every column. This avoids losing the negative entry $a_{13}=-1$ and makes the final subtraction of a negative sum visible.

## 2. Calculate the two diagonal sums

For a general matrix $\begin{pmatrix}a&b&c\\d&e&f\\g&h&i\end{pmatrix}$, Sarrus' rule is

$$\det A=(aei+bfg+cdh)-(ceg+bdi+afh).$$

Here the three downward products are

$$aei=1\cdot3\cdot5=15,\quad bfg=2\cdot4\cdot2=16,\quad cdh=(-1)\cdot0\cdot1=0.$$

Their sum is $31$. The three upward products are

$$ceg=(-1)\cdot3\cdot2=-6,\quad bdi=2\cdot0\cdot5=0,\quad afh=1\cdot4\cdot1=4.$$

Their sum is $-2$. Subtract the entire upward sum:

$$\boxed{\det A=31-(-2)=33}.$$

Sarrus' rule in this form applies to $3\times3$ matrices; repeating diagonal patterns is not a general determinant method for larger sizes.

## 3. Choose an economical check

The row replacement in the verification leaves the determinant unchanged and makes the first column contain two zeros. Expanding along that column reduces the check to a single $2\times2$ determinant. This checks the answer with a different structure rather than repeating all six Sarrus products.

## 4. Verification

Use one short check based on a determinant-preserving row replacement:

$$R_3\leftarrow R_3-2R_1=(2,1,5)-(2,4,-2)=(0,-3,7).$$

Thus

$$\det A=\det\begin{pmatrix}1&2&-1\\0&3&4\\0&-3&7\end{pmatrix}=1\det\begin{pmatrix}3&4\\-3&7\end{pmatrix}=21-(-12)=33.$$

Only the first entry contributes in the first-column expansion, so this verifies the Sarrus result with one small determinant.
