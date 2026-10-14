# Exercise 8. Row Operations and Their Reversibility

## The question

We are given

$$A=\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}.$$

Perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step, then state an operation that reverses each of the three.

## Before calculating: what a row operation is

A row operation changes one row of a matrix using other rows. There are three types:

- **add a multiple of one row to another** (steps 1 and 2),
- **swap two rows** (step 3),
- **scale a row by a non-zero number** (not used here, but it completes the list).

Each operation changes the matrix in a controlled way that loses no information. That is what makes them safe to use in elimination, and it is why each one can be undone.

## 1. Step 1: $R_2\leftarrow R_2-2R_1$

Subtract twice row 1 from row 2. Row 1 is $(1,2,-1)$, so $2R_1=(2,4,-2)$:

$$R_2-2R_1=(2-2,\ 4-4,\ 1-(-2))=(0,\,0,\,3).$$

Row 1 and row 3 stay unchanged:

$$A_1=\begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix}.$$

## 2. Step 2: $R_3\leftarrow R_3+R_1$

Add row 1 to row 3:

$$R_3+R_1=(-1+1,\ 1+2,\ 3+(-1))=(0,\,3,\,2).$$

$$A_2=\begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix}.$$

## 3. Step 3: interchange $R_2$ and $R_3$

Swap the second and third rows:

$$A_3=\begin{pmatrix}1&2&-1\\0&3&2\\0&0&3\end{pmatrix}.$$

The matrix is now **upper triangular** (zeros below the diagonal), which is the goal of elimination. The swap was needed because step 1 produced a zero in the pivot position of row 2.

## 4. Reversing each operation

To undo an operation, apply the operation that restores the previous matrix. Undo in the **reverse order**, last step first.

| Step | Operation | Reversing operation |
|---|---|---|
| 3 | $R_2\leftrightarrow R_3$ | $R_2\leftrightarrow R_3$ (swap again) |
| 2 | $R_3\leftarrow R_3+R_1$ | $R_3\leftarrow R_3-R_1$ |
| 1 | $R_2\leftarrow R_2-2R_1$ | $R_2\leftarrow R_2+2R_1$ |

Two points about these:

- A swap is its own inverse.
- Adding a multiple of a row is undone by subtracting the same multiple. This works because row 1, the row being added, is never altered by the operation itself.

The order matters. For example, if we undid step 1 before step 3, we would be adding $2R_1$ to the wrong row.

## 5. Verification

Apply the reversing operations to $A_3$ and check that we get back to $A$.

**Undo step 3** (swap $R_2$ and $R_3$):

$$\begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix}=A_2.\ ✓$$

**Undo step 2** ($R_3\leftarrow R_3-R_1$): $(0,3,2)-(1,2,-1)=(-1,1,3)$:

$$\begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix}=A_1.\ ✓$$

**Undo step 1** ($R_2\leftarrow R_2+2R_1$): $(0,0,3)+(2,4,-2)=(2,4,1)$:

$$\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}=A.\ ✓$$

We recover the original matrix exactly, so every operation was reversible.

**Determinant check.** Adding a multiple of a row does not change the determinant, and a swap changes its sign. So $\det A_3=-\det A$. Computing both:

$$\det A=1(12-1)-2(6+1)+(-1)(2+4)=11-14-6=-9,$$

$$\det A_3=1\cdot3\cdot3=9\quad(\text{triangular: product of the diagonal}).$$

Indeed $9=-(-9)$. ✓
