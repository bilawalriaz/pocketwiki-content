# Probability vector

A probability vector (also called a stochastic vector) is a vector whose entries are non-negative and sum to exactly one. Behind every probability vector sits an experiment that produces an outcome and a discrete random variable, a function that assigns a numerical value to each outcome. Rolling a die yields six outcomes, so a die's probability vector has six entries, one probability per face.

A probability vector of length $n$ gives the probability mass function of a random variable with $n$ possible values, the function that lists each value alongside its probability, and this is the standard description of a discrete probability distribution. The same vector can be written as a column or as a row.

## Examples

$$x_0 = \begin{bmatrix}0.5\\0.25\\0.25\end{bmatrix},\quad x_1 = \begin{bmatrix}0\\1\\0\end{bmatrix},\quad x_2 = \begin{bmatrix}0.65&0.35\end{bmatrix},\quad x_3 = \begin{bmatrix}0.3&0.5&0.07&0.1&0.03\end{bmatrix}$$

$x_1$ places all weight on a single outcome, the case of full certainty, while $x_0$ splits weight across three.

## Mean, length, and variance

Because the entries sum to 1, the mean of the components of any $n$-entry probability vector is $1/n$.

The variance $\sigma^2$ of the components satisfies

$$\sigma^2 \in \left[0,\ \frac{n-1}{n^2}\right].$$

The lower bound, zero variance, occurs when all entries equal $1/n$, which is the uniform distribution and the case of maximum uncertainty. The upper bound $(n-1)/n^2$ occurs when one entry equals 1 and the rest are 0, the case of full certainty. Because the upper bound shrinks as $n$ grows, the variance of any probability vector on $n$ outcomes shrinks toward zero in high dimensions. Analysts often bin outcomes into coarser categories to raise the variance and reveal structure hidden by fine granularity. The same drift toward uniformity with increasing $n$ underlies entropy in information theory and statistical mechanics.

The Euclidean length of a probability vector is tied to variance by

$$\|p\| = \sqrt{n\sigma^2 + \tfrac{1}{n}}.$$

Length is minimized at $1/\sqrt{n}$ when all entries equal $1/n$, the most uncertain vector, and reaches 1 when one entry equals 1 and the rest are 0, the most certain.

## The probability simplex

The set of all probability vectors of dimension $n$ forms the probability simplex, denoted $\Delta_{n-1}$:

$$\Delta_{n-1} = \{\,p \in \mathbb{R}^n \mid p_i \geq 0,\ \sum_{i=1}^n p_i = 1\,\}.$$

A simplex is the convex hull of $n$ affinely independent points, the smallest set of points that span a flat of dimension $n-1$ without redundancy: for $n=2$ a line segment, $n=3$ a triangle, $n=4$ a tetrahedron, and so on. The probability simplex uses the standard basis vectors $e_1, e_2, \dots, e_n$ as its vertices, each one a certain-outcome distribution.

Although the vectors live in $\mathbb{R}^n$, the simplex itself is $(n-1)$-dimensional, because the constraint $\sum p_i = 1$ removes one degree of freedom. It lies on the affine hyperplane whose normal vector is $a = (1, 1, \dots, 1)$, and every point of that hyperplane lies at perpendicular distance $1/\sqrt{n}$ from the origin.

The components $p_i$ act as barycentric coordinates, weights that locate a point inside a simplex by how much mass it assigns to each vertex, so each interior point of $\Delta_{n-1}$ represents a mixture over the $n$ outcomes and each vertex a single certain outcome. Every discrete distribution on $n$ outcomes corresponds to exactly one point in $\Delta_{n-1}$, and vice versa. Any other simplex in $\mathbb{R}^n$ can be obtained from $\Delta_{n-1}$ by an affine transformation, making it the canonical reference simplex.

The simplex has sharp vertices, straight edges, and flat faces, not a smooth surface. Assigning a zero probability to an outcome moves the point onto a lower-dimensional face, since that outcome is no longer possible. Adding one new possible outcome raises $n$ by one and adds a new vertex; connecting that vertex to every face of the old simplex produces the facets of the higher-dimensional simplex, so a triangle with a new vertex becomes a tetrahedron.

The centroid $u = (1/n, \dots, 1/n)$, which encodes the uniform distribution, has Euclidean length $\|u\| = 1/\sqrt{n}$ from the origin, since the line from the origin to the centroid coincides with the simplex's normal. Each vertex lies at Euclidean distance $\sqrt{(n-1)/n}$ from the centroid.

The simplex occupies a thin $(n-1)$-dimensional slice of the $n$-dimensional unit hypercube at perpendicular distance $1/\sqrt{n}$ from the origin. Its $(n-1)$-dimensional content is

$$V_{n-1} = \frac{\sqrt{n}}{(n-1)!},$$

obtained by taking $e_n$ as a base point, forming edge vectors $v_i = e_i - e_n$, and computing the Gram matrix $G_{ij} = v_i \cdot v_j$ with determinant $n$, then dividing the parallelepiped content $\sqrt{\det G}$ by $(n-1)!$. Because $V_{n-1}$ shrinks factorially as $n$ grows while the enclosing unit hypercube keeps unit volume, the fraction of the hypercube occupied by the simplex becomes super-exponentially small in high dimensions.
