[[Header Pages/Linear Algebra|Back to Linear Algebra]]

# Spanning Sets and Linear Independence

---

Tags: #mathematics 

---

## Linear Combinations

Given vectors $\vec v_0\dots\vec v_n$ and scalars $c_0\dots c_1$, a vector that is in the form: 
$$\vec y = c_0\vec v_0\dots c_n\vec v_n$$
is called a linear combination of the vectors $\vec v_0\dots\vec v_n$.

To determine whether a vector $\vec b$ is a linear combination of a set of other vectors $\{\vec v_0\dots\vec v_n\}$ , we can use an augmented matrix. If the system is inconsistent, the vector is not a linear combination of the set:
$$
\left[\begin{array}{rrr|r}
\vec v_0 & \dots & v_n & \vec b
\end{array}\right]
$$

---
---

## Spans of Vectors Sets

A span of a set of vectors, written $Span\{\vec v_0\dots\vec v_n\}$, is the set of all vectors that can be written as linear combinations of $\vec v_0\dots\vec v_n$ for any coefficients $c_0\dots c_n$ which can be any value in $\Bbb R$.

---
---

## Linear Independence

A set of vectors $\{\vec v_0\dots\vec v_n\}$ is said to be linearly independent if the only coefficients $c_0\dots c_n$ which satisfy the equation 
$$
c_0\vec v_0 + \dots + c_n\vec v_n = 0
$$
are when all of the coefficients are equal to zero.

That is, all of the vectors do not share the same direction in any dimension.

To determine whether a set of vectors are linearly independent, determine if the following system is consistent or inconsistent:
$$
\left[\begin{array}{rrr|r}
\vec v_0 & \dots & \vec v_n & 0
\end{array}\right]
$$
If the system is consistent, then the set of vectors are linearly independent. Otherwise, they are not.

If you let $\vec v_0\dots\vec v_n$ be vectors in $\Bbb R^n$, then all of the following statements are either **all true** or **all false**:
1. The vectors $\vec v_0\dots\vec v_n$ are linearly independent
2. The system $\left[\begin{array}{rrr|r}\vec v_0 & \dots & \vec v_n & 0\end{array}\right]$ has *only* the trivial solution
3. A Reduced Echelon Form of $\left[\begin{array}\vec v_0 & \dots & \vec v_n\end{array}\right]$ has a pivot position in every column
	-  There are no free variables
4. For every $\vec b$ in $\Bbb R^n$ the system $\left[\begin{array}{rrr|r}\vec v_0&\dots&\vec v_n&0\end{array}\right]$ has at most one solution.

---

#### Dependence Relations

If a set of vectors is linearly dependent, we can write a dependence relation for the set.

In a dependence relation, we provide an example of coefficients that show that the trivial solution is not the only solution that results in a homogenous system.

An example of a dependence relation for a set of 3 vectors in $\Bbb R^2$:
$$
1\left[\begin{matrix}0\\1\end{matrix}\right] + 1\left[\begin{matrix}1\\0\end{matrix}\right] - 1\left[\begin{matrix}1\\1\end{matrix}\right] = \left[\begin{matrix}0\\0\end{matrix}\right]
$$

A dependence relation is just an example of one out of infinitely many solutions.