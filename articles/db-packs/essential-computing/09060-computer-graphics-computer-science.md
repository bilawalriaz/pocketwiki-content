# Computer graphics (computer science)

Computer graphics is a sub-field of computer science that studies methods for digitally synthesizing and manipulating visual content. Although the term often refers to three-dimensional graphics, it also covers two-dimensional graphics and image processing. The discipline focuses on the mathematical and computational foundations of image generation rather than purely aesthetic concerns, and it shares territory with the related field of visualization, which also works with visual and geometric information but has its own emphases.

## What the field works with

Computer graphics is connected to applied mathematics, computational geometry, computational topology, computer vision, image processing, and scientific and information visualization. Its everyday applications include print design, digital art, special effects, video games, and visual effects.

The work divides into a small number of large subfields:

- Geometry: how to represent and process surfaces.
- Animation: how to represent and manipulate motion.
- Rendering: algorithms that reproduce how light travels through a scene.
- Imaging: acquiring or editing images.

## Geometry: representing surfaces

Because an object's appearance depends largely on its exterior, graphics systems usually store a boundary representation, typically a 2D surface. Since real surfaces are not finite, computers store discrete approximations. Polygonal meshes, and to a lesser extent subdivision surfaces, are the most common representation, though point-based representations have grown more popular. Surface simplification, which produces successive coarser approximations of a mesh, is a common operation.

These representations are usually Lagrangian, meaning the spatial samples move with the surface. For deforming surfaces that undergo many topological changes, such as fluids, Eulerian descriptions such as level sets, where spatial samples stay fixed, are often a better fit. Geometry includes implicit surface modeling, digital geometry processing (reconstruction, simplification, fairing, mesh repair, parameterization, remeshing, mesh generation, surface compression, and editing), discrete differential geometry, point-based graphics, and out-of-core mesh processing for datasets too large for main memory.

## Animation: representing motion

Animation describes how surfaces and other phenomena move or deform over time. Most historical work used parametric and data-driven models; physical simulation, including cloth modeling and fluid dynamics, has become more common as computers have grown more powerful. Subfields include performance capture, character animation, and physical simulation.

## Rendering: turning a model into an image

Rendering generates an image from a model. It may simulate light transport to produce photorealistic images, or it may deliberately use a non-photorealistic style. Realistic rendering reduces to two basic operations: transport, the amount of light that passes from one place to another, and scattering, how a surface interacts with light at a given point. Visibility is a major part of transport. Scattering is described by a bidirectional scattering distribution function (BSDF), and shading describes how material properties vary across a surface, both of which are usually written in a program called a shader. Rendering subfields include transport, scattering, non-photorealistic rendering, physically based rendering, real-time rendering (typically on GPUs), and relighting.

## A short history

Computer graphics emerged from advances in computing, display technology, and human-computer interaction. Early systems used vector displays. A foundational milestone came in 1963, when Ivan Sutherland's Sketchpad ran on the TX-2 and let users create and manipulate line drawings in real time with a light pen, an achievement that also seeded computer-aided design.

During the late 1960s and 1970s, research groups such as the University of Utah graphics lab pushed the field from wire-frame line drawings toward polygonal models, shaded surfaces, and computer animation. In 1975 Martin Newell created the Utah teapot, which became a standard test model for rendering techniques and visual realism. In the late 1970s and 1980s, raster graphics made more realistic images practical, and by the 1990s dedicated graphics processing units made real-time 3D graphics increasingly practical on personal computers, workstations, and game systems. The field developed dedicated venues: SIGGRAPH, formally organized in 1969, Eurographics, founded in 1980, and the journal ACM Transactions on Graphics.

## Tools of the trade

By category, common software reflects the same divisions. Bitmap and image editing tools include Adobe Photoshop, Corel Photo-Paint, GIMP, and Krita. Vector drawing tools include Adobe Illustrator, CorelDRAW, Inkscape, Affinity Designer, and Sketch. Architecture tools include AutoCAD, FreeCAD, VariCAD, QCAD, LibreCAD, DataCAD, and Corel Designer. Video editing tools include Adobe Premiere Pro, Sony Vegas, Final Cut, DaVinci Resolve, Cinelerra, and VirtualDub. Sculpting, animation, and 3D modeling tools include Blender 3D, Wings 3D, ZBrush, Sculptris, SolidWorks, Rhino3D, SketchUp, 3ds Max, Cinema 4D, Maya, and Houdini. Digital composition tools include Nuke, Blackmagic Fusion, Adobe After Effects, and Natron. Renderers include V-Ray, RedShift, RenderMan, Octane Render, and Mantra.
