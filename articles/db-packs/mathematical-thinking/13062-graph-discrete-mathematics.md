# Graph (discrete mathematics)

A graph is a structure made of two sets: a set of **vertices** (also called nodes or points) and a set of **edges** connecting pairs of them. Each edge is a relationship between two vertices, drawn as dots joined by lines. If two people at a party shake hands, draw a dot for each person and a line between every pair that shook hands; the result is a graph. If instead one person owes money to another, draw an arrow from debtor to creditor; the result is a *directed graph* (or digraph), because the relationship runs one way.

Graphs are the basic object of study in graph theory, a branch of discrete mathematics. The term "graph" in this sense was introduced by J. J. Sylvester in 1878, drawn by analogy to the chemical-structure diagrams (Kekulé "chemico-graphical images") used to depict molecular bonds.

## Formal definition

An undirected graph is a pair G = (V, E), where V is a set of vertices and E is a set of unordered pairs {u, v} of vertices called edges. The **order** of a graph is |V| (usually n); the **size** is |E| (usually m), though in complexity discussions "size" sometimes means |V| + |E|. The **degree** of a vertex is the number of edges touching it; a loop (an edge from a vertex to itself) counts twice.

Two vertices joined by an edge are **adjacent**; the edge is **incident** to both. A vertex with no edges is **isolated**. A **multigraph** permits several edges between the same pair of vertices. A **graph with loops** permits edges of the form {v, v}. When loops and multiple edges are excluded, the graph is a **simple graph**. A graph with no vertices is an **empty graph**.

For a simple graph of order n, the maximum possible degree is n − 1 and the maximum number of edges is n(n − 1)/2; allowing loops raises these to n + 1 and n(n + 1)/2.

A graph can also be encoded as an n × n **adjacency matrix** A, where A[i][j] counts edges from vertex i to vertex j. For a simple undirected graph A[i][j] is 0 or 1, A[i][i] = 0, and A is symmetric. Allowing loops gives nonzero diagonal entries; allowing multiple edges raises entries above 1.

A **directed graph** replaces unordered pairs with ordered pairs: G = (V, E) where E ⊆ {(x, y) : x ≠ y}. In the edge (x, y), x is the **tail** and y the **head**. To allow multiple directed edges between the same endpoints, use the triple G = (V, E, φ) with an incidence function φ mapping each edge to an ordered pair; this is a **directed multigraph**. A **mixed graph** carries both directed and undirected edges. A **weighted graph** assigns a number (a cost, length, or capacity) to each edge, which is how shortest-path problems such as the traveling salesman problem are posed.

## Important varieties of graph

- **Complete graph** Kₙ: every pair of vertices is joined. K₅ has five vertices and ten edges.
- **Bipartite graph**: vertices split into two sets W and X with all edges running between them, none within; equivalently, a graph with chromatic number 2. A **complete bipartite graph** has every possible W-to-X edge.
- **Path graph** of order n: vertices v₁, …, vₙ with edges {vᵢ, vᵢ₊₁}; the two endpoints have degree 1 and the rest degree 2.
- **Cycle graph** of order n ≥ 3: a path plus the edge {vₙ, v₁}; every vertex has degree 2.
- **Tree**: a connected undirected graph in which any two vertices are joined by exactly one path, equivalently connected and acyclic. A **forest** is an acyclic undirected graph, a disjoint union of trees. A **polytree** is a directed acyclic graph whose underlying undirected graph is a tree.
- **Planar graph**: one that can be drawn in the plane without edges crossing.
- **Regular graph**: every vertex has the same degree k (a k-regular graph).
- **Connected graph**: every pair of vertices is linked by a path; otherwise **disconnected**. In a directed graph, **strongly connected** means a directed path runs both ways between every ordered pair; **weakly connected** means the underlying undirected graph is connected. A graph is **k-vertex-connected** if removing any k − 1 vertices leaves it connected.

## Operations and generalizations

Standard operations build new graphs from old. Unary ones include edge contraction, the line graph, dual graph, complement, and graph rewriting; binary ones include disjoint union and the cartesian, tensor, strong, and lexicographic products.

Several structures generalize graphs. A **hypergraph** lets a single edge join any positive number of vertices. Viewing each edge as a 1-simplex and each vertex as a 0-simplex makes a graph into a **simplicial complex**, and complexes generalize graphs by allowing higher-dimensional simplices. Every graph also gives rise to a **matroid**. In category theory, a small category has an underlying directed multigraph whose arrows are the morphisms, via a forgetful functor to the category of quivers. In computer science, directed graphs represent finite-state machines and knowledge structures such as conceptual graphs, and a binary relation on a set X is itself a directed graph whose edges are the related pairs.
