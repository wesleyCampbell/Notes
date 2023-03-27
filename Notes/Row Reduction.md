[[Header Pages/Linear Algebra|Back to Linear Algebra]]

# Row Reduction

---

Tags: #mathematics 

---

## Systems of Equations

A linear equation is defined as:
$$
c_0x_0 + \dots + c_nx_n = b
$$
where coefficients $c_0\dots c_n$ are any value in $\Bbb R$.

We can express a system of such equations such as :
$$
\begin{equation}
\begin{cases}
ax + by + cz = d\\
ex + fy + gz = h\\
ix + jy + kz = l
\end{cases}
\end{equation}
$$
In terms of an augmented matrix where the columns align with the variables and the rows align with the equations:
$$
\left [ \begin{array}{ccc|r}
a & b & c & d\\
e & f & g & h\\
i & j & k & l
\end{array}\right ]
$$

---

#### Consistency

A system of equations can either be consistent or inconsistent. 

A consistent solution has at least one solution:
- One unique solution
- Infinitely many solutions

An inconsistent system has no solution.

---

#### Homogeneous System

A system of equations is defined as homogeneous if all the equations are equal to 0.
With $A$ being a matrix with dimensions mxn, a homogenous system can be represented with the expression $\left[\begin{array}{r|r}A&0\end{array}\right]$.

An example of an Homogeneous System:
$$
\left[\begin{array}{rrr|r}
3 & 5 & -4 & 0\\
-3 & -2 & 4 & 0\\
6 & 1 & -1 & 0
\end{array}\right]
$$

A homogeneous system has at least one solution: $\vec x = 0$, or the trivial solution.

$\left[\begin{array}{r|r}A&0\end{array}\right]$ has a nontrivial solution if and only if $A$ has at least one free variable.

---
---

## Back Substitution

In the case of a triangular system of equations such as:
$$
\begin{equation}
\begin{cases}
x - y - z = 2\\
y + 3z = 5\\
5z = 10
\end{cases}
\end{equation}
$$
we can utilize back substitution to find the value of z, use that to find the value of y, and then use those to values to find the value of x.

---
---

## Row Echelon Form

In row echelon form, an augmented matrix follows the following rules:
1. All rows consisting entirely of zeros are at the bottom
2. Each leading entry of a row is in a column to the right of the leading entry of the rows above (forms a triangle)

An example of a matrix in Row Echelon Form:
$$
\left[\begin{array}{ccc|c}
3 & 2 & 1 & 4\\
0 & -4 & 4 & -10\\
0 & 0 & 3 & 4
\end{array}\right ]
$$

###### Rank
- The number of nonzero rows in the row echelon form of a matrix is called the rank of the matrix
- The rank is equal to the number of columns - the number of free variables

---
---

### Reduced Row Echelon Form

All matrixes in Reduced Row Echelon Form are also in Row Echelon Form.

In Reduced Row Echelon Form, an augmented matrix follows the following rules:
1. All rows consisting entirely of zeros are at the bottom
2. Each leading entry of a row is in a column to the right of the leading entry of the rows above
3. The leading entry in each nonzero row is 1
4. Each leading 1 is the only nonzero entry in its column

An example of a matrix in Row Echelon Form:
$$
\left[\begin{array}{rrr|r}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 3\\
0 & 0 & 0 & 0
\end{array}\right]
$$

###### Pivot Position:
- A position in a matrix that corresponds to a leading 1 in the Reduced Row Echelon form of A

###### Pivot Column:
- A column of a matrix that contains a pivot position
- The number of pivot columns are equal to the number of leading variable

###### Leading vs. Free Variables:
- Leading variables are the number variables that can be solved
- Free variables are variables that cannot be solved and correspond to parameters
- If a matrix has the same number of free variables as columns, there is a unique solution to the matrix. 
- If there is not the same number of free variables as columns, there is not a unique solution to the matrix

---
---

### Elementary Row Operations

There are three operations that we can perform on an augmented matrix without changing the solution of the corresponding system:
1. Interchange two rows ($R_1\rightleftarrows R_2$)
2. Multiply all entries in a row by a nonzero scalar ($c \cdot R_1$)
3. Add a scalar multiplied by a row to another row ($R_1 += c\cdot R_2$)

Two matrices that can be joined by a sequence of elementary row operations are called row equivalent and will have the same solution.

---
---

## Gaussian Elimination

A process of solving a system of equations by using an augmented matrix.

To find the solution of a matrix, transform an augmented matrix to its equivalent row echelon form.

Using the row echelon form of the matrix, use back substitution to solve the system of equations.

---
---

## Gauss-Jordan Elimination

A process of solving a system of equations by using an augmented matrix.

To find the solution of an augmented matrix, transform it to its reduced row echelon form.

Take the values from row echelon form to solve the system of equations.

---
---

