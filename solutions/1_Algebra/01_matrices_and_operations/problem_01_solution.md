# Exercise 1. Matrix Size and Entries

## The question

We are given

$$A=\begin{pmatrix}2&-1&3\\0&4&5\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\-2&3\\4&1\end{pmatrix}.$$

1. What are the sizes of $A$ and $B$?
2. What are the entries $a_{12}$, $a_{23}$, $b_{21}$, $b_{32}$?
3. What are the second row of $A$ and the first column of $B$, written as vectors?

## Before calculating: the conventions

Everything here depends on two conventions, and mixing them up is the most common mistake in the whole topic.

- **Size** is always written as *rows × columns*.
- **Entries** are always indexed *row first, then column*. So $a_{ij}$ is the entry in row $i$, column $j$.

## 1. Sizes

Count the horizontal lines (rows) first, then the vertical lines (columns).

- $A$ has 2 rows and 3 columns, so $A$ is a $2\times 3$ matrix.
- $B$ has 3 rows and 2 columns, so $B$ is a $3\times 2$ matrix.

## 2. Reading off entries

For each entry, go down to the row given by the first index, then across to the column given by the second.

- $a_{12}$: row 1, column 2 of $A$, so $a_{12}=-1$.
- $a_{23}$: row 2, column 3 of $A$, so $a_{23}=5$.
- $b_{21}$: row 2, column 1 of $B$, so $b_{21}=-2$.
- $b_{32}$: row 3, column 2 of $B$, so $b_{32}=1$.

## 3. Rows and columns as vectors

The second row of $A$ is

$$\text{row}_2(A)=\begin{pmatrix}0&4&5\end{pmatrix},$$

a vector with 3 entries, written horizontally.

The first column of $B$ is

$$\text{col}_1(B)=\begin{pmatrix}1\\-2\\4\end{pmatrix},$$

a vector with 3 entries, written vertically.

## 4. Verification

The results can be checked against the sizes from step 1.

- A row of $A$ has as many entries as $A$ has columns: 3. ✓
- A column of $B$ has as many entries as $B$ has rows: 3. ✓
- The indices are valid: $a_{12}$ and $a_{23}$ need $i\le 2$, $j\le 3$, which fits a $2\times3$ matrix, and $b_{21}$ and $b_{32}$ need $i\le 3$, $j\le 2$, which fits a $3\times2$ matrix. ✓
