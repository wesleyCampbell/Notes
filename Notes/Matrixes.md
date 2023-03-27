[[Header Pages/Linear Algebra|Back to Linear Algebra]]

# Matrixes

---

Tags: #mathematics 

---

## Definition

A matrix is a rectangular array of numbers called the entries or elements of the matrix.

Values are stored at specific indexes.

A matrix is $m\times n$ if it has $m$ rows and $n$ columns:
$$
\left[\begin{matrix}
a_{0,0} & a_{0, 1} & \dots & a_{0, n}\\
a_{1, 0} & a_{1, 1} & \dots & a_{1, n}\\
a{2, 0} & a_{2, 1} & \dots & a_{2, n}\\
\vdots & \vdots & \ddots & \cdots\\
a_{m, 0} & a_{m, 1} & \dots & a_{m, n}
\end{matrix}\right]
$$

We can also write a matrix in column form:
$$
A = \left[\begin{matrix}\vec a_0&\vec a_1&\dots&\vec a_n\end{matrix}\right]
$$

or in row form:
$$
A = \left[\begin{matrix}\vec A_0\\\vec A_1\\\vdots\\\vec A_m\end{matrix}\right]
$$

###### Diagonal Matrix:
- A diagonal matrix is defined as a matrix where the only nonzero values are on the diagonal
- More formally, the only nonzero values in the matrix are $a_{i, i}$

---
---

## Matrix Operations

#### Matrix Addition

To add two matrices together, they must be of the same dimensions. 

To find the result, you simply add together each corresponding index from the two matrices:
$$
\left[\begin{matrix}1&0\\2&3\end{matrix}\right] + \left[\begin{matrix}1&2\\-3&4\end{matrix}\right] = \left[\begin{matrix}2&2\\-1&7\end{matrix}\right]
$$

A formal definition: 
$$A = \left[\begin{matrix}\vec a_0&\dots&\vec a_n\end{matrix}\right]$$
$$B = \left[\begin{matrix}\vec b_0&\dots&\vec b_n\end{matrix}\right]$$
$$
A + B = \left[\begin{matrix}\vec a_0 + \vec b_0&\dots&\vec a_n + \vec b_n\end{matrix}\right]
$$

---

#### Transpose

To take the transpose of a matrix, take the rows of the matrix and turn them into the columns.

More formally:
$$
A = \left[\begin{matrix}\vec a_0&\dots\vec a_n\end{matrix}\right]
$$
$$
A^T = \left[\begin{matrix}\vec a_0\\\vdots\\\vec a_n\end{matrix}\right]
$$

###### Symmetrical Matrices:
- A matrix is defined as symmetrical if $A=A^T$
- Only square matrices can be symmetrical

---

#### Matrix Multiplication 

###### Scalar Multiplication

When multiplying a scalar by a vector, the resulting matrix can be found by the following equation:
$$
c\left[\begin{matrix}\vec a_0&\dots&\vec a_n\end{matrix}\right] = \left[\begin{matrix}c\space\vec a_0&\dots&c\space\vec a_n\end{matrix}\right]
$$

###### Matrix Multiplication

To multiply two matrices together, they must have the correct dimensions. To multiply any two matrices, they must have the dimensions $a\times b$ and $b\times c$, where $a, b, c$ are any value in $\Bbb C$.

Put another way, to multiply two matrices, the column count of the first matrix must equal the number of rows of the second matrix.

Note that matrix multiplication doe not follow the associative property of scalar multiplication. Order does matter: $A\cdot B \not= B\cdot A$ for most cases.

Note that you can define the dot product using matrix multiplication:
$$
\vec u\cdot\vec v = \vec u^T\space\vec v
$$

The definition of matrix multiplication is as follows, assuming matrix A has dimensions $m\times n$ and matrix B has dimensions of $n\times r$
$$
A\space B = \left[\begin{matrix}
\vec A_0\cdot\vec b_0 & \vec A_0\cdot\vec b_1&\dots&\vec A_0\cdot\vec b_r\\
\vec A_1\cdot\vec b_0 & \vec A_1\cdot\vec b_1&\dots&\vec A_1\cdot\vec b_r\\
\vdots&\vdots&\ddots&\vdots\\
\vec A_m\cdot\vec b_0 & \vec A_m\cdot\vec b_1&\dots&\vec A_m\cdot\vec b_r
\end{matrix}\right]
$$

Additionally, you can use the following definition:
$$
A\space B = A\left[\begin{matrix}\vec b_0&\dots&\vec b_r\end{matrix}\right] = \left[\begin{matrix}A\vec b_0&\dots&A\vec b_r\end{matrix}\right]
$$

Note that $A_i$ is the ith *row* vector of matrix $A$ and $b_i$ is the ith *column* vector of matrix $B$.

###### Matrix Powers

You can only find the power of a square matrix, as the dimensions would not align.

For any matrix A that is $n\times n$, as long as $k\ge0$, you simply multiply 1 by $A$, $k$ times.

---

### Matrix Algebra

You need to make sure that you preserve the multiplication order when performing matrix algebra.
Because $A\space B \not=B\space A$, you need to make sure not to multiply the wring side of the equation.

$$
A(B + C) = AB + AC
$$
$$
(B + C)A = BA + CA
$$

If you have a matrix equation and you multiply both sides by a matrix, you must multiply both sides on the *left* by the matrix **or** both sides on the *right* by the matrix. 

---
---

## Identity Matrix

An $n\times n$ matrix of the form $I_n=\left[\begin{matrix}1&0&\dots&0\\
0&1&\dots&0\\
\vdots&\vdots&\ddots&\vdots\\
0&0&\dots&1\end{matrix}\right]$ is called the $n\times n$ identity matrix.

The columns of $I_n$ are called the standard unit vectors:
$$
e_0 = \left[\begin{matrix}1\\0\\0\\\vdots\\0\end{matrix}\right]\quad\space\quad
e_1 = \left[\begin{matrix}0\\1\\0\\\vdots\\0\end{matrix}\right]
$$

#### Elementary Matrices

An elementary matrix is a matrix by performing a single row operation on the identity matrix $I$.
For example, the following are elementary matrices:
$$
E_1=\left[\begin{matrix}1&0&0\\0&1&0\\4&0&1\end{matrix}\right],\quad  E_2=\left[\begin{matrix}0&1&0\\1&0&0\\0&0&1\end{matrix}\right],\quad 
E_3=\left[\begin{matrix}1&0&0\\0&1&0\\0&0&5\end{matrix}\right]
$$

All elementary matrices are invertible.

---
---

## Matrix Inverses

An $n\times n$ matrix $A$ is said to be *invertible* if there is a $n\times n$ matrix $C$ such that $A\space C=I$ and $C\space A=I$.

Although we cannot divide by a matrix, we can multiply by the inverse of a matrix.
Only square matrices can be invertible.

Matrix inverses are invaluable in solving equations with matrices in them.

The inverse of a $2\times2$ matrix $A = \left[\begin{matrix}a&b\\c&d\end{matrix}\right]$ can be found with the following equation:
$$
A^{-1} = \frac1{a\space d-b\space c}\left[\begin{matrix}d&-b\\-c&a\end{matrix}\right]
$$

However, to find the inverse of an $n\times n$ matrix $A$, we can use row reduction to solve the following system:$$\left[\begin{array}{r|r}A&I\end{array}\right]$$
If the system is consistent, there is an inverse for matrix $A$, otherwise there is not.

Note that there are a large number of [[Fundamental Theorem of Invertible Matrices|properties]] of inverse matrices.

---
---