# Vectors

---

Tags: #mathematics #vectors 

## Vector Definition

Vectors have both *magnitude* and *direction*, which are features of a vector

One definition of a vector is a one-dimensional array.
Another is a directed line segment.

The Polar definition of a vector is a length and an angle. 

Vectors can either be column vectors:  $\vec v = \left [ \begin{matrix} 3 \\ 6 \end{matrix} \right ]$  or row vectors:  $\vec v = \left [ \begin{matrix} 3 & 6\end{matrix}\right ]$


The dimension of a vector is defined in $\Bbb R^n$ format, where $n$ is the dimension of the vector.

---

#### Unit Vectors

A vector is defined as a unit vector if the magnitude of the vector is equal to 1.
To normalize any vector, divide it by its magnitude.

Unit vectors are designated with a hat: 
$$
\hat v = \frac 1 {||\vec v||}\vec v
$$

---

#### Magnitude

The length of a vector, or the norm of a vector is the magnitude of the vector.

If the dimensions of the vectors are known, the formula for the magnitude of a vector is:
$$
||\vec v|| = \sqrt {\vec v\cdot\vec v}
$$

---
---

## Vector Operations

#### Distance Between Two Vectors

To find the distance between two vectors $\vec u$ and $\vec v$, use the following formula:
$$
dist(\vec u, \vec v) = || \vec u - \vec v || 
$$

---

#### Vector Addition and Subtraction

To add and subtract vectors, simply add each of the corresponding dimensions from each vector:

$$\left [ \begin{matrix} 1 \\ 2 \\ 3 \end{matrix} \right ] + \left [ \begin{matrix} 4\\5\\6\end{matrix} \right ] = \left [ \begin{matrix} 5\\7\\9\end{matrix} \right ]$$

Additionally, vectors can be added geometrically by putting the tail of one vector onto the head of another:

![[vectoraddition.png]]

**Algebraic Laws of Algebra Addition**:
1. $\vec u + \vec v = \vec v + \vec u$
2. $\vec u + 0 = \vec u$
3. $\vec u -\vec u = 0$
4. $c(\vec u + \vec v) = c\vec u + c\vec v$
5. $(c + d)\vec u = c\vec u + d\vec u$

---

#### Angle Between Two Vectors

To find the angle between any two vectors, use the following formula:
$$
\theta = \arccos(\frac{\vec v\cdot\vec u}{||\vec v||\space||\vec u||})
$$
Note that if that $\vec u\cdot \vec v = 0$, the two vectors are orthogonal to one another.

---

#### Vector Multiplication

###### Scalar Multiplication:

To multiply a vector by a scalar, just take each value of the vector and multiply it by the scalar:

$$2\cdot \left[\begin{matrix}4 \\ 3 \\ 5\end{matrix}\right] = \left [ \begin{matrix}8\\6\\10 \end{matrix}\right ]$$

Multiplying a vector with a vector is more complex than multiplying by a scalar.

###### Dot Product:

Provides a scalar from two vectors.
Measures how close the direction of the two vectors are to each other, or how close to parallel they are.

$$
\vec A \cdot \vec B = \vert \vec A \vert \cdot \vert \vec B \vert \cos \theta
$$

An additional way of calculating the dot product of two vectors is by taking the sum of each corresponding dimension multiplied together: 

$$
\left [ \begin{matrix} a\\b\\c\end{matrix} \right]\cdot \left [\begin{matrix}d\\e\\f \end{matrix}\right ] = ad + be + cf
$$

If the dot product of two vectors is equal to 0, this means that the vectors are perpendicular or orthogonal. 

Similarly, of the dot product of two vectors is equal to their magnitudes multiplied together, then they are parallel. 

Algebraic Laws of Dot Product:
1.  $\vec u\cdot \vec v = \vec v \cdot \vec u$
2. $(\vec u + \vec v) \cdot \vec w = \vec u\cdot \vec w + \vec v\cdot\vec w$
3. $(c\vec u)\cdot \vec v = c(\vec u\cdot\vec v) = \vec u\cdot (c\vec v)$
4. $\vec u\cdot\vec u \ge 0$
5. $\vec u = 0\Rightarrow \vec u\cdot\vec u = 0$

---

###### Cross Product:

$\vert \vec A \times \vec B \vert = \vert \vec A \vert \cdot \vert \vec B \vert \sin \theta$

or 

$\vec A = <a, b, c>$
$\vec B = <d, e, f>$
$$
\left [ \begin{matrix} a & b \\ c & d\end{matrix} \right ]
$$
$$
\vec A \times \vec B = \hat i (bf-ce) - \hat j (af - cd) + \hat k (ae-bd)
$$

-16i + 0j + 0k

-17.6i - 27.2j + 30k

---
---

## Orthogonal Projection

Orthogonal projection is when you project the component of one vector that matches the other vector: 

![[YBmT9-1981042009.png|400x300]]

The formula for calculating the orthogonal projection of $\vec x$ onto $\vec y$ is:
$$
proj_{\vec y}\space\vec x = \frac{\vec y\cdot\vec x}{\vec y\cdot\vec y}\vec y
$$

---
---

## Coded Example

```python
class Vector:
	def __init__(self, *values):
		self.values = values

	def magnitude(self):
		return math.sqrt(x ** 2 + y ** 2 + z ** 2)

	def add(self, vector):
		return Vector(self.x + vector.x)
```