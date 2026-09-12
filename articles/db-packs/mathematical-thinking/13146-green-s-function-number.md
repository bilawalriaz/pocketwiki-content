# Green's function number

A Green's function is the response of a material to an instantaneous point source, and it lets engineers build the solution to any forcing problem by summing such point responses. Real bodies have edges, surfaces, and centers, and each of those locations forces a particular mathematical condition on the response. Cataloging those conditions by hand is error-prone, so in 1988 Beck and Litkouhi proposed a short code—the Green's function number—that labels the coordinate system and the boundary conditions in one glance. The code is purely about geometry and boundary type, so it applies to any linear differential problem with the same structure: diffusion, acoustics, electromagnetics, and fluid dynamics, in addition to heat conduction.

The code has two parts. The leading letter or letters pick the coordinate system: X, Y, Z for Cartesian; R, Z, φ for cylindrical; RS, φ, θ for spherical. The digits that follow describe what happens at each geometric boundary of the domain, one digit per boundary, listed in the order the coordinate is written.

Four digit values cover every standard situation:

- 0 marks a place where no physical boundary exists but the solution must remain finite, such as far away in a semi-infinite body or at the center of a cylinder or sphere. Treating this as its own category lets the code handle infinite and bounded geometries uniformly.
- 1 is a Dirichlet condition, G = 0 at the boundary.
- 2 is a Neumann condition, ∂G/∂n = 0, meaning no flux crosses that surface.
- 3 is the Robin condition k∂G/∂n + hG = 0, which mixes conduction and convection and models a surface losing heat to a surrounding fluid. Here k is thermal conductivity and h is the convective heat transfer coefficient.

A few worked cases show how the digits map to geometry. X11 names the one-dimensional slab between x = 0 and x = L with Dirichlet boundaries on both faces. X20 names a semi-infinite solid from x = 0 to infinity with Neumann at x = 0; the trailing 0 advertises that infinity is a "must stay finite" boundary, not a wall. X10Y20 names a quarter-infinite plate, Dirichlet on the x = 0 edge and Neumann on the y = 0 edge, with both infinite directions flagged as 0. Two and three dimensions are handled by concatenating coordinate blocks.

In cylindrical coordinates, R03 is the Green's function for a solid cylinder of radius a with Robin cooling on its curved surface and boundedness at the axis. R10 describes a large body containing a cylindrical void of radius a whose inner wall satisfies Dirichlet, with boundedness at large r. R01φ00 adds the azimuthal angle φ and uses 00 for the angle because the angle wraps around: periodic continuity, where G and ∂G/∂φ both match at φ = 0 and φ = 2π, is recorded as two type-0 boundaries rather than as its own digit. RS02 does the same job for a solid sphere of radius b with Neumann at the outer surface and boundedness at the center.

The label points to a unique boundary value problem, and that uniqueness is what makes the system useful for indexing and retrieving Green's functions from large reference collections.
