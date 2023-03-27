[[Header Pages/Linear Algebra|Back to Linear Algebra]]

# Subspaces and Row-Column Space

---

Tags: #mathematics 

---

## Subspaces

#### Definition

A subspace of $\Bbb R^n$ is any collection of vectors in $\Bbb R^n$ such that:
1. The zero vector **0** is in S
2. If $\vec u$ and $\vec v$ are in S, then $\vec u+\vec v$ is in S (S is closed under vector addition)
3. If $\vec u$ is in S, and $c$ is a scalar, then $c\vec u$ is in S (S is closed under scalar multiplication)

If a subset of $R^n$ is a subspace, then all three statements above will be true. 
If one statement is false, then the subset is not a subset.

---

#### Examples of Subspaces

All lines and planes passing through the origin are subspaces.

All [[Spanning Sets and Linear Independence#Spans of Vectors Sets|spans]] for vectors $\vec v_0\dots\vec v_p$ in $\Bbb R^n$ are subspaces.

---
---

## Row-Column Space

#### Definition

Given a $m\times n$ matrix $A$: 
1. The *row space* of the $A$, $Row(A)$, is the subspace of $\Bbb R^n$ spanned by the rows of $A$
2. The *column space* of $A$, $Col(A)$, is the subspace of $\Bbb R^n$ spanned by the rows of $A$

Symbolically:
$$
Row(A) = Span\{\vec A_1\dots\vec A_m\}
$$
$$
Col(A) = Span\{\vec a_1\dots\vec a_n\}
$$


---
---

## Basis of a Subspace

A basis for a subspace $S$ of $\Bbb R^n$ is a set of vectors $\{\vec b_1\dots\vec b_n\}$ such that:
1. $\{\vec b_1\dots\vec b_n\}$ is linearly independent
2. and S = $span\{\vec b_1\dots\vec b_n\}$

The basis of a subspace is a collection of vectors that are linearly independent and that span the subspace. 

###### Find Basis of Row Space
1. Row reduce row vectors
2. The non-zero row vectors are the basis of the row space

###### Find the Basis of Column Space
1. Row reduce column vectors
2. Take the pivot columns of the initial matrix as the basis

###### Find the Basis of Null Space
1. Find the solutions of $A\space\vec x = \vec0$
2. Express them in vector form
3. Take those vectors as the basis


---
---

## Null Space

The null space of a matrix $A$ is the set of all solutions of the homogeneous equation $A\space x = \vec 0$

The null space is a subspace.