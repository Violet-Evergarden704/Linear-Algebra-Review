# Notes for Lecture 2:  Elimination with Matrices
**Elimination**
Example Matrix:
$$
A=
\begin{bmatrix}
1 & 2 & 1\\
3 & 8 & 1\\
0 & 4 & 1
\end{bmatrix}

$$

**1st pivot** : number in index(1,1)
Keep the pivot row unchanged
$$
A (row2 - 3 * row1) -> 
\begin{bmatrix}
1 & 2 & 1\\
0 & 2 & -2\\
0 & 4 & 1
\end{bmatrix}
$$
Make the number in (2,1) to be 0
Called the 21-step
Then 31-step, as (3,1)is already 0, skip
And now x is eliminated

**2nd pivot** : number in (2,2)
32-step:row3 - 2 * row2
$$
A (row3 - 2 * row2) -> 
\begin{bmatrix}
1 & 2 & 1\\
0 & 2 & -2\\
0 & 0 & 5
\end{bmatrix}
$$

**3nd pivot** : number in (3,3)

And the last matrix is called Upper Triangular(U)
Pivots can't be 0
If meet 0 in pivot position, try to switch rows which does not have 0 in pivot position

**Back Substitution**
Create the **Augmented Matrix**
$$
A = 
\begin{bmatrix}
1 & 2 & 1 & 2\\
3 & 8 & 1 & 12\\
0 & 4 & 1 & 2
\end{bmatrix}
->
\begin{bmatrix}
1 & 2 & 1 & 2\\
0 & 2 & -2 & 6\\
0 & 4 & 1 & 2
\end{bmatrix}
->
\begin{bmatrix}
1 & 2 & 1 & 2\\
0 & 2 & -2 & 6\\
0 & 0 & 5 & -10
\end{bmatrix}$$
$$
\begin{bmatrix}
2\\
6\\
-10
\end{bmatrix}
$$
is called vector c, which comes from vector b

*Ax=b -> Ux = c*
Ux = c would be easy to solve
Back Substitution: solve the equations in a reverse order

**Operation in Matrices Forms**
matrix * column = column, a combination of columns
row * matrix = row, a combination of rows

*What matrix will do 21-step: subtract 3 * row1 from row2?*
XA = B
'Cause we're keeping row1 and row2 unchanged,the first row of X will be 100 and the 3rd row 001, as we need 1 row1 to form the 1st row of the result and 1 row3 to form the 3rd row of the result.
the identity matrix:
$$
I = 
\begin{bmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{bmatrix}
$$
Now that we want 3*row1 to get subtracted off, we need to add -3 to the (2,1)index of the X, and then 1 at (2,2), 0 at (2,3) so that it adds up B as the result
X:
$$
X =
\begin{bmatrix}
1 & 0 & 0\\
-3 & 1 & 0\\
0 & 0 & 1
\end{bmatrix}
$$
the matrix is called E for elementary matrix or elimination matrix
$E_{21}$ for solving 21-step

Then 32-step:
$$
E_{32} =
\begin{bmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & -2 & 1
\end{bmatrix}
$$
$E_{32}(E_{21}A) = U$

Another type of elementary matrices which exchanges two rows: **permutation matrix**
Just do the same operation with I, get the P matrix
To exchange columns instead, right multiply the P matrix

**Row operations: multiply on the left**
**Column operations: multiply on the right**

**What matrix takes me from A to U, solving all the elimination in one shot?**
$(E_{32}E_{21})A = U$ move the parenthesis, but never change order