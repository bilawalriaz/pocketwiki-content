# Vector calculus

Vector calculus is the mathematics of differentiation and integration applied to vector fields, primarily in three-dimensional Euclidean space ℝ³. It overlaps with multivariable calculus, which also covers partial differentiation and multiple integration. The subject underlies differential geometry, partial differential equations, and much of physics and engineering, including the description of electromagnetic fields, gravitational fields, and fluid flow.

## Origins

Vector calculus was developed from the theory of quaternions by J. Willard Gibbs and Oliver Heaviside in the late 19th century. Most of the notation and terminology still in use was fixed by Gibbs and Edwin Bidwell Wilson in their 1901 book *Vector Analysis*. Isaac Newton's earlier work on the geometry of curves and motion anticipated many of its ideas. In its standard form using the cross product, the subject does not generalize cleanly to dimensions higher than three; geometric algebra, based on the exterior product, does.

## Scalar and vector fields

A scalar field smoothly assigns a number to every point in space; temperature, pressure, and the Higgs field are standard examples. A vector field smoothly assigns a vector to each point and can be visualized as a collection of arrows whose magnitude and direction vary with position. Wind velocity, magnetic force, and gravitational force are all modelled as vector fields.

A pseudovector field looks identical to an ordinary vector field but changes sign under an orientation-reversing map. The curl of a vector field is the most familiar pseudovector field: reflecting a vector field reverses the sign of its curl.

## Vector algebra

The non-differential operations used throughout the subject are called vector algebra. The basic operations are vector addition, scalar multiplication, the dot product (which returns a scalar), and the cross product of two vectors in ℝ³ (which returns a pseudovector). The scalar triple product **v**₁·(**v**₂×**v**₃) and the vector triple product **v**₁×(**v**₂×**v**₃) are built from these.

## Differential operators

The core of vector calculus is a small family of differential operators built from the del operator ∇. On a scalar field *f* and a vector field **F**:

- **Gradient** ∇*f*: the rate and direction of steepest change of a scalar field. Maps scalars to vectors.
- **Divergence** ∇·**F**: a scalar measuring the local source or sink strength of a vector field. Maps vectors to scalars.
- **Curl** ∇×**F**: a pseudovector measuring the local rotational tendency of a vector field in ℝ³. Maps vectors to pseudovectors.
- **Laplacian** ∇²*f* = ∇·∇*f*: the difference between the value of a field at a point and its average over infinitesimal balls around it. A vector Laplacian ∇²**F** = ∇(∇·**F**) − ∇×(∇×**F**) acts on vector fields.

These operators obey identities that resemble the algebraic identities for multiplication, which is why the notation ∇*f*, ∇·**F**, ∇×**F** works.

## Integral theorems

The three core operators each come with a fundamental theorem that generalizes the one-dimensional fundamental theorem of calculus to higher dimensions:

- **Gradient theorem.** The line integral of ∇φ along a curve from *p* to *q* equals φ(*q*) − φ(*p*).
- **Divergence theorem.** The volume integral of ∇·**F** over a solid *V* equals the flux of **F** through the closed boundary surface ∂*V*.
- **Stokes' theorem.** The surface integral of ∇×**F** over a surface Σ equals the line integral of **F** around the closed boundary curve ∂Σ.

In two dimensions the divergence and curl theorems collapse to Green's theorem.

## Applications

For a differentiable scalar function *f*(*x*, *y*), the linear approximation
*f*(*x*, *y*) ≈ *f*(*a*, *b*) + ∂*f*/∂*x*(*a*, *b*)(*x*−*a*) + ∂*f*/∂*y*(*a*, *b*)(*y*−*b*)
gives the equation of the tangent plane to the graph at (*a*, *b*). Local maxima and minima of a smooth function of several variables occur at points where the gradient vanishes; classifying a critical point as a maximum, minimum, or saddle point requires examining the eigenvalues of the Hessian matrix of second partial derivatives.

## Generalizations

The gradient and divergence, together with their integral theorems and the Laplacian, generalize to any dimension. The curl and cross product do not: the curl of a vector field is a vector field only in dimensions 3 and 7 (and trivially in dimensions 0 and 1), and the same dimensions are the only ones admitting a binary cross product. Vector calculus extends to any three-dimensional oriented Riemannian manifold, where the tangent space at each point carries an inner product and an orientation.

Two modern frameworks subsume vector calculus. Geometric algebra replaces vector fields with *k*-vector fields and the cross product with the exterior product, which is defined in every dimension. Differential forms replace vector fields with *k*-covector fields; from this viewpoint grad, curl, and div are special cases of the exterior derivative of 0-forms, 1-forms, and 2-forms, and the gradient, divergence, Stokes', and Green's theorems all become instances of a single general Stokes' theorem. Both frameworks reveal that standard vector calculus implicitly identifies mathematically distinct objects, which keeps its notation compact but obscures the underlying structure.

Source: adapted from "Vector calculus" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Vector_calculus
