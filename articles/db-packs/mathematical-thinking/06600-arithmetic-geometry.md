# Arithmetic geometry

Arithmetic geometry is the part of mathematics that uses the methods of algebraic geometry to study problems in number theory. It centers on **Diophantine geometry**, which asks for the rational points, meaning the solutions in rational numbers, of systems of polynomial equations. The equations define shapes called algebraic varieties, and arithmetic geometry studies those shapes and counts or classifies their rational points.

A classical example is the hyperelliptic curve $y^2 = x(x+1)(x-3)(x+2)(x-2)$. Faltings' theorem states that any algebraic curve of genus greater than 1 has only finitely many rational points; the points $(-2,0)$ and $(-1,0)$ are two such points on this curve. Proved by Gerd Faltings in 1983, the same theorem settled the Mordell conjecture and is strictly stronger than the older Mordell–Weil theorem, which only guarantees that the rational points on an abelian variety form a *finitely generated* group.

More abstractly, arithmetic geometry is the study of *schemes of finite type* over the spectrum of the ring of integers, the framework in which the usual geometric language of varieties is adapted to integer-valued arithmetic.

## The objects: rational points and their fields

The rational points of interest are solutions of polynomial equations defined not only over the rationals but over several kinds of fields that are not algebraically closed: **number fields** (finite extensions of the rationals), **finite fields** (used to encode discrete arithmetic), ***p*-adic fields** (completions of the rationals at a prime *p* that give a notion of closeness based on divisibility), and **function fields** (analogues of number fields coming from curves). The real numbers are excluded from this framework. A **height function** attached to a point measures its arithmetic complexity and lets mathematicians compare solutions across examples.

Two tools give these varieties their modern structure: **étale cohomology**, a topological invariant for varieties over finite fields built from algebraic rather than continuous data; and ***p*-adic Hodge theory**, which studies when cohomological features of a complex variety extend to its *p*-adic counterpart.

## A short history

**Nineteenth-century origins.** Carl Friedrich Gauss observed that a homogeneous polynomial equation with rational coefficients has a non-zero integer solution whenever it has a non-zero rational solution. In the 1850s, Leopold Kronecker formulated the Kronecker–Weber theorem, introduced the theory of divisors, and built explicit bridges between number theory and algebra. His "dearest dream of youth" (*liebster Jugendtraum*) became Hilbert's twelfth problem, which proposes recasting number theory inside quotient rings of polynomial rings over the integers.

**Modern foundations.** In the late 1920s, André Weil's doctoral work led to the Mordell–Weil theorem. Foundations of algebraic geometry were rebuilt in the 1930s and 1940s by Oscar Zariski and others, drawing on valuation theory and ideal theory from commutative algebra. In 1949, Weil posed the Weil conjectures about local zeta-functions of varieties over finite fields, a package of four statements linking arithmetic counts to topological data. This framework drove Alexander Grothendieck, together with Jean-Pierre Serre, Michael Artin, and Jean-Louis Verdier, to recast algebraic geometry using sheaf theory and then scheme theory in the 1950s and 1960s. Bernard Dwork proved the rationality of the local zeta function in 1960, Grothendieck and his collaborators used étale cohomology to prove two further Weil conjectures by 1965, and Pierre Deligne closed the package in 1974 with the analogue of the Riemann hypothesis.

**Modularity and elliptic curves.** Between 1956 and 1957, Yutaka Taniyama and Goro Shimura proposed the conjecture, now the modularity theorem, that every elliptic curve is attached to a modular form. Andrew Wiles used modularity lifting to prove Fermat's Last Theorem in 1995. In the 1960s, Shimura introduced **Shimura varieties**, generalisations of modular curves that have since served as a natural source of examples for the Langlands program.

**Finiteness results.** In 1977–1978, Barry Mazur proved the torsion conjecture, listing every possible torsion subgroup of an elliptic curve over the rationals; Loïc Merel extended the result to all number fields in 1996. Faltings's 1983 theorem that any curve of genus greater than 1 has only finitely many rational points remains the central finiteness result of the subject.

**Twenty-first century.** In 2001, proofs of the local Langlands conjectures for $\mathrm{GL}_n$ relied on the geometry of certain Shimura varieties. In the 2010s, Peter Scholze introduced **perfectoid spaces** and new cohomology theories for working over *p*-adic fields, with applications to Galois representations and to parts of the weight-monodromy conjecture.

Source: adapted from "Arithmetic geometry" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Arithmetic_geometry
