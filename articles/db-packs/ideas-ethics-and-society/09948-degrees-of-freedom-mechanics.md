# Degrees of freedom (mechanics)

In physics, the **degrees of freedom (DOF)** of a mechanical system is the number of independent parameters needed to completely specify its configuration. A train on a track has one DOF, described by a single distance. A car with stiff suspension, treated as a rigid body on a plane, has three DOF: two translations (forward/back and side-to-side) plus one rotation (heading). A free rigid body in three-dimensional space has at most six DOF: three translations and three rotations, written **3T3R**.

These six are conventionally named surge, sway, and heave for translation, and roll, pitch, and yaw for rotation. A ship at sea uses all six. An aircraft in flight has three DOF for trajectory and three for attitude, again totalling six. Lower mobility arises when constraints remove some. A block on a flat table keeps two translations and one rotation (2T1R, three DOF). A SCARA-style XYZ robot keeps only three translations (3T, three DOF). A human arm modelled as an open kinematic chain has seven DOF: three rotation axes at the shoulder, one at the elbow, three at the wrist. Because a pose in space only needs six, the extra DOF is called *redundancy*, useful for example to swing the elbow around an obstacle.

A deformable body can be thought of as infinitely many point particles, giving it effectively infinite DOF. In practice it is approximated by a finite-DOF model, or even as a rigid body, when the analysis concerns large overall motions rather than internal deformation, as in satellite dynamics.

## Counting DOF: particles and constraints

The DOF of a system is the minimum number of coordinates needed once all constraint equations are applied. A single particle in a plane needs two coordinates (two DOF); in space, three (three DOF). Two free particles in space together have six DOF. Tying them at a fixed distance, as in a diatomic molecule, imposes one constraint equation and reduces the count to five: pick any five coordinates, then solve the distance formula for the sixth.

## The mobility formula for linkages

For a mechanism built from many rigid links joined by joints, the **mobility formula** gives the total DOF. Each free rigid body in space contributes six DOF, so *n* moving bodies contribute 6*n*. A joint removes DOF: a one-DOF joint (hinge, slider) imposes 6 − 1 = 5 constraints, a two-DOF joint (cylindrical) imposes 4, and so on. With *j* joints, each removing 6 − *fᵢ* DOF, the mobility is

**M = 6*n* − Σ(6 − *fᵢ*) = 6(N − 1 − *j*) + Σ *fᵢ***

where N includes the fixed ground link, so N = *n* + 1. Two special cases matter.

- **Simple open chain** (serial manipulator, one end fixed to ground): N = *j* + 1, so M = Σ *fᵢ*. A serial robot of six revolute or prismatic joints has M = 6.
- **Simple closed chain** (a loop, both ends attached to ground): N = *j*, so M = Σ *fᵢ* − 6. The RSSR spatial four-bar has four one-DOF joints summing to eight, giving M = 2, one being rotation of the coupler about the line joining its two spherical joints.

When the design restricts every body to move in parallel planes (a planar linkage) or on concentric spheres (a spherical linkage), each free link has three DOF instead of six, the formula's constant changes from 6 to 3, and the closed-chain correction becomes −3. A planar four-bar, a closed loop with four one-DOF joints, gives M = 4 − 3 = 1, matching its single input crank.

## Holonomic and non-holonomic systems

A system whose controls cover all of its DOF is **holonomic**; one whose controls cover fewer is **non-holonomic**. A car-like robot in 2D needs three coordinates to describe its pose, two for position and one for heading, but at any instant has only two controls (forward motion and steering angle), so it is non-holonomic. A fixed-wing aircraft with three or four control inputs (forward motion, roll, pitch, and to a limited extent yaw) flying through 3D space is likewise non-holonomic: it cannot move straight up, down, left, or right.

## Exact constraint design

A device can be under-constrained (wobbly, with uncontrolled motion) or over-constrained (jamming, with stress in the structure). Linkages are designed using the **exact constraint method**, which matches the number and direction of constraints precisely to the DOF that should remain.
