# Notes for Lecture 1: The Geometry of Linear Equations

**Linear Algebra to solve what problems?**

n equations with n unknowns :

* Row picture
* Column picture

together making a matrix form

**Example:**

$$
\begin{bmatrix}
2&-1 \\
-1&2
\end{bmatrix}
\quad
\begin{bmatrix}
x\\
y
\end{bmatrix}
=
\begin{bmatrix}
0 \\
3
\end{bmatrix}
$$

as a matrix form of 2 equations and 2 unknowns

first matrix -> A
vector of unknowns -> **X**
right matrix -> b
A**X** = b

**Row picture：**
First equation(row) 2x - y = 0 can be viewed as a straight line in the xy plane going through the origin


Second equation(row) -x + 2y = 3 can be viewed as a straight line in the xy plane not going through the origin
The two lines meet at (1,2), which is the solution

**Column picture：**

$$
x
\begin{bmatrix}
2\\
-1
\end{bmatrix}
+y
\begin{bmatrix}
-1\\
2
\end{bmatrix}
=
\begin{bmatrix}
0 \\
3
\end{bmatrix}
$$

This means that the vector on the right can be expressed as a **linear combination** of the two columns in the matrix A, where x and y are the **coefficients**.

**Three dimension**

**Row picture:**
Each row is a plane in 3d space
two planes meet -> a line
3rd plane with the line -> a point, which is the solution

**Column picture:**

$$
x
\begin{bmatrix}
2\\
-1\\
0
\end{bmatrix}
+y
\begin{bmatrix}
-1\\
2\\
-3
\end{bmatrix}
+z
\begin{bmatrix}
0\\
-1\\
4
\end{bmatrix}
=
\begin{bmatrix}
1 \\
1\\   
3
\end{bmatrix}
$$

Linear combination of 3 vectors

**When will the 3 vectors not able to produce some b here?Can we always produce every b?**
any 2 columns happen to lie in the same plane, nothing new is contributed
Suppose we have 9 equations and 9 unknowns, we want to know if we can produce b by using 9 vectors' linear combination.
That is, in the 9-dimension space, whether we can find a linear combination of 9 vectors that can fill the whole 9d space.
*If any two of the 9 vectors happen to lie in the same 8d-plane in the 9d space, they give nothing new.*

**Matrix Form**
A*x* = b
How to multiply the matrix by the vector?
By row or by column
By column : viewed as a linear combination of A's columns
By row : row vector multiply column vector then adds up
