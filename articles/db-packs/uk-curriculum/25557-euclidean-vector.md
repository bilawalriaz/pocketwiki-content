# Euclidean vector

A Euclidean vector is a geometric object with magnitude (length) and direction. It is drawn as an arrow from an initial point *A* to a terminal point *B*, denoted $\overrightarrow{AB}$. The magnitude is the distance between the points; the direction is the displacement from *A* to *B*. Vectors can be added and scaled, forming a vector space. In physics they represent quantities like velocity, force, and acceleration—anything with magnitude and direction that obeys vector addition.

## Bound and free vectors

A **bound vector** has a fixed initial point. A **free vector** is an equivalence class of all directed segments with the same magnitude and direction; two arrows represent the same free vector if they are equipollent (form a parallelogram). In a space with a chosen origin, every free vector corresponds to a unique bound vector starting at that origin. Mechanics distinguishes them: a force is a bound vector because its point of application matters; velocity is free.

## Coordinate representation

Choose an origin *O* and an orthonormal basis $\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3$ (unit vectors along perpendicular axes). Any vector $\mathbf{a}$ becomes a triple of scalar components:
$$\mathbf{a} = a_1\mathbf{e}_1 + a_2\mathbf{e}_2 + a_3\mathbf{e}_3 = (a_1, a_2, a_3).$$
In physics the basis is often written $\mathbf{i}, \mathbf{j}, \mathbf{k}$ or $\hat{\mathbf{x}}, \hat{\mathbf{y}}, \hat{\mathbf{z}}$. The components are the projections onto the axes. This representation turns geometric operations into arithmetic on components.

## Basic operations

**Equality**: $\mathbf{a} = \mathbf{b}$ iff $a_1=b_1, a_2=b_2, a_3=b_3$.

**Addition**: $\mathbf{a}+\mathbf{b} = (a_1+b_1, a_2+b_2, a_3+b_3)$. Geometrically, place the tail of $\mathbf{b}$ at the head of $\mathbf{a}$; the sum is the arrow from the tail of $\mathbf{a}$ to the head of $\mathbf{b}$ (parallelogram rule). Addition is commutative and associative.

**Subtraction**: $\mathbf{a}-\mathbf{b} = (a_1-b_1, a_2-b_2, a_3-b_3)$. Draw both from the same point; the difference is the arrow from the head of $\mathbf{b}$ to the head of $\mathbf{a}$.

**Scalar multiplication**: $r\mathbf{a} = (ra_1, ra_2, ra_3)$. The vector stretches by factor $|r|$; if $r<0$ it reverses direction. Scalar multiplication distributes over addition: $r(\mathbf{a}+\mathbf{b}) = r\mathbf{a}+r\mathbf{b}$.

**Length (magnitude, norm)**:
$$\|\mathbf{a}\| = \sqrt{a_1^2 + a_2^2 + a_3^2} = \sqrt{\mathbf{a}\cdot\mathbf{a}},$$
from the Pythagorean theorem (basis vectors are orthogonal unit vectors).

**Unit vector**: $\hat{\mathbf{a}} = \mathbf{a}/\|\mathbf{a}\|$ (undefined for the zero vector $\mathbf{0}=(0,0,0)$). Unit vectors indicate pure direction.

**Zero vector**: $\mathbf{0}$ has length zero, arbitrary direction, and acts as the additive identity.

## Dot product

The dot product (scalar product, inner product) returns a scalar:
$$\mathbf{a}\cdot\mathbf{b} = \|\mathbf{a}\|\|\mathbf{b}\|\cos\theta = a_1b_1 + a_2b_2 + a_3b_3,$$
where $\theta$ is the angle between the vectors when drawn from a common start. Geometrically, it is the length of $\mathbf{a}$ times the projection of $\mathbf{b}$ onto $\mathbf{a}$. It vanishes iff the vectors are orthogonal. The dot product defines both angle and length in any dimension.

## Cross product

The cross product (vector product) exists only in three and seven dimensions. In $\mathbb{R}^3$:
$$\mathbf{a}\times\mathbf{b} = \|\mathbf{a}\|\|\mathbf{b}\|\sin\theta\,\mathbf{n},$$
where $\mathbf{n}$ is a unit vector perpendicular to both $\mathbf{a}$ and $\mathbf{b}$ chosen by the **right-hand rule** (curl fingers from $\mathbf{a}$ to $\mathbf{b}$; thumb gives $\mathbf{n}$). In components:
$$\mathbf{a}\times\mathbf{b} = (a_2b_3-a_3b_2)\mathbf{e}_1 + (a_3b_1-a_1b_3)\mathbf{e}_2 + (a_1b_2-a_2b_1)\mathbf{e}_3.$$
The result is a vector orthogonal to the plane of $\mathbf{a}$ and $\mathbf{b}$. Its magnitude equals the area of the parallelogram spanned by them. The cross product is anti-commutative: $\mathbf{a}\times\mathbf{b} = -\mathbf{b}\times\mathbf{a}$.

## Scalar triple product

$(\mathbf{a}\ \mathbf{b}\ \mathbf{c}) = \mathbf{a}\cdot(\mathbf{b}\times\mathbf{c})$. Its absolute value is the volume of the parallelepiped with edges $\mathbf{a}, \mathbf{b}, \mathbf{c}$. It is zero iff the three vectors are linearly dependent (lie in one plane). In a right-handed orthonormal basis it equals the determinant of the $3\times3$ matrix with the vectors as rows.

## Changing basis

A vector is the same geometric object in any basis. If $\{\mathbf{e}_k\}$ and $\{\mathbf{n}_j\}$ are two orthonormal bases, the components transform via a **direction cosine matrix** (rotation matrix) $C$ where $c_{jk} = \mathbf{n}_j\cdot\mathbf{e}_k = \cos\angle(\mathbf{n}_j,\mathbf{e}_k)$:
$$\begin{bmatrix}u\\v\\w\end{bmatrix} = C\begin{bmatrix}p\\q\\r\end{bmatrix}.$$
$C$ is orthogonal: $C^{-1}=C^\top$, $\det C = 1$. Components transform *contravariantly* (opposite to the basis rotation) so the vector itself stays fixed. This contravariance captures the physical idea that a vector has magnitude and direction independent of coordinates.

## Physics: vectors, pseudovectors, and calculus

Position $\mathbf{x}$, displacement $\mathbf{y}-\mathbf{x}$, velocity $\mathbf{v} = d\mathbf{x}/dt$, and acceleration $\mathbf{a} = d\mathbf{v}/dt$ are vectors. Force $\mathbf{F} = m\mathbf{a}$ (Newton's second law). Work $W = \mathbf{F}\cdot(\mathbf{x}_2-\mathbf{x}_1)$. Vector-valued functions are differentiated and integrated component-wise.

Under a mirror reflection (orientation reversal), most vectors (displacement, velocity, force) transform like the coordinates—they are **polar vectors** (true vectors). Some, like angular velocity, magnetic field, and torque, gain an extra minus sign; these are **pseudovectors** (axial vectors). Pseudovectors arise as cross products of polar vectors. The distinction matters for symmetry analysis.

## Generalizations

The algebraic rules (addition, scaling, dot product) generalize to $\mathbb{R}^n$ and abstract vector spaces. The cross product does not; its higher-dimensional analogue is the exterior product, yielding bivectors. In a pseudo-Euclidean space (e.g., Minkowski space of special relativity) the squared length can be negative. In thermodynamics and other fields, vectors live in spaces without a natural length or angle: affine spaces for bound vectors, vector spaces for free vectors. A vector is a rank-1 contravariant tensor; tensors generalize the transformation behavior to higher ranks.